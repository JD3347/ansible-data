# Bootstrapping a new production node

First add the node to inventories/production along with connection details.

Then install Python on the managed node. For example, on Ubuntu:

    ansible <name> -i ./inventory -m raw -a "apt-get update"
    ansible <name> -i ./inventory -m raw -a "apt-get -y install python"

Where <name> matches the name you gave the node in the inventory file.

Next add the node to site.yml along with the roles you want.
