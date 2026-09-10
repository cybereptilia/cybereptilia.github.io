---
layout: post
title: "Machine Learning in AI: What Machine Learning Actually Is"
date: 2026-09-09
---

The term Artificial intelligence by itself is an umbrella term. Machine learning is the instrument underneath it, and it does the work in almost every system promoted as AI today. For security professionals the distinction is important, given what a model is able to do or not depends significantly from how it learned.

## Learning instead of rules

Traditional software encodes decisions a human already made. A signature-based antivirus engine compares documents against a compilation an individual applied. The logic is explicit, auditable, and blind to anything not found on the list.

Machine learning changes this. Once you supply data, the algorithm takes charge in deriving the rule itself, producing a model that generalizes to inputs it has never seen before. Such generalization composes the value proposition, but it also contributes to every problem below. The model can classify a malware variant an analyst is yet to examine. It can also express confidence while being incorrect, for reasons no practitioner can inspect.

## How models learn

**Supervised learning** trains models based on labeled examples. Like ten million emails tagged as phishing or legitimate, and it classifies the eleven millionth. Its constraint is that labeling can be expensive and often unavailable for the more important threats.

**Unsupervised learning** works on unlabeled data, finding structure on its own. This is where anomaly detection comes in. It is never taught what an attack might look like, only what normal looks like, which often explains both its value against novel threats and its false positive rate.

**Reinforcement learning** trains through interaction, making decisions and receiving rewards or penalties, suiting sequential decision problems.

## Deep learning and generation

Deep learning makes use of neural networks with many layers, each building a more abstract representation than the last. Its importance is planted on the removal of feature engineering. Former methods required an expert to make decisions on which features of a file mattered, now deep networks learn the features themselves.

Generative models are the current frontier. Instead of classifying the input given, they produce output that resembles their training data. The shift from sorting elements that exist to creating things that do not is the most consequential change for security in a decade. 

## Why it matters both ways

On defense, machine learning powers phishing classification, malware detection, and behavioral analytics. These inherit the constraints above: a supervised model can only be as good as its labeled data, and an unsupervised model flags deviation, not malice.

On the offense side, generative capability changed the picture. Schmitt and Flechais, writing in *Artificial Intelligence Review* in 2024, map machine learning onto every stage of the social engineering attack lifecycle and identify three magnifying areas: realistic content creation, advanced targeting and personalization, and automated attack infrastructure. 

The asymmetry is worth noticing. A defensive model with just one percent positive rate is an operational liability. An offensive model with a one percent success rate across ten thousand targets can be a successful operation.

## The limits

Every model is dependent on its training data and inherits its gaps. Every model drifts as the environment distances itself from what it learned. Deep models tend to resist explanation, so something such as "the model flagged it" may be the only available answer. And models can and have been attacked directly through crafted inputs or poisoned training data, making the control itself an attack surface.

Having an understanding of the machine inside AI is what allows you to ask a vendor the correct questions. Not whether a product has AI implemented, but what it learned from, how often it is retrained, and what occurs when iit is wrong.

---

Schmitt, M., & Flechais, I. (2024). Digital Deception: Generative Artificial Intelligence in Social Engineering and Phishing. *Artificial Intelligence Review*, 57. [Preprint](https://arxiv.org/abs/2310.13715)


