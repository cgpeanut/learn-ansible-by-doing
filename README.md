# learn ansible by doing
    <h1><center>git-setup</center></h1>
    <center><img src="Images\git-setup.png"></center
### Chapter 2: Installtion and Configuration
    - lab 1: Deploying ansible
    1. login to Control Host server with ssh.
    - ssh cloud_user@control-server-ip-address
    - sudo yum install epel-release
    -  sudo yum install ansible
    2. Create an Ansible Useri on the control node.
    - sudo useradd ansible
    3. Connect to the workstation node
    ssh workstation
    4. Add ansible user to workstation and set ansible password.
    - sudo useradd ansible
    - sudo passwd ansible
    - logout
    5. Configure Ansible User on the Workstation Host so sudo works without password.
    - Log in to the workstation host as cloud_user.
    - ssh cloud_user@workstation
    - sudo visudo: add below root
    - ansible   ALL=(ALL)   NOPASSWD: ALL
    - logout
    6. Create simple inventory
    - create a simple inventory, /home/ansible/inventory, consistng of only the workstation host.
    - On the control host, as the ansible user, run the following commands:
    - vim /home/ansible/inventory
    - add the test "workstation" to the file and save using wq! in vim
    7. Write an Ansible Playbook
    - we need to write an Ansible playbook in /home/ansible/git-setup.yml on the control node.
    - vim /home/ansible/git-setup-yml
    - add the following test to the file
    <h1><center>git-setup</center></h1>
    <center><img src="Images\git-setup.png"></center>
    - lab 2: Getting started with ansible
    - lab 3: Ad-Hoc Ansible Commands
    - lab 4: Working with Ansible Inventories

### Additional Resources
Install Ansible on the control host.
    - sudo yum install epel-release
    - sudo yum install ansible
Create an 'ansible' user on both the control host and workstation host being sure to set password.
    - On each host, run the noted commands below. Make sure you set a password. Assuming you are cloud_user
    - sudo useradd ansible
    - sudo passwd ansible
Configure a pre-shared key for Ansible that allows the user to log in from 'control' to 'workstation' without password. 
    - sudo -i -u ansible (provide cloud_user a sudo password)
    - ssh-keygen (accept defaults)
    - ssh-copy-id workstation (provide ansible user a password)
    - logout

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