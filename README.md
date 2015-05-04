# ansible-hackday
References and materials for GCB Informatics Ansible Hackday

GCB Informatics is running a hack day on May 7, 2015. This event will focus on automated provisioning of servers, specifically using [Ansible](http://ansible.com).

## Contributing

Please feel free to append to this file before the hackday, especially to include use cases or other references. We do not plan to make __playbooks__ public, but methods/resources and tasks for the the hackday should be tracked in this repo.

## Preparation

To have a productive hackday, everyone should familiarize themselves with:

1. [Installing Ansible](http://docs.ansible.com/intro_installation.html#installing-the-control-machine) aka Ansible Core - the command-line application. Ansible's [main website](http://ansible.com) makes it hard to discover that there is a [FOSS python command-line application](https://github.com/ansible/ansible
) called `ansible`, which is what we're primarily interested in. The [docs](http://docs.ansible.com) are great though, and ansible can be installed with your package manager of choice (yum/apt/brew), with python's `pip`, or from source.
2. The infrastructure pieces - how ansible runs, and how this compares to other provisioning/config systems:
  - a "control machine" where ansible itself executes (typically on-demand)
  - one or more managed nodes that are configured by the control machine.
3. The functional pieces - how to configure ansible to do your bidding:
  - [Inventories](http://docs.ansible.com/intro_inventory.html) - Lists of hosts (managed nodes) and their groupings (e.g. web servers, database servers)
  - [Playbooks](http://docs.ansible.com/playbooks.html) - recipes that the control machine executes on a managed node. [Best Practices](https://docs.ansible.com/playbooks_best_practices.html)
  - [Modules](http://docs.ansible.com/modules_by_category.html) - the steps in the recipe, tailored to specific software packages (e.g. the [yum module](http://docs.ansible.com/yum_module.html#examples) will install packages via yum declaratively.

## Examples/resources/further reading

[ansible-examples](https://github.com/ansible/ansible-examples) Ansible's own examples for playbooks demonstrating best practices
[Playbooks special topics](http://docs.ansible.com/playbooks_special_topics.html) - advanced or clever tricks for playbooks - step debugging, dry-run, lookups, tags, vault
[GCB's ansible playbooks on gitorious](https://gitorious.oit.duke.edu/gcb-it/ansible_playbooks) - Limited use for now - focused on a few web applications, but shows a concrete example of what can be done
[Ansible Galaxy](https://galaxy.ansible.com) - Community repository of playbooks for reuse. Like GitHub for ansible playbooks.

## Targets

__Prior to the hackday, please list a few (2-3) use cases to consider/generate ideas__

### Dan L:
1. Compiling and deploying cookieDaemon securely (with passwords, ssh keys, etc stored in [vault](http://docs.ansible.com/playbooks_vault.html))
2. Building/updating/deploying docker images on local resources (local registry, no docker hub)
