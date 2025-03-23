---
layout: projectpage
title: End-to-end causal inference
description: '[<a href=''https://github.com/py-why/dowhy''>DoWhy</a>, <a href=''https://www.pywhy.org/''>PyWhy</a>] Unlike prediction, causal inference depends critically on assumptions: "no causes in, no causes out". To help researchers formally state and verify causal assumptions, I built DoWhy, an open-source Python library that is widely used across industry and academia. I now work on methods to improve the state-of-the-art for verification and robustness tests in causal inference.'
importance: 2
category: work
related_publications: true
---

Unlike prediction, causal inference depends critically on assumptions: "no causes in, no causes out". To help researchers formally state and verify causal assumptions, I built DoWhy {% cite sharma2020dowhy %}, an open-source Python library that conceptualizes causal inference as a four-step process: model, identify, estimate and refute. The library has over three million downloads and is widely used across industry and academia. A key benefit is that Dowhy allows users to verify their causal assumptions using state-of-the-art validation checks. I continue to work on building better methods to validate causal assumptions.

However, two limitations still exist for applying causal methods in practice: 1) reliance on the user to provide a causal graph upfront; 2) complexity of assumptions that make it difficult to choose the right estimation method given a dataset. In late 2022, I stumbled upon [an interesting discovery](https://arxiv.org/abs/2305.00050): LLMs are really good at inferring causal relationships from scientific literature and in some cases, can even suggest missing relationships or confounders for a study {% cite kiciman2024-frontiers %}. Based on these results, my current research focuses on how LLMs can be used to alleviate both these challenges. See [PyWhyLLM](https://github.com/py-why/pywhyllm) for early demos on how LLMs can accelerate the process of building a causal graph and how they can be used to guide a user on different choices during a causal analysis.

In the future, I hope that we can democratize causal analysis and increase its adoption across science and business: users may specify a causal query in natural language and the system can work with them to answer their query. To enable this vision, I also work on fundamental improvements to causal effect estimation and root-cause analysis methods.

<div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pearl_dowhy_tweet.png" class="img-fluid rounded z-depth-1" %}
</div>

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
{% for repo in site.data.repositories.gh_causal_repos %}
{% include repository/repo.liquid repository=repo %}
{% endfor %}
</div>

##### Scalable causal effect estimation

- Estimating causal effect of online recommendation systems on our behavior {% cite Sharma2018-rr Sharma2016-qk Sharma2015-as %}
- Estimating causal effect of a novel intervention using proxies {% cite Xu2021-eh %}

##### Scalable root-cause analysis

- Scalable methods for root cause diagnosis {% cite nagalapatti2025robust sharma2022counterfactual %}

##### Democratizing causal analysis

- Algorithms that can infer causal relationships using both existing knowledge and data {% cite vashishtha2025causal %}
