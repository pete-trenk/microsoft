https://gm-spacagna.medium.com/multi-index-retrieval-proven-strategies-for-efficient-accurate-knowledge-access-5b563c7abbed

What is the fundamental value of Foundry IQ? Who are its competitors?
Why information-retrieval and what's special about foundry IQ that couldn't be done with other embedding engines and vector stores?
- "Knowledge bases offer superior recall and cost tradeoffs" - what is recall in this sense and are knowledge bases something that only msft offers or is it just an architectural pattern?

1.) Central control and governance over the context used for information retrieval?

You control what knowledge sources comprise a knowledge base so you can define a domain of knowledge; applies to both indexed and remote knowledge sources.

Separation of duties

Observability and auditable - you get a single place to answer “what content grounded this answer, and was the user entitled to it?” That matters for NERC CIP and CEII reviews.

On-Behalf-Of (OBO) agent authentication
- an agent can be configured to inherit the permissions of the user that operates it to control what resources that user is able to access through agentic tasks (enforces role boundaries). Microsoft’s federated Copilot connectors work this way.

- document-level access control, enabling organizations to enforce fine-grained permissions at the document level
- ACLs/RBACs/Purview sensitivity labels

2.) Permission-aware access to indexed knowledge (auto-enforced, compliance)


You configure fine-grain permissions to documents a particular user can see within the content of a knowledge source, so agents return only content the user is authorized to see.

Note, user-level controls apply only when the source supports document-level permissions and those permissions are configured to sync.
- Sharepoint - a file or page (e.g., outage escalation policy)
- SQL (note, an indexed SQL knowledge sources isn't the same as access to a SQL table/database)
- - https://learn.microsoft.com/zh-cn/Azure/search/agentic-knowledge-source-how-to-azure-sql?pivots=python

For remote knowledge sources, permission enforcement is really a value add of Foundry IQ

3.) Token Efficiency
- "agentic retrieval that finds relevant data automatically without wasting tokens"

https://learn.microsoft.com/en-us/azure/search/samples-python
https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/foundry-iq-improve-recall-by-up-to-54-with-knowledge-bases/4524852

