# PAH - Execution Environments
This Ansible playbook uses the Ansible role infra.ee_utilities.ee_builder to build EEs and upload them to Red Hat Private Automation Hub.

The Ansible Role documenation can be found here: https://galaxy.ansible.com/ui/repo/published/infra/ee_utilities/content/role/ee_builder/

## Getting Started
1. Go through all the variable files in vars/ and give it account infomation.

2. In vars/ee.yml - Edit the variable ee_list with all of your EEs. An example for the Role documention is given along with our current EEs.

3. Target a RHEL host that can support podman.

3. In the Ansible Controller Job Template:
    - Add the Extra Var below in the playbook launch
    - Enable Privilege Escalation option

### Needed Extra Vars
aap_environment = 'test' / 'prod' # to choose what PAH environment configuration file to use