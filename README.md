# ansibleDeployBigip
# ansible-playbook for installing as3 rpm package and deploy as3 declaration to BIG-IP.

BIG-IP variables are managed in bigip_vars.yml

USAGE:

Deploy AS3 declaration (as3.json) to BIGIP host with optional USER (default=admin), PASSWORD (default=admin)

ansible-playbook deploy_as3.yml -e "BIGIP=10.0.0.1"
ansible-playbook deploy_as3.yml -e "BIGIP=10.0.0.1 PASSWORD=admin"
ansible-playbook deploy_as3.yml -e "BIGIP=10.0.0.1 USER=admin PASSWORD=admin"

Deploy AS3 templated declaration (as3-http-app.j2, http_app_vars.yml) to BIGIP host with optional USER (default=admin), PASSWORD (default=admin)

ansible-playbook deploy_as3_http_app.yml -e "BIGIP=10.0.0.1"
ansible-playbook deploy_as3_http_app.yml -e "BIGIP=10.0.0.1 PASSWORD=admin"
ansible-playbook deploy_as3_http_app.yml -e "BIGIP=10.0.0.1 USER=admin PASSWORD=admin"

Delete all tenants and uninstall as3 package from BIG-IP host with optional USER (default=admin), PASSWORD (default=admin):

ansible-playbook delete_as3.yml -e "BIGIP=10.0.0.1"
ansible-playbook delete_as3.yml -e "BIGIP=10.0.0.1 PASSWORD=admin"
ansible-playbook delete_as3.yml -e "BIGIP=10.0.0.1 USER=admin PASSWORD=admin"
