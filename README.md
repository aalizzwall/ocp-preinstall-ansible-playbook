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


  * Install Package & Config Setting before OpenShift
  
  ```bash
  # ansible-playbook -i hosts preinstall.yml
  ```

  * Install docker and setup docker-storage

  ```bash
  # ansible-playbook -i hosts docker-storage.yml
  ```

##### (Option)
  * Setup nfs-server

  ```bash
  # ansible-playbook -i hosts nfs-server.yml
  ```

  * Set selinux permissive

  ```bash
  # ansible-playbook -i hosts selinux.yml
  ```

#### In `afterinstall` folder
##### After Install


  * dnsmasq `.xpaas.example.com`
  
  ```bash
  # ansible-playbook -i ../afterinstall/hosts dnsmasq.yml
  ```

### Maybe issue

  * Cant resolv s2i registry fqdn , like `cluster.svc`
