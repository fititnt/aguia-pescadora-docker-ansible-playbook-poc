# aguia-pescadora-docker-ansible-playbook
Veja https://github.com/EticaAI/aguia-pescadora/issues/32


## Instalação

```bash
cp hosts.dist hosts

# Configure qual servidor quer fazer a instalação
vi hosts
ansible-playbook -i hosts aguia-pescadora-docker.yml
```

### Requisitos para instalação

#### Ansible

- [Ansible](https://www.ansible.com/)

#### Roles usados pelo Ansible

O usa o [nickjj/ansible-docker](https://github.com/nickjj/ansible-docker).
(Testado com a versão v1.8.0 (2018-12-19) do nickjj/ansible-docker, porém
versões mais novas possivelmente devem permanecer funcionando).

```
ansible-galaxy install nickjj.docker
```
