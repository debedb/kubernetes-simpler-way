# Kubernetes simpler way

## Background

Inspired by @kelseyhightower's [Kubernetes The Hard
Way](https://github.com/kelseyhightower/kubernetes-the-hard-way), 
these are just notes from installing Kubernetes for my own purposes
(largely, [development](http://romana.io/) and research). This, of
course, is not intended to be anywhere near production.

This is not a PR to the original because I couldn't quite figure out
how to make it make sense in parallel to the all-encompassing
original. If anyone has an idea, let me know.

## Goals

The goal is to focus on being able to experiment with K8S
functionality which is the added value and ignore things that are
not. For example, security is an issue everywhere, and so it is an
orthogonal concern and just gets in the way (I really do not need to
spend time on signing certificates and stuff if all I want is to
deploy Kubernetes on a few local VMs). Similarly, an issue of 
operating HA etcd. 

## Differences

The following are the major things that are changed/adopted from the
original:

 * etcd and master nodes do not need to be HA; a single node will do
 * Completely ignore security (no certs, no SSL/TLS/HTTPS)
 * Can do with a single node (the master is also a single worker)
 * Not limited to
[GCP](https://github.com/kelseyhightower/kubernetes-the-hard-way/blob/master/docs/01-infrastructure-gcp.md),
but starting with VMWare Fusion (because that's one piece of my
infrastructure). 

## Labs

 * Provisioning
   * [VMWare Fusion] (this assumes VMWare Fusion Pro 8.5.0 for now)
     * This assumes OSX with Kubernetes installed (TBD)
   


## See also

 * https://github.com/kubernetes/kops/
 * https://github.com/kubernetes/kubeadm/