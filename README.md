# Chronograph Ansible Playbook

Use this to set up Chronograph on your webservers.

```
  ansible-playbook \
    --inventory $CHRONOGRAPH_STAGING_INVENTORY \
    --user $CHRONOGRAPH_STAGING_USER \
    --private-key $CHRONOGRAPH_STAGING_PRIVATE_KEY \
    --become
    webserver.yml
```
