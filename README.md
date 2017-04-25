# Introduction
The original repo is in [here](https://github.com/Woorank/vagrant-mesos-cluster). It's primarily for vagrant, and cannot be transparently applied to bare mental(I've tried but got a curious result).

# What I do
+ Rewrited some scripts and make it primarily for **Ubuntu 14.04**.
+ Add cAdvisor to mesos slaves

# Potential Bugs
+ In `cluster.yml`, I use `ansible_em1.ipv4.address` to refer the host ip, it works in my machines for the primary network interfaces are called `em1`, you may replace it with `eth0`

# How to use
+ Update your machines in `inventory/vagrant`
+ Make sure your current machine can access machines specified in `inventor/vagrant` via `root` without passwords
+ `ansible-playbook cluster.yml`
