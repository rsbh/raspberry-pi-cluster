# raspberry-pi-cluster


## Install Ansible

```
brew install ansible
```

## Ping all

```sh
ansible cluster -m ping
```


## Install K3s on main machine

```sh
ansible-playbook playbooks/k3s.yml
```


## Verify the running k3s nodes

```sh
ansible pi-main -b -a "k3s kubectl get nodes"
```

## Install Github Actions Runner

```sh
ansible-playbook playbooks/ga-runner.yml -e runner_token={TOKEN}
```
