# Kubernetes https://kubernetes.io/

https://github.com/kubernetes/kubernetes
 an open-source container orchestration system for automating software deployment, scaling, and management.[5][6] Google originally designed Kubernetes, but the Cloud Native Computing Foundation now maintains the project.

Kubernetes works with Docker, Containerd, and CRI-O.[7] Originally, it interfaced exclusively with the Docker runtime[8] through a "Dockershim"; however, since 2016, Kubernetes has deprecated the shim in favor of directly interfacing with the container through Containerd, or replacing Docker with a runtime that is compliant with the Container Runtime Interface (CRI).[9][10][11]

Amazon, Google, IBM, Microsoft, Oracle, Red Hat and VMware offer Kubernetes-based platforms or infrastructure as a services (IaaS) that deploy Kubernetes.[12][13]


[](#awesome-kubernetes)Awesome-Kubernetes
=========================================

[![Awesome](https://camo.githubusercontent.com/abb97269de2982c379cbc128bba93ba724d8822bfbe082737772bd4feb59cb54/68747470733a2f2f63646e2e7261776769742e636f6d2f73696e647265736f726875732f617765736f6d652f643733303566333864323966656437386661383536353265336136336531353464643865383832392f6d656469612f62616467652e737667)](https://github.com/sindresorhus/awesome) [![Links validator](https://github.com/ramitsurana/awesome-kubernetes/actions/workflows/links.yaml/badge.svg)](https://github.com/ramitsurana/awesome-kubernetes/actions/workflows/links.yaml) [![Python application](https://github.com/ramitsurana/awesome-kubernetes/actions/workflows/main.yml/badge.svg)](https://github.com/ramitsurana/awesome-kubernetes/actions/workflows/main.yml) [![Slack Widget](https://camo.githubusercontent.com/cb406a539893edb165893064201260cafe2932901c7c2d6e097a02545430efc6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f536c61636b2d4368616e6e656c2d626c75652e7376673f7374796c653d666c61742d737175617265)](https://kubernetes.slack.com/messages/awesome-kubernetes) [![Documentation Status](https://camo.githubusercontent.com/1aabd4758a08d595a1179070bf41fe00459f2ab8f5810697b52794934c76c17b/68747470733a2f2f72656164746865646f63732e6f72672f70726f6a656374732f617765736f6d652d6b756265726e657465732d62792d72616d6974737572616e612f62616467652f3f76657273696f6e3d6c6174657374)](https://awesome-kubernetes-by-ramitsurana.readthedocs.io/en/latest/?badge=latest) [![Binder](https://camo.githubusercontent.com/581c077bdbc6ca6899c86d0acc6145ae85e9d80e6f805a1071793dbe48917982/68747470733a2f2f6d7962696e6465722e6f72672f62616467655f6c6f676f2e737667)](https://mybinder.org/v2/gh/ramitsurana/awesome-kubernetes/master)

A curated list for awesome kubernetes sources inspired by [@sindresorhus' awesome](https://github.com/sindresorhus/awesome)

[![final-k8s](https://cloud.githubusercontent.com/assets/8342133/26794201/62c1a006-4a3e-11e7-8bf9-4449814648f2.png)](https://cloud.githubusercontent.com/assets/8342133/26794201/62c1a006-4a3e-11e7-8bf9-4449814648f2.png)

> "Talent wins games, but teamwork and intelligence wins championships."
> 
> \-- Michael Jordan

Without the help from these [amazing contributors](https://github.com/ramitsurana/awesome-kubernetes/graphs/contributors), building this awesome-repo would never has been possible. Thank You very much everyone !!

**Thanks to Gitbook.This awesome list can now be downloaded and read in the form of a book. Check it out --> [https://ramitsurana.gitbook.io/awesome-kubernetes/docs](https://ramitsurana.gitbook.io/awesome-kubernetes/docs) .Keep Learning Keep Sharing !!**

**If you see a package or project here that is no longer maintained or is not a good fit, please submit a pull request to improve this file. Thank you!**

[](#what-is-kubernetes)What is Kubernetes?
------------------------------------------

> Kubernetes is an open-source system for automating deployment, scaling, and management of containerized applications. It groups containers that make up an application into logical units for easy management and discovery.

_Source:_ [What is Kubernetes](http://kubernetes.io/)

[](#history)History
-------------------

**Kubernetes is known to be a descendant of Google's system BORG**

> The first unified container-management system developed at Google was the system we internally call Borg. It was built to manage both long-running services and batch jobs, which had previously been handled by two separate systems: Babysitter and the Global Work Queue. The latter???s architecture strongly influenced Borg, but was focused on batch jobs; both predated Linux control groups.

_Source:_ [Kubernetes Past](http://research.google.com/pubs/archive/44843.pdf)

[](#date-of-birth)Date of Birth
-------------------------------

Kubernetes celebrates its birthday every year on 21st July. Kubernetes 1.0 was released on July 21 2015, after being first announced to the public at Dockercon in June 2014.

[](#roadmap)Roadmap
-------------------

The awesome-kubernetes will now soon be available in the form of different releases and package bundles, It means that you can download the awesome kubernetes release up to a certain period of time, The release for awesome kubernetes 2015 bundle is released. Checkout the releases column for more info.

[](#featured-on)Featured On
---------------------------

*   [Google Cloud](https://cloud.google.com/community/)
*   [freeCodeCamp](https://www.freecodecamp.org/news/a-friendly-introduction-to-kubernetes-670c50ce4542/)

* * *

[](#starting-point)Starting Point
=================================

_A place that marks the beginning of a journey_

*   [Kubernetes Community Overview and Contributions Guide](https://docs.google.com/presentation/d/1JqcALpsg07eH665ZXQrIvOcin6SzzsIUjMRRVivrZMg/edit?usp=sharing) by [Ihor Dvoretskyi](https://twitter.com/idvoretskyi/)
*   [Are you Ready to Manage your Infrastructure like Google?](http://blog.jetstack.io/blog/k8s-getting-started-part1/)
*   [Google is years ahead when it comes to the cloud, but it's happy the world is catching up](http://www.businessinsider.in/Google-is-years-ahead-when-it-comes-to-the-cloud-but-its-happy-the-world-is-catching-up/articleshow/47793327.cms)
*   [An Intro to Google???s Kubernetes and How to Use It](http://www.ctl.io/developers/blog/post/what-is-kubernetes-and-how-to-use-it/) by [Laura Frank](https://twitter.com/rhein_wein)
*   [Kubernetes: The Future of Cloud Hosting](https://github.com/meteorhacks/meteorhacks.github.io/blob/master/_posts/2015-04-22-learn-kubernetes-the-future-of-the-cloud.md) by [Meteorhacks](https://twitter.com/meteorhacks)
*   [Kubernetes by Google](http://thevirtualizationguy.wordpress.com/tag/kubernetes/) by [Gaston Pantana](https://twitter.com/GastonPantana)
*   [Key Concepts](http://blog.arungupta.me/key-concepts-kubernetes/) by [Arun Gupta](https://twitter.com/arungupta)
*   [Application Containers: Kubernetes and Docker from Scratch](https://keithtenzer.com/containers/application-containers-kubernetes-and-docker-from-scratch/) by [Keith Tenzer](https://twitter.com/keithtenzer)
*   [Learn the Kubernetes Key Concepts in 10 Minutes](http://omerio.com/2015/12/18/learn-the-kubernetes-key-concepts-in-10-minutes/) by [Omer Dawelbeit](https://twitter.com/omerio)
*   [The Children's Illustrated Guide to Kubernetes](https://kubernetes.io/blog/2016/06/illustrated-childrens-guide-to-kubernetes/) by [Deis](https://github.com/deis)
*   [The ???kubectl run??? command](http://medium.com/@mhausenblas/the-kubectl-run-command-27c68de5cb76#.mlwi5an7o) by [Michael Hausenblas](https://twitter.com/mhausenblas)
*   [Docker Kubernetes Lab Handbook](https://github.com/xiaopeng163/docker-k8s-lab) by [Peng Xiao](https://twitter.com/xiaopeng163)
*   [Curated Resources for Kubernetes](https://hackr.io/tutorials/learn-kubernetes)
*   [Kubernetes Comic](https://cloud.google.com/kubernetes-engine/kubernetes-comic/) by [Google Cloud Platform](https://cloud.google.com/)
*   [Kubernetes 101: Pods, Nodes, Containers, and Clusters](https://medium.com/google-cloud/kubernetes-101-pods-nodes-containers-and-clusters-c1509e409e16) by [Dan Sanche](https://medium.com/@sanche)
*   [An Introduction to Kubernetes](http://www.digitalocean.com/community/tutorials/an-introduction-to-kubernetes) by [Justin Ellingwood](https://twitter.com/jmellingwood)
*   [Kubernetes and everything else - Introduction to Kubernetes and it's context](https://rinormaloku.com/introduction-application-architecture/) by [Rinor Maloku](https://twitter.com/rinormaloku)
*   [Installation on Centos 7](http://severalnines.com/blog/installing-kubernetes-cluster-minions-centos7-manage-pods-services)
*   [Setting Up a Kubernetes Cluster on Ubuntu 18.04](https://mherman.org/blog/2018/08/20/setting-up-a-kubernetes-cluster-on-ubuntu/)
*   [Cloud Native Landscape](https://landscape.cncf.io/)
*   [The Kubernetes Handbook](https://www.freecodecamp.org/news/the-kubernetes-handbook/) by [Farhan Hasin Chowdhury](https://twitter.com/frhnhsin)
*   [Bootstrapping Microservices](https://www.manning.com/books/bootstrapping-microservices-with-docker-kubernetes-and-terraform) by [Ashley Davis](https://twitter.com/ashleydavis75)
*   [Kubernetes Native Microservices with Quarkus, and MicroProfile](https://www.manning.com/books/kubernetes-native-microservices-with-quarkus-and-microprofile) by [John Clingan](https://twitter.com/jclingan) and [Ken Finnigan](https://twitter.com/kenfinnigan)
*   [How to Deploy a REST API in Kubernetes](https://www.loginradius.com/blog/async/rest-api-kubernetes/)
*   [Securing Kubernetes Secrets](https://www.manning.com/books/securing-kubernetes-secrets) by [Alex Soto Bueno](https://github.com/lordofthejars) and [Andrew Block](https://github.com/sabre1041)
*   [Kubeflow in Action](https://www.manning.com/books/kubeflow-in-action) by [Juana Nakfour](https://twitter.com/nak4red) and Sanjay Arora
*   [Kubernetes on Windows](https://www.manning.com/books/kubernetes-on-windows) by [Jay Vyas](https://twitter.com/jayunit100) and James Sturtevant
*   [Kubernetes explained](https://blog.brainboard.co/kubernetes-explained)

[](#contributing)Contributing
=============================

Contributions are most welcome!

This list is just getting started, please contribute to make it super awesome.

Check out the [Contributing Guidelines](https://github.com/ramitsurana/awesome-kubernetes/blob/master/docs/guidelines/CONTRIBUTING.md).

[](#license)License
===================

[![Creative Commons License](https://camo.githubusercontent.com/11b9a412da4f93e847989b8255d8b77d92aecf51741005da3e6e3b8c2b79b219/68747470733a2f2f692e6372656174697665636f6d6d6f6e732e6f72672f6c2f62792d6e632f342e302f38387833312e706e67)](http://creativecommons.org/licenses/)  
awesome-kubernetes by [Ramit Surana](http://www.linkedin.com/in/ramitsurana) is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/).