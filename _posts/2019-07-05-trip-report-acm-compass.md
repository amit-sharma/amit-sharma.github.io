---
layout: post
title: "Trip report from ACM COMPASS: 2nd Conference on Computing and Sustainable Societies"
date: 2019-07-05
description: highlights from the conference
tags: societal-impact trip-report
categories: societal-impact
---

Last year, I attended the inaugural ACM conference on Computing and Sustainable Societies ([COMPASS](http://www.acmcompass.org)) and was immediately sold on the vision: a conference on the _societal impact of computing systems_. In the backdrop of increasing concerns on the use of artificial intelligence in decision-making, threats to environmental sustainability, and the long-standing challenges we face in global development, it only makes sense to think how computing technologies can be applied for social good. What I also liked was the inclusive nature of the conference: whether you work in HCI, systems, data science, machine learning or any other field of computing, all such work is welcome. From the outset, it looked like a grand experiment in creating a computing research community focused on societal impact (rather than methods), almost too good to be true.

The second edition of the conference just concluded and I'm glad to report that the experiment is thriving. There were a number of exciting talks across systems, HCI and data science. There is also a considerable presence from both industry and academia, including NGOs and social enterprises. The full list of talks is available [here](https://acmcompass.org/accepted-papers) ([Day 1](https://www.youtube.com/watch?v=46gIqhB24KU), [Day 2](https://www.youtube.com/watch?v=hzjqvB97B8k), [Day 3](https://www.youtube.com/watch?v=6IuBX3CJn9o)). Below I touch upon a few highlights.

## Low-cost sensing

There is a lot of promise around sensors to enable informed decision-making using real-time data and help in monitoring cities, traffic, infrastructure, agricultural fields and even the environment. Often, however, the high cost of sensors make them impractical for deployment in the Global South. [Engineer Bainomugisha](http://ibaino.net/index.html) from Makerere University gave an impressive talk on using low-cost sensors for tracking air pollution. They have even [deployed hundreds](https://www.airqo.net) of them in Kampala, Uganda! Data from these pollution sensors enable a more granular view of the problem (e.g., by different parts of a city) and has the potential to transform how local governments tackle pollution.

{% include figure.liquid loading="eager" path="assets/img/airqo.png" class="img-fluid rounded z-depth-1" title="A live map report from Kampala, Uganda [Source: The AirQo project.]" %}

<div class="caption">
   A live map report from Kampala, Uganda [Source: The AirQo project.]
</div>

Aerial imagery can be another way for sensing in low-resource contexts. Using satellite data, one of the papers developed an algorithm to determine road quality in Kenya. Another paper from my colleagues in MSR India developed a low-cost alternative to drones for monitoring agricultural fields using a helium ballon and a smartphone (Best Paper Award). These papers utilized machine learning models for computer vision and I think there is a lot to explore in applying machine learning methods on these datasets.

## Interactive Voice Response (IVR) systems

IVR? Many in the Global North may associate IVR phone systems with frustrating customer service experiences. But due to low penetration of smartphones and data access in many parts of the Global South, IVR systems are one of the biggest successes as platforms for information sharing. Over the past few years, the ICTD community has developed IVR solutions for applications such as [citizen journalism](http://cgnetswara.org), [maternal and child health](http://www.cse.iitd.ernet.in/~aseth/genderNtechICTD19-1909-01.pdf), [agricultural and health practices](https://gramvaani.org), and more. This year we saw an impressive study on using IVR systems to augment school lessons for children in low-resource communities (Best Paper Award). The authors created a set of questions that complement school lessons for French language in a rural community in Côte d'Ivoire and found how the family plays a key role in helping children interact with the system. I also got a chance to present two of our projects on IVR: one on models of spreading mass awareness through IVR, and another on evaluating a social network for people with disability (in collaboration with an NGO, [Enable India](http://www.enableindia.org)).

## Mechanism design

Another theme that came out throughout the conference was on designing incentives and efficient markets for social good. One of the talks was on setting incentives for encouraging people to collect images of birds in under-represented areas, another optimized incentives for spreading awareness by sharing with peers. More generally, these problems fall under the broad definition of mechanism design. [Daniel Mutembesa](https://scholar.google.com/citations?user=5Bou78sAAAAJ&hl=en) gave a great tutorial on mechanism design and talked about a project on encouraging field workers to [collect images](http://air.ug/mcrops/) of the cassava crop, one of the staples in Africa. Given the ubiquity of field workers in agriculture, health and finance in the Global South, I look forward to more work on incentive design.
{% include figure.liquid loading="eager" path="assets/img/mcrop.png" title="Mcrop system for crowdsourcing images of diseased cassava crop [Source: Mutembesa et al. 2018]" %}

<div class="caption">
    Mcrop system for crowdsourcing images of diseased cassava crop [Source: Mutembesa et al. 2018]
</div>

## Data science and machine learning

Finally, there were a number of papers that used available data to ask interesting questions. One of the studies looked at the Indian census to analyze development of districts over the past ten years, leading to questions on progress of different kinds of infrastructure and geographical clustering in economic development. There was also work on building models to help people make better decisions. As a call to action, one of the papers listed [potential problems](https://arxiv.org/abs/1810.11383) where machine learning can be used for societal impact, based on interviews with stakeholders in East Africa. It was also good to see discussions on the ethics of using machine learning in societally critical domains. For instance, one [study](https://dssg.uchicago.edu/project/proactive-outreach-to-reduce-harassment-of-nyc-rental-housing-tenants/) developed a machine learning model to predict which buildings in New York are more likely to have tenants vulnerable to forceful eviction and guide city officials to visit those buildings. One of the concerns acknowledged by the authors was fairness in the selection of buildings for such visits, since the training data excluded any buildings that were not visited in the past. Questions of fairness, explainability and ethics also came up during the panel discussion on AI in Global Health.

## Deployment experiences and challenges

All said and done, the real impact of the above research projects is when they are deployed. And as people working in global development know well, translation from research to practice can be very tricky. That's why it was heartening to see work on deployment experiences being presented as full papers in the main conference. My favorite was on the [large-scale deployment of electricity sensors](https://noahklugman.com/papers/hardware_compass2019.pdf) in Ghana for providing citizens accurate data on where and how often power cuts occur. The authors faced many challenges from scaling up a small pilot to large-scale deployment, especially in incorporating local knowledge in their design (and grappling with laws around individual registration of SIM cards). Qualitative studies on deployed systems for social good also highlighted many of the challenges that go unseen when designing these systems. One paper highlighted the [difficulties that refugees face](http://www.nixdell.com/papers/2019-refugee-COMPASS.pdf) due to the identity systems used by UNHCR that did not consider refugees themselves as participative agents for the system, and another highlighted the difficulties that an internet-based monitoring system created for home health aides in the United States.

## Summary

There were many more interesting projects especially at the poster
session. It also helped that this year the conference was held in Accra, Ghana,
keeping in with the inclusive nature of the conference (last year COMPASS was in the
US). It was exciting to meet researchers from different African universities
and see the work that they are doing. I hope that there are many more such
conferences that provide opportunities for students in different parts of the
world to engage with the latest research. Closer home, MSR India continues to
contribute to this research direction; we presented four papers and a couple of posters this year. [Rahul Panicker](https://in.linkedin.com/in/rahulap) from Wadhwani AI in India gave an exciting talk on AI applications in enhancing global health delivery systems, and it was great to
see research from [Aaditeshwar Seth](http://www.cse.iitd.ernet.in/~aseth/) on agricultural pricing and district development models.

If you would like to know more details, you can find the talks here: [Day 1](https://www.youtube.com/watch?v=46gIqhB24KU), [Day 2](https://www.youtube.com/watch?v=hzjqvB97B8k), [Day 3](https://www.youtube.com/watch?v=6IuBX3CJn9o). The full list of papers is available [here](https://acmcompass.org/accepted-papers) and the proceedings should be online soon.
