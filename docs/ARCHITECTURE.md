# Sanitized architecture case study

## Research question

How can a local legal AI system remain useful across multiple workflows without allowing retrieved
text, user assertions, conversation memory, and model generations to collapse into one untraceable
context?

## Design

The prototype uses four conceptual layers:

1. **Workspace and authorization.** Conversations, matters, documents, and workflow artifacts are
   scoped to an authenticated tenant and matter boundary.
2. **Evidence acquisition.** Uploaded documents, OCR/VLM observations, internal knowledge, and
   legal sources retain distinct provenance and authority metadata.
3. **Workflow orchestration.** Seven tools share a common run contract while applying
   workflow-specific required inputs and output schemas.
4. **Verification and presentation.** Generated claims are checked against eligible evidence.
   Unsupported output can be downgraded, accompanied by a warning, or withheld.

## Deployment model

The primary target is on-premises operation. Local model serving, document processing, and vector
storage remain inside the deployment boundary. An optional legal-data gateway is conceptually
separated from user documents and model inference, allowing only approved source synchronization.

## Important boundaries

- Conversation memory helps continuity but is not promoted to legal authority.
- Retrieval relevance does not override legal-source hierarchy.
- OCR and VLM observations are evidence candidates, not verified facts.
- A completed model response is not equivalent to an accepted legal answer.
- Production deployment would still require current authoritative data, professional legal review,
  identity integration, key management, retention policies, and operational validation.

Implementation details and source code are intentionally excluded from this public case study.
