---
layout: page
title: Visualizations
---
## Proposed MQA Pipeline
![](/assets/img/1.png)

Our proposed VQA system takes as input an image, its corresponding meta-data, and an associated question.

## Implementation Overview
![](/assets/img/8.png)

The overall workflow diagram of our project.

## Data Flow Diagram
![](/assets/img/7.png)

The data flow diagram of our proposed MQA system.

## System Design

### Instance Mask Generation Module
![](/assets/img/mask2former.png)

Our instance mask generation module utilizes Mask2Former, which is the recent SOTA framework for generating instance masks.

### Scene Graph Generation Module
![](/assets/img/sg_gen.png)

Scene graph generation module is responsible for generating a scene graph for the image if that is not provided as an input. Scene graphs represent visual scenes as objects and their attributes as nodes of the graph and the relationships between them as edges.

### Sub-components of Feature Extraction Module
![](/assets/img/4.png)

The feature extraction module takes the 4 inputs and processes them individually into a format that is then consumed by the QA model.

### QA Model Backbone 1: Single Stream - ViLT
![](/assets/img/ViLT.png)

We use ViLT as one of our baseline QA models, which is a recently proposed parameter efficient model following the single-stream architecture. ViLT processes the images similar to the textual inputs. 

### QA Model Backbone 2: Dual Stream - LEXMERT
![](/assets/img/5.png)

The LXMERT QA model has 2 separate streams for image and text modalities. Each stream focuses on individual modalities and encodes the relationships and interactions between different entities present in them.

### Parameter-Efficient Fine-Tuning: Adapter
![](/assets/img/adapters.png)

The architecture of the adapter layer and how it is incorporated into the transformer block.

### Parameter-Efficient Fine-Tuning: Prefix Tuning
![](/assets/img/prefixtuningvilt.png)

Prefix tuning is a light-weight alternative strategy to fine-tuning and is able to achieve comparable results especially in low-data resource settings. It is also shown to be more robust and generalisable when compared to fine-tuning.

## Dataset Analysis
![](/assets/img/gqa_1.png)

GQA question distribution analysis.

![](/assets/img/vqa_1.png)

VQA-2.0 question distribution analysis.

![](/assets/img/tally_1.png)

TallyQA question distribution analysis.

## Dataset Creation

### Data Generation Workflow
![](/assets/img/data_gen_workflow.png)

The workflow for generating our dataset for our VQA task.

### Question Generation Overview
![](/assets/img/qa_gen.png)

The question generation overview illustrates our question generation image sources and proposed numbers of generated questions for each split.

### Question Generation Workflow
![](/assets/img/qa_gen_wf.png)

The question generation workflow summarizes the process of our sampling and balancing process on GQA, VQA-2.0 and TallyQA.

### Question Sampling Overview
![](/assets/img/qa_sam.png)

The question sampling overview illustrates our sampling sources and sampling number for each split.

### Question Balancing Example on VQA-2.0
![](/assets/img/vqa_color_bal.png)

Comparison of our question balancing result on VQA-2.0 train split's color questions.

