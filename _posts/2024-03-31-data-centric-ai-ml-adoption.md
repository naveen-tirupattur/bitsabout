---
layout: post
title: "Data centric approach to AI/ML"
date: 2024-03-31
--- 
As companies race to adopt AI/ML into their workflows and products, the need for a cohesive data strategy has never been
more important. This wave is being driven by the huge improvements in the capabilities of models via 
novel architectures and cloud computing that has democratized the ability to train/deploy/host these models at scale. 
However, the another important factor is the ubiquity of data available for training and inference. This has been made 
possible by the 2010s wave of Big Data that led to emergence of tools and platforms to collect, ingest, process and 
store huge amounts of data. 

Having the right data is more important than having a lot of data. The right data can be defined as: 
1. data that is relevant to the problem you are trying to solve. 
2. data that you can trust (this is a bit more nuanced, I will explain this in detail below).

## Unpacking Data Trustworthiness: A Critical Component
Let's dive deeper on the second point - data that you can trust. This is a very important aspect that is often overlooked.
Quality of the data is as important as the quality of the model. This is because, even the best model will not 
perform well if the data is of poor quality.

What is trustworthy data? 
* data that is accurate, complete and consistent.
* data that is free from biases, and anomalies.
* data that is discoverable, well-documented, well-understood, and well-organized. 
* data that is compliant with regulations and has privacy guardrails.

A cohesive and a comprehensive data platform is a pre-requisite for trustworthy data. In this post I will focus on a few
key aspects of data platform that are important for building trust in data: observability and metadata.

### Observability
It's the ability to measure and monitor the state of data for correctness, completeness and consistency. From my experience data quality issues can be very complicated to troubleshoot and expensive to fix. It is often due to disconnect between the data producers and consumers. Data contracts is a concept that is gaining traction to bridge this gap. I think this will help in early detection of data quality issues centered around data correctness(regex matching, value checks etc.) and schema changes that break things downstream. However, the observability system should also monitor for data delays, anomalies in data and ensure consistency of data(no missing data etc.) during its entire lifecycle. In the context of AI/ML, it is also important to detect for bias in the data, monitor for data, concept and model drift to ensure that the data is representative of the real world. Bias detection is a complex problem and is beyond the scope of this post. This system to should also provide alerts and notifications to the data producers and consumers when there are issues with the data. It should also provide a way to surface information about data quality like:
* SLAs: What are the SLAs around the data like freshness, correctness and completeness? Are they being met?
* Checks: What checks have been configured and run on the data, and what was the result of those checks?

### Metadata
Data is often siloed in different systems, owned by different teams, and it is hard to find the right data for the problem you are trying to solve. Apart from cataloging the data for search and browse(schema, sample values, field descriptions etc.), there is a need for single source of truth for metadata to enable better understanding of data and trust in data. It should provide the provenance and lineage of the data (how it was created, transformations that have been applied etc.). Along with this, it should also provide metadata about data quality, access controls, retention policies, and privacy policies (like whether PII has been removed) around the data. Lack of understanding and trust in data tends to cause proliferation of data silos leading to data duplication, inconsistency. It also has cost impact due to time and resources spent in creating and maintaining these silos. 

Apart from building trust in the data, a single source of truth will help in making the data more usable. Building this requires a lot of coordination between different teams, and a buy-in from different stakeholders. Technical challenges aside, it also requires a shift in thinking about data. Data is often seen as a byproduct of the work that we do, and not as a product in itself. Successful implementation of data as product approach involves seamless interactions between various systems like data discoverability, data observability, data governance, data processing and data storage. It is important to establish best practices like ownership of data, naming standards, data modeling, clear SLAs around the data, and clear policies around data retention, data privacy. 

## Conclusion
In conclusion, a data centric approach to AI/ML is important for building trust in data. Trustworthy data leads to models whose performance can be reasoned about, and explained. This in turn leads to trust in the models, and better business outcomes. Building trust in data involves combination of product and process oriented thinking. Getting it right will have huge benefits in terms of cost savings from reduced data downtime and performance gains. Another important aspect that is generally missing in many organizations is the metrics to track the cost of data, and this makes it hard to justify the investments in data observability and metadata tracking. I think, treating data as product leads to better understanding of the cost of data, and the value it brings to the organization. It is a hard problem to solve, and getting it right will take time. Approaching this an iterative manner, and starting with the most important data is a good way to start. 






