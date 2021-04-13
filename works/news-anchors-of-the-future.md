---
title: News Anchors of the Future
date: 2020-03-01
image: /img/news_01_small.gif
ref:
  supervision: Dipl.-Künstler Max Neupert
  institution: Bauhaus-Universität Weimar
  year: 2020
---

<iframe src="https://player.vimeo.com/video/404982095?title=0&byline=0&portrait=0" width="640" height="640" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

In the 1980s, British [Channel 4](https://www.channel4.com/) tried to imagine the TV of the future. They created Max Headroom as the host of a music show. He was supposed to be an AI character although played by an actual human actor, [Matt Frewer](http://en.wikipedia.org/wiki/Matt_Frewer). After shooting, the fragments were cut in a way that would be called “[glitchy](https://www.pbs.org/video/off-book-art-glitch)” nowadays. This imperfection is a very important part of the character, serving as a signifier for an artificial humanoid character.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/vS17G1MXzLk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

When so called neural networks came up, a discussion started about which kinds of labour can be done by so called artificial intelligence. Some people are convinced even artists and musicians will be replaced by computer systems. [Hatsune Miku](http://en.wikipedia.org/wiki/Hatsune_Miku) was originally the name voicebank which can be used with Yamaha’s Vocaloid software. From 2010 on, albums for Hatsune Miku have been produced. In 2012 “she” gave her first concert as a holograph, gaining huge popularity.

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/YSyWtESoeOc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Max Headroom and Hatsune Miku are popular examples for avatars, fictional characters with a virtual representation created through CGI and video cutting techniques. With this history in mind, how would avatars for TV news look like? Having trained a machine learning model with news host images, the software can generate new news hosts. Most approaches aim at generating a photorealistic representation of a human. Referring to Max Headroom, it is more interesting to create avatars looking human-like, having some flaws, and thus, to include technical characteristics in the design process.

First tests were carried out with the [few-show-vid2vid](https://github.com/NVlabs/few-shot-vid2vid) framework by NVIDIA. At this time, the idea was different: The news host were supposed to have dog faces. Due to technical problems this approach was abandoned for now.

![Dog anchor.](/img/news_01.gif)

[RunwayML](https://runwayml.com/) is a SaaS company providing shared machine learning models. For this experiment, the StyleGAN (to be more precise [StyleGAN2](https://github.com/NVlabs/stylegan2)) framework by NVIDIA was used, which gained popularity due to its ability of generating almost photorealistic faces. The model was trained with the [FaceForensics](http://niessnerlab.org/projects/roessler2018faceforensics.html) dataset by Technische Universität München, consisting of videos of news hosts. Using [ffmpeg](http://ffmpeg.org/) a part of these video files were converted to image sequences and fed into RunwayML’s training system. After completing the training, a video was generated walking through different parameters for image generation, creating this fluid transition from one host to another. This training was completed after 2000 steps. The model can be expanded and the quality improved by continuing the training.

![RunwayML](/img/news_02.png)

* [NFT @ Hic et Nunc: News Anchors of the Future #01](https://www.hicetnunc.xyz/objkt/30392)
* [NFT @ Hic et Nunc: News Anchors of the Future #02](https://www.hicetnunc.xyz/objkt/31411)