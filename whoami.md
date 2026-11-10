---
layout: page
title: About
heading: Marius Eriksen
permalink: /whoami/
draft: true
---

I consider myself a generalist: I have spent a career enthralled first and foremost with *computing* — distributed systems, programming languages, programming concurrent systems, algorithms, machine learning, embedded systems — resisting specialization, but going deeply into one area after another. It’s just so much *fun*. I find most satisfaction in work that lets me “see the whole stack”, and to cut through Gordian knots. Nothing has been more thrilling than the instances where my work in computing has made contact with people’s lived reality: using machine learning to reduce my daughter’s disease burden, and to help people detect cancers early.

I strongly believe that any problem at the frontier — whether of scale, knowledge, novelty, or application of technology — will be fun and interesting. I have found that what matters most is the people I work with: throughout my career I have been fortunate to have colleagues who have enriched my work and experience more than they can imagine.

## My timeline so far

<div class="timeline">
  <div class="tl-row"><span class="tl-years">2000–2004</span><div><span class="tl-place">CITI, University of Michigan</span><span class="tl-what">NFSv4, computer security.</span></div></div>
  <div class="tl-row"><span class="tl-years">2001–2004</span><div><span class="tl-place">OpenBSD</span><span class="tl-what">File systems, NFS, X11 window manager, networking.</span></div></div>
  <div class="tl-row"><span class="tl-years">2004–2008</span><div><span class="tl-place">Google</span><span class="tl-what">Fast web protocols, caching, differential compression, elastic job management.</span></div></div>
  <div class="tl-row"><span class="tl-years">2008–2009</span><div><span class="tl-place">Mixerlabs</span><span class="tl-what">Geolocation, database-as-a-service, query languages.</span></div></div>
  <div class="tl-row"><span class="tl-years">2009–2016</span><div><span class="tl-place">Twitter</span><span class="tl-what">Geolocation, scaling, site reliability, RPC systems, orchestration services, application APIs and composition, source control, engineering direction, programming languages, developer tools.</span></div></div>
  <div class="tl-row"><span class="tl-years">2016–2019</span><div><span class="tl-place">GRAIL</span><span class="tl-what">Large-scale data processing, bioinformatics pipelines, ML for cancer detection, programming languages, developer tools.</span></div></div>
  <div class="tl-row"><span class="tl-years">2020–</span><div><span class="tl-place">Facebook/Meta</span><span class="tl-what">Global service and capacity placement, capacity management, service management platform, model serving (inference) systems, linear optimization, large-scale distributed training systems, agent orchestration infrastructure, cloud systems, control plane infrastructure.</span></div></div>
</div>

## Work that’s stuck, and stuck with me

* Built [**cwm**](https://en.wikipedia.org/wiki/Cwm_(window_manager)), now the default window manager for OpenBSD.
* At Google, I led [**Google Web Accelerator**](https://en.wikipedia.org/wiki/Google_Web_Accelerator), whose ideas survived in SPDY and HTTP/2.
* Co-designed and implemented [**Finagle**](https://github.com/twitter/finagle), Twitter’s RPC system. Co-designed and implemented most of the low-level [concurrent](https://monkey.org/~marius/futures-arent-ersatz-threads.html) [programming](https://queue.acm.org/detail.cfm?id=3001119) libraries still in use today. “[Your Server as a Function](https://monkey.org/~marius/funsrv.pdf)” captures many of these ideas, and became the basis for server programming elsewhere: wangle/folly (Facebook’s core server libraries), [tokio](https://www.reddit.com/r/rust/comments/4vzomj/announcing_tokio_a_finagle_inspired_network/) (concurrent programming for Rust).
* Continued to push the envelope for RPC systems ([**RPC Redux**](https://monkey.org/~marius/redux.html)), including distributed debugging, and delegated naming. Many of these ideas (and their implementations in Finagle) became the technological base of modern service meshes (through [Linkerd](https://linkerd.io/2017/01/24/linkerd-joins-the-cloud-native-computing-foundation/)).
* Co-designed and implemented Twitter’s [**Strato**](https://www.thestrangeloop.com/2018/leverage-vs-autonomy-in-a-large-software-system.html), a *system for composing systems* into a single virtual database through which new product features are defined. We built distributed database technologies, a custom language, and deep integration into the Twitter stack. It is now the primary way products interface with Twitter’s infrastructure.
* When my daughter was diagnosed with **Type 1 Diabetes**, I immediately saw how technology could help ease the burden of this chronic disease. I [reverse engineered the RF protocol](https://github.com/mariusae/pingrf) for the Animas insulin pump and built custom hardware to communicate with it. I then built a closed-loop model-predictive-control system that used her blood glucose and carbohydrate input histories in order to determine an insulin dosage schedule every 5 minutes. The model was trained on a few months’ worth of data. Details in this [TensorFlow Meets](https://www.youtube.com/watch?v=WlPP4MJhQkI&list=PLQY2H8rRoyvyOeER8UNF-1zXaCKGLZVog&index=3) interview with Pete Warden. (Embedded ML for health!) My daughter used this system 24/7 for 5 years before similar commercial systems became available.
* Designed and implemented [**Reflow**](https://github.com/grailbio/reflow), a programming language to implement coarse-grained data pipelines. Its distributed orchestration runtime transparently enables full *parallelism and incrementalism*. Reflow also *fully embraced cloud computing* by being “[self-managed](https://medium.com/grail-eng/self-managing-serverless-computing-with-bigmachine-e75bd412ef5a)”. You simply invoke reflow with appropriate cloud credentials, and it self-manages all the underlying resources (compute, storage, caches, etc.). Reflow is the basis of all bioinformatics pipelines at GRAIL.
* Designed and implemented [**Bigslice**](https://medium.com/grail-eng/bigslice-a-cluster-computing-system-for-go-7e03acd2419b), a large-scale, high-performance data processing system with a simple programming model. We used this system for most of our data processing at GRAIL.
* With colleagues, [developed a **cancer classification model using patch CNNs**](https://patentimages.storage.googleapis.com/c2/fd/66/ece941341366f6/US20210327534A1.pdf). Without biological priors, we were able to develop a high-performance classifier based entirely on the genomic data, based on ML techniques from astronomy.
* With many colleagues, designed and developed **Flux: a global capacity management system** for Meta ([OSDI paper](https://www.usenix.org/system/files/osdi23-eriksen.pdf)). Flux enabled us to jointly optimize service and capacity placement, providing a truly global (i.e., region-less) service model.
* Co-designed and implemented [**IPnext**](https://atscaleconference.com/ipnext-metas-next-generation-inference-platform/), Meta’s inference serving platform, used to serve all recommender systems (timeline, ads, etc.) as well as content understanding models at Meta.
* Co-designed and implemented Meta’s **Control Plane Platform**. This system provides a high-level control plane programming model supporting a simple developer experience, efficient incremental updates, large scale, and high legibility. It is now used across a wide variety of core control planes at Meta, and is the standard for building new control planes at Meta.
* Co-designed and implemented [**PyTorch Monarch**](https://pytorch.org/blog/introducing-pytorch-monarch/), a single-controller distributed orchestration system for PyTorch. It is now used both for training applications (most heavily in RL/post-training) and also for large-scale agent orchestration (e.g., RSI applications).
* I genuinely enjoy **technical writing**. Nothing forces clarity of thinking quite like putting words down on the page. Some of my writing has made it into the canon: “[Your Server as a Function](https://monkey.org/~marius/funsrv.pdf),” “[Futures Aren’t Ersatz Threads](https://monkey.org/~marius/futures-arent-ersatz-threads.html),” “[Hints for Writing Unix Tools](https://monkey.org/~marius/unix-tools-hints.html).”
{: .work}

## Elsewhere

[marius@monkey.org](mailto:marius@monkey.org) · [monkey.org/~marius](https://monkey.org/~marius) · [GitHub](https://github.com/mariusae) · [Threads](https://www.threads.com/@mariusae) · [X](https://x.com/marius)
