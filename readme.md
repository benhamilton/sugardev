# sugardev - sugarcrm development environments

**Note**: This information is loosely based on this [SugarCRM KB](https://support.sugarcrm.com/Resources/Environments/Development_Environments/Vagrant_Development_Environment/)

**Note**: If you need to restore a SugarCRM backup, the additional information [on how to restore the MySQL database and change locations](https://support.sugarcrm.com/Knowledge_Base/Platform_Management/Cloning_a_Sugar_Instance_for_Testing/) will be useful.

## Pre-requisites

- [Vagrant](https://www.vagrantup.com/docs/installation/)
- [Virtual box](https://www.virtualbox.org/wiki/Downloads)
- SugarCRM files (You'll need to get these from SugarCRM)

## Steps

1. Create a directory i.e. `SugarEnt-9.0.0` and change to that directory
2. Copy the SugarCRM install files to that folder i.e. `SugarEnt-9.0.0.zip`
3. Run the following commands to do the initial setup:
```bash
vagrant init sugarcrm/php71es56
vagrant up --provider virtualbox
```

To suspend this SugarCRM instance:
```bash
vagrant suspend
```

To restart this SugarCRM instance, change to it's folder and run:
```bash
vagrant up
```

[Visit this instance in the browser](http://localhost:8080/sugar/) by visiting:
```
http://localhost:8080/sugar/
```

If you have more than one instance setup, you can run:
```bash
vagrant global-status
```
to see a list of vagrant instances and their status.

To delete/destroy a vagrant instance:
```bash
vagrant destroy XXXXXXXX
```
where XXXXXXXX is the ID listed in the out put of the `global-status` command.
