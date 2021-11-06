# My Ansible Config

## Dev Workflow

Build a docker image for testing

```console
you@host$ docker build -t nvm-computer .
```

Modify the local.yml file however you'd like. Then use the `rebuild` script to create a container and open a terminal into it

```console
you@host$ ./rebuild
```

Once inside of the docker container, run the ansible playbook using the `run-ansible` script
```console
root@9bh23e$: ./run-ansible
```

Ansible will run and install/configure the container. You can modify the ansible command inside `run-ansible` to only run specific tasks with a particular tag.

## Realworld Usage

Install ansible on your new computer (**TODO**: provide a bash script that can be copied for doing this). Then run this playbook:
```console
you@host$ ansible-pull -U https://github.com/ncko/ansible --ask-become-pass --ask-vault-pass
```

## Todo
- provide a bash script that can be copied and created in a new environment to install ansible and run this playbook
