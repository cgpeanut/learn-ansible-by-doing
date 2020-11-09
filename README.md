# learn ansible by doing
### Chapter 2: Installtion and Configuration
![visudo](https://prnt.sc/vgceqx
    - lab 1: Deploying ansible
    - 1. login to Control Host server with ssh.
    - ssh cloud_user@control-server-ip-address
    - sudo yum install epel-release
    -  sudo yum install ansible
    - 2. Create an Ansible Useri on the control node.
    - sudo useradd ansible
    - 3. Connect to the workstation node
    ssh workstation
    - 4. Add ansible user to workstation and set ansible password.
    - sudo useradd ansible
    - sudo passwd ansible
    - logout
    - 5. Configure Ansible User on the Workstation Host so sudo works without password.
    - Log in to the workstation host as cloud_user. 
    - ssh cloud_user@workstation
    - sudo visudo: add below root
    ![visudo](https://prnt.sc/vgceqx)

    - logout
    6. Create simple inventory
    - lab 2: Getting started with ansible
    - lab 3: Ad-Hoc Ansible Commands
    - lab 4: Working with Ansible Inventories
Chapter 3: Plays and Playbooks
    - lab 1: Ansible Playbooks: The Basics
    - lab 2: Ansible Playbooks: Error Handling
    - lab 3: Working with Ansible Templates, Variables, and facts
    - lab 4: Writing Your First Ansible Playbook
    - lab 5: Deploying Service Using Apache
    - lab 6: Advanced Features in Ansible Playbooks
Chapter 4: Roles
    - lab 1: Working with Ansible Roles
Chapter 5: Working With Files 
    - lab 1: File Manipulation with Ansible
Chapter 6: Ansible Vault
    - lab 1: Working with Condfidential Data in Ansible