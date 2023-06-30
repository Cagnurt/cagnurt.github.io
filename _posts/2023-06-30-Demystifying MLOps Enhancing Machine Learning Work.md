---
layout: post
title: "Demystifying MLOps: Enhancing Machine Learning Workflow and Addressing Key Challenges"
---

#### What is MLOps?

Main Source:

[https://azure.microsoft.com/en-in/resources/drive-efficiency-and-productivity-with-machine-learning-operations/](https://azure.microsoft.com/en-in/resources/drive-efficiency-and-productivity-with-machine-learning-operations/)

**MLOps:**

- Concept or way of working. Not a product or service
- Approach for streamlining end-to-end ML life cycle
- Does for Data scientists and/or ML engineers what DevOps does for developers

##### What problems does it address?

MLOps addresses the following gaps:

- DevOps teams strive to automate all their workflows, and for the most part, today they have. However, data scientists/ml engineers are excluded. For example, Git is a perfect tool for building, testing and deploying to a production environment. However, due to the nature of ML projects, Git can be an environment that makes this problematic.
- ML projects may require tuning, scalability, automation, and packaging. These tasks may take months, and the process is iterative. DevOps does not propose a strategy to support this continuity.

#### Versioning

##### What is dataset/model versioning?

It is the process of applying different naming of different stages of a data/model.

##### In which cases would it be useful?

- Facilitating easy sharing
- Collaboration
- Model reuse in an environment that includes comprehensive access control
- Traceability

##### How does it differ from software versioning?

In ML, the data changes over time, and models need to be retrained regularly, which is not the case for software engineering. If the module requires the requirements in the software engineering field, it is frozen.

#### ML in Academia vs. Industry

##### What are the differences between doing ML in academic and industrial settings?

|  | Academia | Industry |
| --- | --- | --- |
| Approach to Metric | Reach an unreached value | Reach an unreached value with many constraints such as less complexity, and low computational cost.  |
| Data | Encourage to open source | Confidentiality of both company and customer data |
| Model | No constrains | Large models are not preferred (as they will be used in real-time) |
| Deployment | No need deployment | Optimization has to be done considering the deployment phase |
| Pipeline | No constrains | Long-term and sustainable (Since it has deployment and mass production, it has a long life cycle) |
| Owner | Individual or Team | Company |
| Motivation | Internally motivated | Product-oriented |
| Money Support | Rare or few (at least for Turkey) | Full support from the company |

#### Performance Issues

##### Say your model has a decent test set performance but performs poorly in production. What could be the issue?

I assume that the performance refers to the metric in this question. Let's say you get high accuracy in your test set but not in production. These are the possible reasons:

- There might be a distribution shift:
    - The customer uses different data distribution than yours. For example, your test set does not cover your customer's need: Bilby is an Australian animal, not found in the animal photos you collected in Turkey. But one of your customers is from Australia and unhappy with this situation.
    - The customer uses different data structures. For example, your test set for image segmentation problems has a high resolution, ex. 1080. But the customers have low resolution, ex 360.
- There might be a concept drift. ("change in the relationships between input and output data in the underlying problem overtime")
    - Although you consider your customer's needs and your test set covers perfectly, the concept of that field may change.

If we assume that the performance refers to the needs:

- There might be a computational cost issue:
    - Your test environment has a higher and more powerful GPU but the production has poor. Although the model fits in the GPU, the evaluation process takes longer in real time. This could be a poor performance from the customer's point of view.
    - The model output requires memory. Your test environment has high memory, and memory is not an issue for you. But the product has less memory. Let us say after a few usages; the customer could not use the product without deleting the old ones because the memory is full. This could be a poor performance from the customer's point of view.

##### How would you address this problem?

The data in which the model fails is examined manually. Try to find a pattern among the data with an error. After finding, a dataset should be created and the model should be retrained with this new dataset. (It is for deep learning. If the data is for machine learning, a discovered or missing feature should be added.)
