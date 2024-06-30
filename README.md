# ServiceGenie
Bulding Customer Service using RAG and LLM

# Problem Statement

Gap in content driven customer service. Issues:
- Increase in customer base and increase in the customer queries.
- High cost to create content driven customer service. High man power as well high resources and time. 
- Losing good customers due to poor communications and hence losing potential customer and business.
- Lack of timely response to customers.
- Lack of common platform to know customer’s issues.


# Why are we solving this Problem statement?

- Enhance the customer service experience by leveraging generative AI technologies to provide personalized, efficient, and proactive support across multiple channels. 
- Automating customer service will reduce cost.
- With increase in customer queries, there is need to increase the resources, AI can help to reduce the burden on the existing resources.
- Increase in timely content driven message to customers, will lead to high customer retention. 
- Timely building features for issues which are faced by customers.

```mermaid
flowchart LR
    subgraph Customer Document Processing
        A[fa:fa-file Customer Documents] -->|Text Processing| T(fa:fa-scissors Text Processor)
        T -->|Processed Text| B(Text Chunks)
        B -->|Generate Embeddings| C(Text Embeddings)
        C -->|Save to Database| D[fa:fa-database Vector DB]
    end
    subgraph Customer Query Processing
        E[Customer Queries] -->|Text Processing| T
        T-->|Processed Text| F(Text Chunks)
        F -->|Generate Embeddings| G(Text Embeddings)
        G -->|k Nearest Neighbours Search| D[fa:fa-database Vector DB]
        D -->|Searched Vectors| R(User Content - K Nearest Neighbours)
    end
    subgraph Content Generation
    R --> |LLM Model| M(Azure OpenAI)
    M --> |Queries Processing| Q(Customer Query Output)
    M --> |Financial Analysis| I(Customer Financial Query GUI)
    M --> |Marketing Analysis| J(Cross Product Sell)
    end
    subgraph Marketing Input
    MI --> |Marketting context| R
    end
    subgraph Financial Input
    FI --> |Financial context| R
    end
```
