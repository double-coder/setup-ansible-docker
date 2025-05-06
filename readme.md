## How to use

*Github CLI* 

```bash
gh repo clone double-coder/setup-ansible-docker
```

From root run - 

```bash
# bring containers up
docker compose up -d

# connect to ansible container
docker exec -it ansible_controller ansible-playbook inventory.ini ping.yml
```
