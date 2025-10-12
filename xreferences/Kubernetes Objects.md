---
category:
  - "[[Courses]]"
author:
  - Nigel Poulton
cover: 
genre:
  - "[[IT-Cloud]]"
length: 
year: 2024
rating: 7
topics:
  - "[[Cloud Computing]]"
  - "[[Kubernetes]]"
last: 2024-11-20
via: ""
tags:
  - references
  - courses
created: 2024-11-20
---


## In A Nutshell

Okay, cloud gurus.
Kubernetes is all about cloud native, yeah?
I've banged that drum for long enough.

## Containers and Pods

A major force driving cloud native is containers.

I mean there's serverless and other stuff as well right,
but containers are the poster child for cloud native.
Only shock horror, Kubernetes doesn't run containers
or at least it doesn't run them directly.
Kubernetes wraps containers in a high level construct called a pod.

So think of it like this.

- VM: Atomic unit for a virtualization environment is the VM
- pod: Atomic nit for a Kubernetes environment is the pod

So the smallest thing you can deploy on a Kubernetes cluster is a pod,
but inside of each pod is one or more containers.

Anyway, application code exists in containers and containers run in pods on Kubernetes.
Well, the pod is an object on the cluster and it's defined in the API as a resource under the core API group.

But pods on their own don't give us a great deal.
So we wrap them in a high level object called a deployment.
## Deployment

So we wrap them in a high level object called a deployment.
This again, is an object on the cluster and it's a resource in the apps API group.

Now, the whole idea of deployments is to make pods scalable,
making rolling updates and rollback simple and a ton of other cool stuff.

So, kinda cool, but really it's about being flexible and more useful.

So, pods and deployments exist in the API.
They can be deployed on the cluster as objects and they're two of the key primitives that make Kubernetes an ideal platform for cloud native micro services apps.


Now, deployments are great for scaling and updates but other objects exist for wrapping your pods.

So, DaemonSets make sure that one and only one of a specific pod will run on every worker in the cluster. 
And then we've got stateful sets for pods or parts of your application with particular stateful requirements.
But away from wrapping and adding to pods there's even more.
Secrets, volumes, low balances, you name it right?

They're all resources in the API and they get deployed on the cluster as objects.

Now I could talk all day about stuff like this
and I'm giving you this primer in case you're new to it all.
But I'm also conscious of time
and that some folks already know it.
So I'm gonna park it there.
If you need more, check out my book.
I cover all the basics you'll need in there.
Time to move on though.
Next up, we're gonna look at a few quick ways
to get a cluster up and running.
And actually if you're already cool with this,
feel free to give it a miss and skip right over.
