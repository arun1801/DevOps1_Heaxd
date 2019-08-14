# DevOps_Heaxd_Assignement

This project will perform below operation =

- Intsall Openshift Cluster on Centos machine with private registry
- Deploy Jenkins CI in Openshift Cluster
- Deploy a dummy application with Blue Green Logic using Jenkins Pipeline

## Ansible Role explanation

This project contains following roles used in playbook

- `common` - This role will install all the prerequisites for the Openshift cluster
- `okd-cluster` - This will install openshift cluster using officially documented [playbooks](https://github.com/openshift/openshift-ansible) by openshift.
- `jenkins` - This will deploy the Jenkins CI application on Openshift Cluster
- `app` - This role contains a dummy pipeline documented in openshift documentation for blue green deployment. This will take approval while doing deployment and perform the blue green deployment.

## Usage

```bash
   ansible-playbook -v playbook.yml
```
