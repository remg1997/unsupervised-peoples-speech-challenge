# Unsupervised Speech in the Wild Challenge Proposal

## Title

**Unsupervised Speech in the Wild: Learning Robust Multilingual Representations from Unsupervised People’s Speech**

## Organisers

**Challenge Organisers**

**1\. Rafael Mosquera-Gómez (MLCommons / Factored AI,** [rafael.mosquera@mlcommons.org](mailto:rafael.mosquera@mlcommons.org))  Rafael Mosquera-Gómez is a Machine Learning Engineer at Factored AI, where he leads projects at the intersection of AI systems and real-world impact. He is a core contributor to the MLCommons Datasets Working Group, with recent work focusing on low-resource NLP in collaboration with Common Crawl. His research interests lie in developing practical and human-centered evaluation methods for LLMs, particularly in high-stakes domains. Rafael recently co-authored the top paper award winner at NeurIPS 2024: *The PRISM Alignment Dataset*, highlighting the potential of survey-based evaluations and participatory alignment.

**2\. Sarah Luger (MLCommons / iMerit,** s[arahluger@gmail.com](mailto:sarahluger@gmail.com))  
Dr. Sarah Luger is an expert in Artificial Intelligence and Natural Language Processing with over two decades of experience, specializing in human communication challenges. She leads the Generative AI Research group at iMerit and is co-chair of the MLCommons Datasets Working Group. Her work spans low-resource MT, online harm detection, annotator diversity, and responsible AI practices. She holds a PhD in Informatics from the University of Edinburgh and previously contributed to IBM Watson. Sarah has held leadership roles across the AI and human computation communities, including organizing evaluation-focused tutorials at IEEE AITest and AAAI.

**3\. Daniel Galvez (NVIDIA, [dt.galvez@nvidia.org](mailto:dt.galvez@nvidia.org) )**

Daniel Galvez is an AI developer technology engineer at NVIDIA, where he works on accelerated speech recognition inference pipelines and toolkits like NeMo, ESPnet, and Kaldi. Prior to joining NVIDIA, he worked on content recommendation and NLP at LinkedIn, and on the Kaldi Automatic Speech Recognition software at Cornell University.

**4\. Sheriff Issaka (UCLA / All Lab,)**  
Sheriff Issaka is a PhD student at UCLA researching bias, fairness, and low-resource language technologies at the MARS Lab. He founded the African Languages Lab (All Lab), an initiative advancing linguistic equity through open-source research and resource development. His work explores multi-turn safety alignment for LLMs and clinical ML with a focus on equitable AI outcomes.

**5\. Chiara Bonfanti (Politecnico di Torino)**  
Chiara Bonfanti is a PhD researcher in Natural Language Processing and Legal Informatics at Politecnico di Torino. Her work centers on semantic analysis and knowledge extraction from complex legal texts, bridging law and cybersecurity domains. She has also contributed to computational pipelines for low-resource language translation.

**6\. Chris Emezue (Mila / Lanfrica)**  
Chris Emezue is a researcher at Mila focused on NLP, causality, and reinforcement learning, with a commitment to enabling AI for low-resource contexts. He is the founder of Lanfrica Labs, a non-profit mapping the landscape and trajectory of AI in Africa, to accelerate innovation and enable a holistic understanding of the continent's AI representation, gaps, and risks.

**7\. Juan Felipe Rodríguez (Factored AI, [juan.rodriguez@factored.ai](mailto:juan.rodriguez@factored.ai) )**  
Juan Felipe Rodríguez is a Machine Learning Engineer specializing in AI systems for education and talent mobility. With a background in computational fluid dynamics and robotics, he has built and deployed large-scale applications powered by modern language models and intelligent systems.

## Introduction

This challenge evaluates **self‑supervised speech representation learning** on real‑world heterogeneous audio at scale. Participants train models **without transcripts** using **Unsupervised People’s Speech (UPS)**. Performance will be assessed via phonetic discrimination, low‑resource ASR probes, multilingual language ID, and speaker clustering.

## Significance

This challenge advances speech research by moving beyond curated corpora  emphasizing multilingual and accent diversity with realistic environments that include noise and music. By evaluating self‑supervised models on spontaneous and heterogeneous audio, the challenge promotes scalable, inclusive representation learning aligned with the Interspeech 2026 theme **“Speaking Together”**, encouraging models that generalize across global voices and real‑world scenarios.

## Rules for Participation

All submissions will consist of trained models submitted through the Dynabench platform and evaluated under controlled conditions to ensure reproducibility and fairness. Participants must train exclusively on the Unsupervised People’s Speech dataset, without the use of transcripts or supervised external data. Submitted models must adhere to transparent reporting requirements, including full disclosure of training configuration, compute usage, and data preprocessing or filtering steps. To guarantee reproducibility, all models must be capable of running inference on a **single A100 GPU at most**, and participants may choose between the main track or the open filtering sub‑track. Dynabench will handle model execution and interactive robustness evaluation.

## Evaluation

The primary evaluation for this challenge will focus on three key metrics that reflect real‑world speech understanding performance: few‑shot ASR accuracy, zero‑shot multilingual language identification, and speaker clustering quality. These metrics collectively assess how well models learn generalizable and language‑agnostic representations from unlabeled audio. Additional considerations, such as cross‑accent robustness and efficiency, will be included to ensure fairness and reproducibility. A leaderboard will rank submissions based on overall performance across these criteria, establishing a clear benchmark for unsupervised speech representation learning.

## Datasets and Baselines

The Unsupervised People’s Speech (UPS) dataset is already publicly available via Hugging Face, enabling immediate and open access for participants. Challenge participants will be provided with official dataloaders designed for efficient streaming and large scale training, ensuring ease of use and reproducibility. In addition, we will release precomputed language identification indices which have been generated using **Whisper 3.0**, offering participants lightweight language guidance without supplying explicit supervised labels. Training will be conducted on designated unlabeled UPS subsets, while evaluation will rely on held‑out multilingual labeled datasets. Baseline systems, including wav2vec2, HuBERT, XLSR, and a Whisper encoder baseline, will be provided to establish performance references for the leaderboard.

## Timeline

* **Release & Baselines:** 12 December 2025

* **Paper Submission Deadline:** 25 February 2026

* **Paper Update Deadline:** 4 March 2026  
* **Rebuttal Period:** 24 April – 1 May 2026  
* **Paper Acceptance Notification:** 5 June 2026  
* **Camera‑Ready Paper Submission:** 19 June 2026  
* **Tutorial Day:** 27 September 2026  
* **Interspeech Conference:** 27 September – 1 October 2026

## Ethics & Conduct

All participants must adhere to the ISCA Code of Conduct, ensuring professional behavior, respect for community standards, and the responsible advancement of speech research. The challenge data is drawn from legally shareable subsets of the Unsupervised People’s Speech dataset, with appropriate ethics documentation and approvals in place. Participants are strictly prohibited from attempting to identify speakers or infer sensitive personal attributes, and all submissions must reflect responsible AI development practices. This challenge emphasizes fairness, transparency, and ethical model evaluation, promoting a research environment that respects data contributors, prioritizes privacy, and advances equitable multilingual speech technology.

## Reviewers

Proposed expert reviewers:

* R. Alexander Milowski

* Jade Newton

* David Adelani

* Abigail Walsh

* Senjuti Dutta

* Marcos Zampieri

* Annie En-Shiun Lee

* Armstrong Foundjem

* Tajuddeen Gwadabe