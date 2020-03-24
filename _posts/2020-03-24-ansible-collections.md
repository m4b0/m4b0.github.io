---
layout: post
title: "Hands on with Ansible Collections"
tags: ansible collections
date: 2020-03-24
---

![Developer image](https://pbs.twimg.com/card_img/1242482564289437696/afaJ9cFm?format=jpg&name=small)

Ansible collections have been introduced previously through two of our blogs 
[Getting Started with Ansible Content Collections](https://www.ansible.com/blog/getting-started-with-ansible-collections) 
and [The Future of Ansible Content Delivery](https://www.ansible.com/blog/the-future-of-ansible-content-delivery). 
In essence, Ansible Automation content is going to be delivered using the collection packaging mechanism.  Ansible 
Content refers to Ansible Playbooks, modules, module utilities and plugins. Basically all the Ansible tools that 
users use to create their Ansible Automation. Content is divided between two repositories:

Ansible Galaxy ([https://galaxy.ansible.com](https://galaxy.ansible.com/))
Automation Hub ([https://cloud.redhat.com/ansible/automation-hub](https://cloud.redhat.com/ansible/automation-hub))

Ansible Galaxy is the upstream community for sharing Ansible Collections.  Any community user can create a 
namespace and share content with anyone. Access to Automation Hub is included with a Red Hat Ansible Automation 
Platform subscription.  Automation Hub only contains fully supported and certified content from Red Hat and our 
partners. This makes it easier for Red Hat customers to determine which content is the official certified, and 
importantly supported, content.  This includes full content from partners such as Arista, Cisco, Checkpoint, F5, 
IBM, Microsoft and NetApp. 

Here is my setup for this demonstration of Ansible Collections:

![Ansible tree image](https://www.ansible.com/hs-fs/hubfs/Ajay%20blog%201.png?width=177&name=Ajay%20blog%201.png)

- ansible.cfg is the Ansible configuration file.  I will elaborate on this in the next section.
- collections is a directory storing all Ansible Collections that my Ansible Playbook will use
- inventory is a directory containing a inventory file named hosts
- play.yaml is my Ansible Playbook

For my example this is a development environment where I just want to download the latest and greatest.  I will use a gitignore file to ignore the downloaded content and only track the requirements file.

![Git ignore image](https://www.ansible.com/hs-fs/hubfs/Ajay%20blog%202.png?width=551&name=Ajay%20blog%202.png)

We define the Galaxy servers under the [galaxy] section of the Ansible configuration file (i.e. ansible.cfg).  An 
Ansible configuration file is an ini formatted file for configuring behavior settings.  This includes settings 
such as changing the return output from JSON to YAML. If you are unfamiliar with an Ansible configuration file 
please refer to the [documentation](https://docs.ansible.com/ansible/latest/installation_guide/intro_configuration.html). 
As a reminder the Ansible configuration file is searched in the following order:

1. ansible.cfg (in the current directory)
2. ~/.ansible.cfg (in the current home directory)
3. /etc/ansible/ansible.cfg 

These tokens should be added now to the ansible.cfg file. An example of this is shown below.  It is recommended 
when using more than one Galaxy server to list them in server_list. The list should be in precedence order with 
your primary location choice first, in this case Automation Hub.

```
[defaults]
stdout_callback = yaml
inventory = inventory/hosts
collections_paths = ./collections

[galaxy]

server_list = automation_hub, release_galaxy

[galaxy_server.automation_hub]
url=https://cloud.redhat.com/api/automation-hub/
auth_url=https://sso.redhat.com/auth/realms/redhat-external/protocol/openid-connect/token
token=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

[galaxy_server.release_galaxy]
url=https://galaxy.ansible.com/
token=xxxxxxxxxxxxxxxxxxxxxx
```

Note the url and auth_url keys that define the Automation Hub repository and authentication endpoint. Also note that 
this file defines where the collections should be downloaded to via the collections_paths parameter (e.g.. ./collections). 
For more information on configuration for Ansible Galaxy and Automation Hub please refer to the 
[Galaxy User Guide](https://docs.ansible.com/ansible/latest/galaxy/user_guide.html#galaxy-user-guide).

Ansible Collections introduce a way to modularize and package automation content effectively. Red Hat Automation 
Hub hosts certified, secure collections that are validated and supported by Red Hat. Ansible Galaxy hosts community 
contributed collections. Customers can access collections from both content repositories. I think of collections as 
a superchargers to the “batteries included” approach that Ansible takes. It up-levels the nuances involved in 
building out automation, allowing users to plug-n-play the latest and greatest automation content being built by 
certified partners and the community.

[Full article](https://www.ansible.com/blog/hands-on-with-ansible-collections)
