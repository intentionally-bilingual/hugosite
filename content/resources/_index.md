---
title: "Resources"
---

##  Software, data and literature in the field
We are maintaining a list of interesting papers, software and data resources used for morphological profiling and biological data science in [the Awesome-Cytodata repository](https://github.com/cytodata/awesome-cytodata). Contributions via pull requests are more than welcome!

## Getting started with morphological profile analyses

Are you interested in analyzing image-based screening experiments but don't have any experience in morphological profiling and wonder where to start? Here are some suggestions:
  - Learn what the basic steps of morphological profiling are
  - Learn what morphological profiling can be used for
  - Identify what are your needs, interests and what tools are available
  - Get your hands dirty and try running an analysis pipeline
  - Get help when needed and stay up to date

### Learn what the basic steps are

Review articles offer all the keys to understand what is at stake and what are the challenges of morphological profing while adopting different perspectives. In particular, [Bougen-Zhukov et al.](https://doi.org/10.1002/cyto.a.22909) describe extensively the terminology used in the field while [Caicedo et al.](https://doi.org/10.1038/nmeth.4397) cover its technical challenges and provide guidelines for all analytical steps, assembled at the creation of the CytoData society. [An image-based profiling handbook](https://cytomining.github.io/profiling-handbook/) describes a full profiling pipeline with AWS cloud computing, including morphological measurements with [CellProfiler](https://cellprofiler.org/) and feature processing with cytominer (with implementations in [R](https://github.com/cytomining/cytominer) and [Python](https://github.com/cytomining/pycytominer), whereas [BioProfiling.jl](https://github.com/menchelab/BioProfiling.jl) is an alternative in Julia). Depending on your background and interests, you might also look for research articles covering specific aspects of the topic, for instance [Rohban et al.](http://doi.org/10.1038/s41467-019-10154-8) nicely define what morphological features are and can be from a statistical point of view. If you are interested in machine-learning approaches, reviews by [Scheeder et al.](https://doi.org/10.1016/J.COISB.2018.05.004) and [Chandrasekaran et al.](https://doi.org/10.1038/s41573-020-00117-w) specifically adress this topic. 

### Learn what morphological profiling can be used for

The fields of high-content screening and morphological profiling already led to several successes in adressing complex biological questions. You can find some of the milestone papers in the field in [the Awesome-Cytodata repository](https://github.com/cytodata/awesome-cytodata), which covers applications ranging from industrial drug development and repurposing to basic research in systems biology studies. Having a glance at the articles you find interesting and their method sections will help you get a sense of what can be done.

### Identify what are your needs and interests

Based on what you learnt so far, you can start to decide on the tools and approaches that are relevant to your work and prioritize the ones you should get familiar with. This will be refined as you start conducting your own analysis and as you meet new challenges, inherent to the biological questions you are adressing and the technical characteristics of your imaging setup. 

### Try out an analysis pipeline yourself

The best way to learn is often through practice. If you identified a paper involving morphological profiling that you like, you could try reproducing the analysis yourself or adapting it to your own data. Overall, observing existing complete profiling pipelines (e.g. with [CellProfiler](https://cellprofiler.org/examples) or with a [simple example from the CytoData Hackathon 2019](https://github.com/cytodata/single-cell-classifier)) will expose you to to all the steps involved in such pipelines and make you think why each of them is needed and understand the sequential nature of processing and analysing imaging data. You might then decide if such a tool is suitable for you or if you would rather look at alternatives for one or several of these steps (e.g. dedicated deep-learning based segmentation methods are available, including pretrained models such as [CellPose](https://github.com/MouseLand/cellpose) and [DeepCell](https://github.com/vanvalenlab/intro-to-deepcell)).


### Get help when needed and stay up to date

Even if no one in your local research community can guide you, you can easily connect with the imaging and profiling community at large. The CytoData society is partnering with the [image.sc forum](https://forum.image.sc/), where experts regularly answer questions about scientific imaging and image analysis and the dedicated open source software. The yearly CytoData conferences and hackathons are also great opportunities to engage with the community and learn about the latest developments in the field. Finally, the society regularly organises tutorials and discussions available on [our YouTube channel](https://www.youtube.com/channel/UCdzwWEyM0OVOpuX_0Ci_DuQ). 

### Disclaimer 

This list is based on our personal experience analyzing high-content imaging data and introducing biomedical researchers to the topic and is therefore highly subjective and incomplete. There are many other good resources out there (some of them can be found in [the Awesome-Cytodata repository](https://github.com/cytodata/awesome-cytodata)) and other approaches might be better suited for you but we hope this general guideline can be useful for beginners.
