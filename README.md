# Managing Large Data Sets with Ansible

Repository to explore issues and strategies for dealing with large data sets in Ansible.

## Loops

### Ansible Loops are Slow

Check out the difference between the bultin Ansible `loop` and `jinja2` loops to combine a bit of data with existing data.

Testing with `jinja2`

```sh
time ansible-playbook playbook-loops.yml --tags combine_jinja
```

Now with `loop`

```sh
time ansible-playbook playbook-loops.yml --tags combine_loop
```

Also, with `with_items`

```sh
time ansible-playbook playbook-loops.yml --tags combine_with
```

Test all of them and ensure same list

```sh
time ansible-playbook playbook-loops.yml
```
