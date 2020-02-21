# test-delete-me

# Demonstration - Preparation

1.  Create an ADC Data Center - Latest Instance (OneLogin)
2.  Ensure most recent Github repo is cloned ([https://github.com/mthiel117/adc-demo-examples](https://github.com/mthiel117/adc-demo-examples)), remove existing configlets and copy read\_csv.py ansible module into place.

```sh
ssh arista@\<adchost-public address\>
Select Shell (bash):  98
cd adc-demo-examples
git pull
rm configlets/*
sudo cp extras/read_csv.py /usr/local/lib/python2.7/dist-packages/ansible/modules/files/.
```

3.  Detach &amp; Remove all ADCDEMO configlets from CVP.
 

# Demos

1. Demonstrate Ansible playbook to create version controlled switch configurations from CSV file
  - Change directory to demo1
```
cd adc-demo-examples/demo1
```
  - Show Playbook, CSV Datafile and Jinja2 Template
```
cat create-configlets.yml
cat datafiles/switch\_info.csv
cat templates/base-cfg.j2
```
