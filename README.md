### Setup streaming postgresql replication

Requirements: 

ansible 2.8.1

master: vagrant vm Ubuntu 16 (ip 192.168.33.11) 

replica: vagrant vm Ubuntu 16 (ip 192.168.33.12) 

1. For setup master run

```
ansible-playbook -i environments/postgresql-hosts main.yml --tags setup_master
```

2. Copy replica's SSH public key to master

3. For setup replica run

```
ansible-playbook -i environments/postgresql-hosts main.yml --tags setup_replica
```