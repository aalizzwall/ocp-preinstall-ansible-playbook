# OpenShift Install ansible playbook 
## How to use?
-----------
### Env Prepare
 - hostname
 - docker-storage device

#### In `preinstall` folder

##### Config Private yum-repo Server


  * Config YUM Repo Server (`/etc/yum.repos.d/ocp-private.repo`)
  
  ```bash
  # ansible-playbook -i hosts yum-repo.yml
  ```
  _Note_ Office `rhel_yum_repo_server` = http://rhlab1.demo.com:8008/repo/

##### Pre Install 


  * Install docker and setup docker-storage

  ```bash
  # ansible-playbook -i hosts docker-storage.yml
  ```

  * Install Package & Config Setting before OpenShift
  
  ```bash
  # ansible-playbook -i hosts preinstall.yml
  ```

##### After Install


  * dnsmasq `.xpaas.example.com`
  
  ```bash
  # ansible-playbook -i hosts dnsmasq.yml
  ```

