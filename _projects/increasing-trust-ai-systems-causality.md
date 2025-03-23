---
layout: projectpage
title: Increase trust in AI systems
description: "[<a href='https://github.com/interpretml/dice'>DiCE</a>] Just like medical treatments or economic policies, AI systems can be considered as interventions in our society. I build methods to help experts interpret an AI system's output and estimate their (differential) impact on different subpopulations. One of these methods, Diverse Counterfactual Explanations (DiCE), has been integrated as a part of Microsoft's Responsible AI platform."
importance: 3
category: work
related_publications: true
---

Just like medical treatments or economic policies, AI systems can be considered as _interventions_ in our society. I build methods to help experts interpret an AI system's output and estimate their (differential) impact on different subpopulations. One of these methods, Diverse Counterfactual Explanations (DiCE), has been integrated as a part of Microsoft's Responsible AI platform.

I also work on improving the generalizability of ML models so that they are less sensitive to their training data distribution. This line of work has led to a NASSCOM AI GameChangers Award (2023-24).

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
{% for repo in site.data.repositories.gh_trustworthyai_repos %}
{% include repository/repo.liquid repository=repo %}
{% endfor %}
</div>

##### Counterfactual explanations

- A methods that generates diverse counterfactual explanations for explaining ML classifiers {% cite Mothilal2020-tp %}
- Using LLMs-generated counterfactuals to explain AI model's predictions {% cite Gat2024-yc %}
- Unifying feature attribution and counterfactual explanation methods: When to use which {% cite Kommiya_Mothilal2021-xi %}
- Evaluating and mitigating bias in image classifiers {% cite Dash2020-ls %}

##### Building prediction models that generalize better

- The challenges of prediction and explanation in social systems {% cite Hofman2017-ee %}
- Using causal reasoning to build generalizable ML classifiers {% cite Mahajan2020-nn Kaur2023-ks Kancheti2022-ds Kumar2023-mh Bansal2023-sa %}

##### Role of causality in trustworthy ML

- The necessary role of causality in understanding when ML explanations can improve human understanding {% cite Chen2023-vb %}
- A framework for deploying trustworthy ML systems based on technology readiness levels {% cite Lavin2022-zi %}
- ML fairness estimates can be misleading without modeling data missingness {% cite Goel2021-tg %}
