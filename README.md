# Chronograph Ansible Playbook

Use this to set up Chronograph on your webservers.

```
  ansible-playbook \
    --inventory $CHRONOGRAPH_INVENTORY \
    --user $CHRONOGRAPH_USER \
    --private-key $CHRONOGRAPH_PRIVATE_KEY \
    --extra-vars chronograph_jar=./chronograph.jar \
    --extra-vars chronograph_config=./config.edn \
    --become
    webserver.yml
```

### Run tests

Curretly, this is just a simple http request to the provisioned machine on port
8000. The extra_vars in Vagrantfile expect ./chronograph.jar and ./config.edn to exist.

To run them:
```
$ vagrant up --provision
```
