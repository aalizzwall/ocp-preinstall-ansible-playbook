# OpenShift Install ansible playbook 
## How to use?
-----------

### Pre Install 

#### In `preinstall` folder

.Note
  * Install Package & Config Setting before OpenShift
  ```bash
  # ansible-playbook -i hosts preinstall.yml
  ```

#### After Install

.Note
  * dnsmasq .xpaas.example.com
  ```bash
  # ansible-playbook -i hosts dnsmasq.yml
  ```

#### Other 

.Note
  * Config YUM Repo Server (`/etc/yum.repos.d/ocp-private.repo`)
  ```bash
  # ansible-playbook -i hosts yum-repo.yml
  ```
  _Note_ Office `rhel_yum_repo_server` = http://rhlab1.demo.com:8008/repo/
