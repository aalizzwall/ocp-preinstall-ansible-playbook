OpenShift Install ansible playbook
==============================
How to use?
-----------

* In `preinstall` folder 

  * Config YUM Repo Server (`/etc/yum.repos.d/ocp-private.repo`)
  ```
  # ansible-playbook -i hosts yum-repo.yml
  ```
  _Note_ Office `rhel_yum_repo_server` = http://rhlab1.demo.com:8008/repo/

  * Install Package & Config Setting before OpenShift 
  ```
  # ansible-playbook -i hosts preinstall.yml
  ```
  
  _Note_ Not included
  * hostnamectl `hostnamectl set-hostname ocp-master1.example.com`
  * docker-storage-setup `volume group`

* After Install

  * dnsmasq `.xpaas.example.com`
  ```
  # ansible-playbook -i hosts dnsmasq.yml
  ```
