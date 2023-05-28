# Kubernetes Failure Stories


**Misconfigurations in Kubernetes do not always constitute Kubernetes hacks. Any weakness in the Kubernetes-based applications can endanger the entire system. Several hacks and several use vcases where you think about the Kubernetes**

* https://security.snyk.io/vuln/?search=kubernetes - Larn about the present CVE that is reaised from the community in the Kubernetes
* https://www.bleepingcomputer.com/news/security/over-900-000-kubernetes-instances-found-exposed-online/
* https://n26.com/en-eu/blog/kubernetes-and-site-reliability-at-n26-an-engineering-success-story - not a roduction downtime story but you can refer to some of the changes that made a huge impact in production
* https://www.datarevenue.com/en-blog/kubeflow-not-ready-for-production
* https://www.youtube.com/watch?v=FrQ8Lwm9_j8
* https://www.youtube.com/watch?v=rjSWVeAvb24
* https://www.youtube.com/watch?v=ay7NibpRAYU
* https://www.wired.com/story/cryptojacking-tesla-amazon-cloud/
* https://threatpost.com/380k-kubernetes-api-servers-exposed-to-public-internet/179679/
* https://www.bleepingcomputer.com/news/security/jenkins-discloses-dozens-of-zero-day-bugs-in-multiple-plugins/
* https://www.crowdstrike.com/blog/cr8escape-new-vulnerability-discovered-in-cri-o-container-engine-cve-2022-0811/
* https://sysdig.com/blog/exposed-prometheus-exploit-kubernetes-kubeconeu/
* https://thehackernews.com/2022/05/yes-containers-are-terrific-but-watch.html
* https://www.trendmicro.com/vinfo/es/security/news/cybercrime-and-digital-threats/tesla-and-jenkins-servers-fall-victim-to-cryptominers
* https://thehackernews.com/2022/07/over-1200-npm-packages-found-involved.html
* https://www.microsoft.com/en-us/security/blog/2021/03/23/secure-containerized-environments-with-updated-threat-matrix-for-kubernetes/
* https://www.paloaltonetworks.com/blog/prisma-cloud/6-common-kubernetes-attacks/


**A compiled list of links to public failure stories related to Kubernetes.**

* [Make your services faster by removing CPU limits - Buffer - blog post 2020](https://erickhun.com/posts/kubernetes-faster-services-no-cpu-limits/)
    * involved: kops, CPU Limit, CPU throttling
    * impact: high latency

* [The case of the missing packet: An EKS migration tale - MindTickle - blog post 2020](https://yashmehrotra.com/post/2020-03-16-case-of-missing-packet/)
    * involved: EKS, AWS CNI Plugin,
    * impact: frequent connection failures when talking to services outside the cluster

* [How we failed to integrate Istio into our platform - Exponea - blog post 2019](https://medium.com/@jakubkulich/sailing-with-the-istio-through-the-shallow-water-8ae81668381e)
    * involved: Istio, GKE, proxy injection
    * impact: stopped Istio rollout, developers' time spent

* [How a couple of characters brought down our site - Skyscanner - blog post 2021](https://medium.com/@SkyscannerEng/how-a-couple-of-characters-brought-down-our-site-356ccaf1fbc3)
    * involved: Gitops, templating, namespace deletion
    * impact: global outage

* [Kubernetes made my latency 10x higher - Adevinta - blog post 2019](https://srvaroa.github.io/kubernetes/migration/latency/dns/java/aws/microservices/2019/10/22/kubernetes-added-a-0-to-my-latency.html)
    * involved: KIAM, DNS, AWS IAM, latency
    * impact: service showing up to x10 higher latencies compared to a deployment in EC2

* [Kubernetes Networking Problems Due to the Conntrack - loveholidays - blog post 2020](https://deploy.live/blog/kubernetes-networking-problems-due-to-the-conntrack/)
    * involved: GKE, conntrack, HAProxy
    * impact: high error rate on network-heavy services
* [DNS issues in Kubernetes. Public postmortem #1 - Preply - blog post 2020](https://medium.com/preply-engineering/dns-postmortem-e169efd45afd)
    * involved: conntrack, DNS, CoreDNS-autoscaler
    * impact: partial production outage
* [CPU limits and aggressive throttling in Kubernetes - Omio - blog post 2020](https://medium.com/omio-engineering/cpu-limits-and-aggressive-throttling-in-kubernetes-c5b20bd8a718)
    * involved: GKE, CPU Limit, CPU throttling
    * impact: high latency, errors
* [When GKE ran out of IP addresses - loveholidays - blog post 2020](https://deploy.live/blog/when-gke-ran-out-of-ip-addresses/)
    * involved: GKE, cluster autoscaler, HPA, Alias IP VPC (VPC Native)
    * impact: stuck deployment, blocked autoscaling of both pods and nodes  

* [A Kubernetes failure story (dex) - anonymous Fullstaq client - Dutch kubernetes meetup slides 2019-06](https://pieterlange.github.io/failure-stories/2019-06.dex.html)
    * involved: etcd, apiserver, dex, custom resources
    * impact: broken control plane on production with no access to o11y due to broken authentication system, no actual business impact

* [How A Cryptocurrency Miner Made Its Way onto Our Internal Kubernetes Clusters - JW Player - Medium post March 2019](https://medium.com/jw-player-engineering/how-a-cryptocurrency-miner-made-its-way-onto-our-internal-kubernetes-clusters-9b09c4704205)
    * involved: Weave Scope, public AWS ELB
    * impact: security issue, cryptominer stealing compute power

* [Intermittent delays in Kubernetes - MindTickle - blog post 2019](https://medium.com/techmindtickle/intermittent-delays-in-kubernetes-e9de8239e2fa)  
    * involved: kops, conntrack DNAT/SNAT, libc, musl
    * impace: intermittent delays in interval of 5 seconds in DNS lookups for HTTP/1.1 and HTTP/2
* [10 Weird Ways to Blow Up Your Kubernetes - Airbnb - KubeCon NA 2019](https://www.youtube.com/watch?v=FrQ8Lwm9_j8)
    * involved: sidecars, DaemonSet, image registry, JVM, HPA
    * impact: outages
* [Did Kubernetes Make My p95s Worse? - Airbnb - KubeCon NA 2019](https://www.youtube.com/watch?v=QXApVwRBeys)
    * involved: CPU Limit, CPU Throttling, DNS
    * impact: high latency

* [A Kubernetes crime story - Prezi - blog post 2019](https://engineering.prezi.com/https-engineering-prezi-com-a-kubernetes-crime-story-2e8d75a77630)
    * involved: AWS EKS, SNAT, conntrack, Amazon VPC CNI plugin
    * impact: delay of 1-3 seconds for outgoing TCP connections

* [Postmortem: New K8s workers unable to join cluster - FREE NOW - postmortem 2019](https://github.com/freenowtech/postmortems/blob/master/2019-09-19%20-%20New%20K8s%20workers%20unable%20to%20join%20cluster.pdf)
    * involved: AWS spot instances, kops, CentOS, container-selinux
    * impact: insufficient cluster capacity in testing environments, failed deployments in production and staging environments

* [How a simple admission webhook lead to a cluster outage - Jetstack - blog post 2019](https://blog.jetstack.io/blog/gke-webhook-outage)
    * involved: ValidatingWebhookConfiguration, GKE node auto-repair
    * impact: prolonged downtime of non-prod environment, nodes lost, failed master upgrade

* [Post Mortem: Kubernetes Node OOM - Blue Matador - blog post 2019](https://www.bluematador.com/blog/post-mortem-kubernetes-node-oom)
    * involved: AWS, SystemOOM, EBS, fluentd-sumologic, no resource requests/limits
    * impact: unknown, Pods killed

* [Kubernetes’ dirty endpoint secret and Ingress - Ravelin - blog post 2019](https://philpearl.github.io/post/k8s_ingress/)
    * involved: GKE, Ingress, replication controller, SIGTERM, "graceful shutdown"
    * impact: occasional 502 errors

* [How a Production Outage Was Caused Using Kubernetes Pod Priorities - Grafana Labs 2019](https://grafana.com/blog/2019/07/24/how-a-production-outage-was-caused-using-kubernetes-pod-priorities/)
    * involved: Pod priorities
    * impact: cascading Pod evictions

* [Moving to Kubernetes: the Bad and the Ugly - Xing - ContainerDays EU 2019](https://www.youtube.com/watch?v=MoIdU0J0f0E)
    * involved: nginx Ingress, network interrupts, conntrack, frozen CronJob, PLEG, stuck controllers
    * impact: lost requests, response time jumps, not ready nodes
* [Kubernetes Failure Stories, or: How to Crash Your Cluster - Zalando - ContainerDays EU 2019](https://www.youtube.com/watch?v=LpFApeaGv7A)
    * involved: AWS IAM, Kubelet, `--kube-api-qps`, Skipper-Ingress, AWS, `OOMKill`, CronJob, CoreDNS, CPU throttling
    * impact: build errors, production outages

* [Build Errors of Continuous Delivery Platform - Zalando - postmortem 2019](https://github.com/zalando-incubator/kubernetes-on-aws/blob/dev/docs/postmortems/jun-2019-kubelet-qps.md)
    * involved: AWS IAM, Kubelet, kube2iam, `--kube-api-qps`
    * impact: build errors

* [10 Ways to Shoot Yourself in the Foot with Kubernetes, #9 Will Surprise You - Datadog - KubeCon Barcelona 2019](https://www.youtube.com/watch?v=QKI-JRs2RIE)
    * involved: CoreDNS, `ndots:5`, IPVS conntrack, `imagePullPolicy: Always`, DaemonSet, NAT instances, `latest` tag, API server `OOMKill`, kube2iam, cluster-autoscaler, PodPriority, audit logs, `spec.replicas`, AWS ASG rebalance, CronJob, Pod toleration, zombies, `readinessProbe.exec`, cgroup freeze, kubectl
    * impact: unknown, API server outage, pending pods, slow deployments

* [How Spotify Accidentally Deleted All its Kube Clusters with No User Impact - Spotify - KubeCon Barcelona 2019](https://www.youtube.com/watch?v=ix0Tw8uinWs)
    * involved: GKE, cluster deletion, browser tabs, Terraform, global state file, git PRs, GCP permissions
    * impact: no impact on end users

* [Kubernetes Failure Stories - Zalando - KubeCon Barcelona 2019](https://www.youtube.com/watch?v=6sDTB4eV4F8)
    * involved: Skipper-Ingress, AWS, `OOMKill`, high latency, CronJob, CoreDNS, `ndots:5`, etcd, CPU throttling
    * impact: multiple production outages

* [Oh Sh\*t! The Config Changed! - Pusher - KubeCon Barcelona 2019](https://www.youtube.com/watch?v=8P7-C44Gjj8)
    * involved: AWS, nginx, ConfigMap change
    * impact: production outage

* [Misunderstanding the behaviour of one templating line - Skyscanner - blog post 2019](https://medium.com/@SkyscannerEng/misunderstanding-the-behaviour-of-one-templating-line-and-the-pain-it-caused-our-k8s-clusters-a420f30a99f1)
    * involved: HAProxy-Ingress, Service VIPs, Golang templating
    * impact: Significantly increased latency, 5XXs thrown from some services



* [Maximize learnings from a Kubernetes cluster failure - NU.nl - blog post 2019](https://www.tibobeijen.nl/2019/02/01/learning-from-kubernetes-cluster-failure/)
    * involved: AWS, `NotReady` nodes, `SystemOOM`, Helm, ElastAlert, no resource limits set
    * impact: user experience affected for internally used tools and dashboards

* [Kubernetes Load Balancer Configuration - Beware when draining nodes - DevOps Hof - blog post 2019](https://www.devops-hof.de/kubernetes-load-balancer-konfiguration-beware-when-draining-nodes/)
    * involved: GCP Load Balancer, `externalTrafficPolicy`, ingress-nginx
    * impact: total ingress traffic outage

* [On Infrastructure at Scale: A Cascading Failure of Distributed Systems - Target - Medium post January 2019](https://medium.com/@daniel.p.woods/on-infrastructure-at-scale-a-cascading-failure-of-distributed-systems-7cff2a3cd2df)
    * involved: on-premise, Kafka, large cluster, Consul, Docker daemon, high CPU usage
    * impact: development environment outage

* [How NOT to do Kubernetes - Sr.SRE Medya Ghazizadeh - Google - Cloud Native Meetup Sep 2018](https://www.youtube.com/watch?v=V0DVkrHf08k)
    * involved: public container registery, ingress wild card, image size, replica count, 12factor
    * impact: security, stablity of clusters.

* [Running Kubernetes in Production: A Million Ways to Crash Your Cluster - Zalando - DevOpsCon Munich 2018](https://www.slideshare.net/try_except_/running-kubernetes-in-production-a-million-ways-to-crash-your-cluster-devopscon-munich-2018)
    * involved: AWS, Ingress, CronJob, etcd, flannel, Docker, CPU throttling
    * impact: production outages

* [Outages? Downtime? - Veracode - blog post 2018](https://sethmccombs.github.io/work/2018/12/03/Outages.html)
    * involved: AWS, AWS IAM, region migration, kubespray, Terraform, pod CIDR
    * impact: QA/dev cluster outage

* [NRE Labs Outage Post-Mortem - NRE Labs - blog post 2018](https://keepingitclassless.net/2018/12/december-4-nre-labs-outage-post-mortem/)
    * involved: GCP, kubeadm, etcd, Terraform, `livenessProbe`
    * impact: production outage

* [A Perfect DNS Storm - Toyota Connected - blog post 2018](https://www.adammargherio.com/a-perfect-dns-storm/)
    * involved: Azure, DNS, `ndots:5`, Alpine musl libc
    * impact: DNS resolution failures

* [Kubernetes and the Menace ELB, the tale of an outage - Turnitin - blog post 2018](https://itnext.io/kubernetes-and-the-menace-elb-the-tale-of-an-outage-c00bef678fc0)
    * involved: AWS, kube-aws, ELB dynamic IPs, API server, kubelet, `NotReady` nodes
    * impact: 15 minutes cluster outage

* [Moving the Entire Stack to K8s Within a Year – Lessons Learned - ThredUP - DevOpsStage 2018](https://www.youtube.com/watch?v=tA8Sr3Nsx1I)
    * involved: AWS, kops, HAProxy, `livenessProbe`, DNS, too many open files
    * impact: unknown outages, DNS errors

* [AirMap Platform Service Outage - AirMap - incident report 2018](https://www.airmap.com/incident-180719/)
    * involved: Azure, `NotReady` nodes, kubelet PLEG, CNI
    * impact: production AirMap platform outage

* [Anatomy of a Production Kubernetes Outage - Monzo - KubeCon Europe 2018](https://www.youtube.com/watch?v=OUYTNywPk-s)
    * involved: AWS, etcd, Linkerd, `NullPointerException`, gRPC client, services without endpoints, incompatible Kubernetes API change
    * impact: production ledger/platform outage

* [Stories from the Playbook - Google - KubeCon Europe 2018](https://youtu.be/N2JUGnwinbQ)
    * involved: GKE, etcd, Docker daemon, Image registry, dnsmasq vulnerabilities
    * impact: production outage

* [101 Ways to "Break and Recover" Kubernetes Cluster - Oath/Yahoo - KubeCon Europe 2018](https://www.youtube.com/watch?v=likHm-KHGWQ)
    * involved: on-premise, namespace deletion, domain name collision, `NotReady` nodes, etcd empty dir, TLS certificate refresh, DNS issues, OOM
    * impact: unknown cluster outages

* [Experiences with running PostgreSQL on Kubernetes - Gravitational - blog post 2018](https://gravitational.com/blog/running-postgresql-on-kubernetes/)
    * involved: PostgreSQL, streaming replication
    * impact: data loss

* [101 Ways to Crash Your Cluster - Nordstrom - KubeCon North America 2017](https://www.youtube.com/watch?v=xZO9nx6GBu0)
    * involved: AWS, `NotReady` nodes, OOM, eviction thresholds, ELB dynamic IPs, kubelet, cluster autoscaler, etcd split
    * impact: full production cluster outage, other outages

* [You Broke Reddit: The Pi-Day Outage - Reddit - blog post 2023](https://www.reddit.com/r/RedditEng/comments/11xx5o0/you_broke_reddit_the_piday_outage/)
    * involved: Calico CNI, Upgrades, labels 
    * impact: global outage

* [10 More Weird Ways to Blow Up Your Kubernetes - Airbnb - KubeCon NA 2020](https://www.youtube.com/watch?v=4CT0cI62YHk)
    * involved: MutatingAdmissionWebhook, CPU Limits, OOMKill, kube2iam, HPA
    * impact: outages
* [Why we switched from fluent-bit to Fluentd in 2 hours - PrometheusKube - blog post 2020](https://prometheuskube.com/why-we-switched-from-fluent-bit-to-fluentd-in-2-hours) 
    * involved: fluent-bit, missing logs, Fluentd
    * impact: lost application logs in production


* [Major Outage: Current account payments may fail - Monzo - Monzo Community post 2017](https://community.monzo.com/t/resolved-current-account-payments-may-fail-major-outage-27-10-2017/26296/95)
    * involved: AWS, etcd, Linkerd, `NullPointerException`, services without endpoints
    * impact: major production outage, full platform outage, current account payments fail

* [Fallacies of Distributed Computing with Kubernetes on AWS - Zalando - AWS User Group Hamburg October 2017](https://www.slideshare.net/RaffaeleDiFazio/fallacies-of-distributed-computing-with-kubernetes-on-aws)
    * involved: AWS, unhealthy nodes, Ingress, CronJob
    * impact: production outage

You can also refer to the bugs and the vulenrablities from [Bugcrowd](https://bugcrowd.com/) and [Hackerone](https://www.hackerone.com/)
