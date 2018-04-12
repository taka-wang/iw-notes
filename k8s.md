# Kubernetes

- [Reasons Kubernetes is cool](https://jvns.ca/blog/2017/10/05/reasons-kubernetes-is-cool/)

- [Kubernetes Architecture](https://github.com/kubernetes/kubernetes/blob/release-1.2/docs/design/architecture.md)


## Key ideas

- IP-per-pod-model
- pods be able to communicate with other pods whether they are running on the same local host or separate hosts.
- Every **node** is assigned a **unique CIDR block** (a range of IP addresses) for pod IPs

## Terminology

- Control Plane
	- API server (kube-apiserver)
	- Controller manager (kube-controller-manager)
	- Scheduler (kube-scheduler)
		- [How does the Kubernetes scheduler work?](https://jvns.ca/blog/2017/07/27/how-does-the-kubernetes-scheduler-work/)
	- etcd
		- [Raft 為什麼是更易理解的分佈式一致性算法](https://read01.com/jjJREo.html)
		- [分散式一致性演算法：Raft 演算法（論文翻譯）](http://www.how01.com/post_66eX1vlzDO9AY.html)

- kubeadm
	- [How kubeadm Initializes Your Kubernetes Master](https://www.ianlewis.org/en/how-kubeadm-initializes-your-kubernetes-master)
	- `kubeadm init`
		- created the necessary certificates for the API
		- started the control plane components
		- installed the essential addons.
			- kube-discovery
			- kube-proxy
			- kube-dns
	- [Limitations](https://kubernetes.io/docs/setup/independent/create-cluster-kubeadm/#limitations)
- Pod - group of one or more containers running on a node (machine)
	- Pod are containers，有精美的 Pod 概念圖 -> [What are Kubernetes Pods Anyway?](https://www.ianlewis.org/en/what-are-kubernetes-pods-anyway) :thumbsup:

	- [The Almighty Pause Container](https://www.ianlewis.org/en/almighty-pause-container) 解釋 pause container 的概念
	  - serve as parent container
	  - serve as the basis of linux namespace
	  - serve as PID 1 to reaps zombie processes
	還有 PID namespace sharing 與 Reaping Zombies 的關係

- node - a server inside of a Kubernetes cluster
- cluster - a group of servers (node) managed by Kubernetes
- master - the server that runs Kubernetes and manages other servers
- worker - servers managed by the master server
- deployment - settings for deploying pods to cluster (Replication Controller)
- service - settings for accessing pods **within** cluster
- ingress - settings for accessing pods from the Internet
- pod networks
- service networks
- cluster IPs
- container ports
- host ports
- node ports
- CNI
	- [Choosing a CNI provider](https://chrislovecnm.com/kubernetes/cni/choosing-a-cni-provider/)
	- [Getting the Flannel host-gw working with Kubernetes](https://prefetch.net/blog/2018/02/20/getting-the-flannel-host-gw-working-with-kubernetes/)

- 名詞解釋與完整圖 -> [The Kubernetes Way: Pod, Controller, Label and More](https://www.stratoscale.com/blog/kubernetes/kubernetes-way-pod-controller-label/)

---

## Learning Resources

- [The Children's Illustrated Guide to Kubernetes](https://deis.com/blog/2016/kubernetes-illustrated-guide/)

- [Kubernetes Beginner's Guide: Learning the basics in an hour](https://www.weave.works/blog/kubernetes-beginners-guide/)

- [Kuberbetes學習筆記](https://www.gitbook.com/book/gcpug-tw/kuberbetes-in-action/details)

- [Udacity - Scalable Microservices with Kubernetes by Google](https://www.udacity.com/course/scalable-microservices-with-kubernetes--ud615)

- [Edx - Introduction to Kubernetes](https://www.edx.org/course/introduction-to-kubernetes)

- [Kelsey Hightower - Managing Containers at Scale with CoreOS and Kubernetes](https://www.youtube.com/watch?v=pozC9rBvAIs)

- [Intro to Kubernetes, setting up your first app and why it’s just like snowboarding](https://codefresh.io/docker-tutorial/kubernetes-snowboarding-everything-intro-kubernetes/)

- [From Monolith to Microservice Architecture on Kubernetes, part 1 — The Api Gateway](https://medium.com/jeroen-rosenberg/from-monolith-to-microservice-architecture-on-kubernetes-part-1-the-api-gateway-eb82f8c2d10c)

- [Introduction to YAML: Creating a Kubernetes deployment](https://www.mirantis.com/blog/introduction-to-yaml-creating-a-kubernetes-deployment/)

---

## Networks

- 圖解 k8s 的網路，很精美的圖解 -> [An illustrated guide to Kubernetes Networking [Part 1]](https://medium.com/@ApsOps/an-illustrated-guide-to-kubernetes-networking-part-1-d1ede3322727) :thumbsup:

- 一系列的文章解釋Pod Network, Service 與 ingress，雖然圖解不是很精確 [Understanding kubernetes networking: pods](https://medium.com/google-cloud/understanding-kubernetes-networking-pods-7117dd28727)  :thumbsup:

- 用簡單的方式解釋 overlay network -> [A container networking overview](https://jvns.ca/blog/2016/12/22/container-networking/) :thumbsup:

- 官方文件 -> [Cluster Networking](https://kubernetes.io/docs/concepts/cluster-administration/networking/)

- [Kubernetes Overview, Part One](https://deis.com/blog/2016/kubernetes-overview-pt-1/)

- [What makes a container cluster](https://cloudplatform.googleblog.com/2015/01/what-makes-a-container-cluster.html?m=1)


---

## Docker Networking

- [What is the relation between docker0 and eth0?](https://stackoverflow.com/questions/37536687/what-is-the-relation-between-docker0-and-eth0)

- [Networking your docker containers using docker0 bridge](https://developer.ibm.com/recipes/tutorials/networking-your-docker-containers-using-docker0-bridge/)

- [探索 Docker bridge 的正確姿勢](http://blog.daocloud.io/docker-bridge/)

- [Four ways to connect a docker container to a local network](http://blog.oddbit.com/2014/08/11/four-ways-to-connect-a-docker/)

- [What is Docker networking?](https://www.oreilly.com/learning/what-is-docker-networking#example-bridge-mode-networking)

- [Networking for Docker Containers (a Primer) Part I](https://mesosphere.com/blog/networking-docker-containers/)

---

## Traefik

- [Multi HTTPS sub domain with Traefik and Docker - Part 1](https://blog.ptrk.io/multi-https-sub-domain-with-traefik-and-docker/)

- [Using Drone and Traefik on Kubernetes to deploy a basic application](https://blog.ptrk.io/using-drone-on-kubernetes-to-deploy-a-basic-application/)

- [How to Use Traefik as a Reverse Proxy for Docker Containers on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-use-traefik-as-a-reverse-proxy-for-docker-containers-on-ubuntu-16-04)

## Monitoring

- [Monitoring in the Kubernetes era](https://github.com/DataDog/the-monitor/blob/master/kubernetes/monitoring-in-the-kubernetes-era.md)

### CI/CD

- [Set Up a Drone CI/CD Pipeline with Kubernetes](https://akomljen.com/set-up-a-drone-ci-cd-pipeline-with-kubernetes/)

- [Using CircleCI and Kubernetes to achieve seamless deployments to Google Container Engine](https://medium.com/google-cloud/using-circleci-and-kubernetes-to-achieve-seamless-deployments-to-google-container-engine-8b26abc04846)

## Setup

- [Bootstrap Kubernetes **the hard way** on Google Cloud Platform. No scripts.](https://github.com/kelseyhightower/kubernetes-the-hard-way)

- [Creating a Kubernetes Cluster from Scratch with Kubeadm](https://zihao.me/post/creating-a-kubernetes-cluster-from-scratch-with-kubeadm/)

- [Installing a DIY bare metal GPU cluster for Kubernetes](https://insights.ubuntu.com/2017/01/30/installing-a-diy-bare-metal-gpu-cluster-for-kubernetes)

## Others

- [Using Existing Ceph Cluster for Kubernetes Persistent Storage](https://akomljen.com/using-existing-ceph-cluster-for-kubernetes-persistent-storage/) :thumbsup:

## Experiences

- [One year using Kubernetes in production: Lessons learned](https://techbeacon.com/one-year-using-kubernetes-production-lessons-learned)

- [Operating a Kubernetes network](https://jvns.ca/blog/2017/10/10/operating-a-kubernetes-network/) :thumbsup:

- [Securing Kubernetes Cluster Networking](https://ahmet.im/blog/kubernetes-network-policy/)

- [MISADVENTURES WITH KUBE DNS](https://blog.sophaskins.net/blog/misadventures-with-kube-dns/)

---

## [Machine Learning on kubernetes](k8s/ml.md)

