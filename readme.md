## How to use

*Clone repo* 

From root run - 

```bash
# bring containers up
docker compose up -d

# connect to ansible container
docker exec -it ansible_controller ansible-playbook inventory.ini ping.yml

## create ansible folders master_playbook.yaml
ansible-playbook -e project_root=test master_playbook.yaml
```
