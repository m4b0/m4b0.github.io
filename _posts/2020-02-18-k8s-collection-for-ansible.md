---
layout: post
title: "The Kubernetes Collection for Ansible"
tags: opensource cncf ansible collection kubernetes k8s
date: 2020-02-18
---

![Kubernetes Collection for Ansible image](https://www.jeffgeerling.com/sites/jeffgeerling.com/files/images/opera-bull-ansible.jpeg)

The Ansible community has long been a victim of its own success. Since I got started with Ansible 
in 2013, the growth in the number of Ansible modules and plugins has been astronomical. That's what 
happens when you build a very simple but powerful tool—easy enough for anyone to extend into any 
automation use case.

The k8s modules and plugins that existed as part of the main ansible package in Ansible 2.9 and 
earlier will still be present in Ansible 2.10 if you run pip install ansible, but I'd recommend 
depending on and using the Kubernetes Collection directly, to make sure you can use the latest 
code as soon as it becomes available.

We're still in the early days of moving the k8s content out of the main Ansible repo into the 
Collection repo, but it's already easier than ever to contribute Kubernetes content! The collection 
includes three sets of tests—all which can be run locally:

- Sanity tests, run via ansible-test sanity --docker, which check for module and documentation 
formatting issues, and for basic Python errors.
- Basic integration tests, run via ansible-test integration --docker, which check for underlying 
issues with Python libraries and the interaction with the Kubernetes API, on a local OpenShift instance.
- Full integration tests, run via molecule test, which test almost all aspects of each module in the 
collection, on a local kind cluster.

You can run these tests, and even use the local environment with molecule to do development work and 
test bug fixes for the Collection. Read more about 
[Testing and Development](https://github.com/ansible-collections/kubernetes#testing-and-development) 
in the collection's README.

Further reading
- [Notes from the AnsibleFest Atlanta 2019 Ansible Contributor Summit](https://www.jeffgeerling.com/blog/2019/notes-ansiblefest-atlanta-2019-ansible-contributor-summit)
- [How to add integration tests to an Ansible collection with Molecule](https://www.jeffgeerling.com/blog/2019/how-add-integration-tests-ansible-collection-molecule)
- [How to evaluate community Ansible roles for your playbooks](https://www.jeffgeerling.com/blog/2019/how-evaluate-community-ansible-roles-your-playbooks)

[Full article](https://www.jeffgeerling.com/blog/2020/kubernetes-collection-ansible)
