# aguia-pescadora-docker-ansible-playbook-poc (Prova de Conceito)
**[rascunho-publico] Veja https://github.com/EticaAI/aguia-pescadora/issues/32**

> _Nota: ainda que este repositório esteja público, **não use este playbook**.
Ele serve apenas como prova de conceito e provavelmente serviria apenas
para ver o que pode ou não ser aproveitado em outros repositórios
(fititnt, 2019-07-21 03:53 BRT)_

## Instalação

```bash
cp hosts.dist hosts

# Configure qual servidor quer fazer a instalação no arquivo hosts
vi hosts

# Dependências
ansible-galaxy install nickjj.docker
ansible-galaxy install kibatic.traefik

# Execute o playbook
ansible-playbook -i hosts aguia-pescadora-docker.yml
```

### Requisitos para instalação

#### Ansible

- [Ansible](https://www.ansible.com/)

#### Roles usados pelo Ansible

Dica: para opções mais avançadas **inclusive procedimento de atualizações e/ou
downgrade de versões** você pode olhar documentação específica dos
desenvolvedores dos roles do ansible.

##### nickjj.docker
O usa o [nickjj.docker](https://github.com/nickjj/ansible-docker).
(Testado com a versão v1.8.0 (2018-12-19) do nickjj.docker, porém
versões mais novas possivelmente devem permanecer funcionando).

Você pode instalar usando

```bash
ansible-galaxy install nickjj.docker
```

##### kibatic.traefik

O usa o Usa o [kibatic.traefik](https://github.com/kibatic/ansible-traefik).
(Testado com a versão v1.7.6 (2019-01-07) do kibatic.traefik, porém
versões mais novas possivelmente devem permanecer funcionando).

Você pode instalar usando

```bash
ansible-galaxy install kibatic.traefik
```

# Licença
Domínio Público
