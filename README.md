# Ansible
### Create Stack script 
put this script 
`#!/bin/bash`

### Click on 
![image](https://user-images.githubusercontent.com/66588814/187157811-f585ad5f-5995-4556-9321-5f94fb047a63.png)
Deployment new Linode and make 3 instance 

### Download Python, SSH, and Ansible on Master System 

### After installation go to the master node and put the IP of two other OS in the host 
cd /etc/ansible/host

### One more change on ansible.cong 
enable 
`host_key_checking = False`

###  Ping the other two host 
`ansible linux -m ping`


### With the help of cat command you can check on child server aslo
` ansible linux -a "cat /etc/os-release"`

### Write one Playbook save with filename.yaml
```
- name: ilovenano
  hosts: linux
  task:

    - name: ensure nano is there 
      apt:
        name: nano
        state: latest
```


### Run it 
`ansible-playbook filename.yaml
`




