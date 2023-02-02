For grading purposes, please refer to apache_linux.yml

To Test the Playbook:

1. Ensure the Linux machine has ansible and SSH installed.
 ```
    sudo apt-get update
    sudo apt-get install software-properties-common
    sudo apt-add-repository ppa:ansible/ansible
    sudo apt-get update
    sudo apt-get install ansible
```
```
    sudo apt-get update
    sudo apt-get install openssh-server
    sudo systemctl start ssh
    sudo update-rc.d ssh enable
```

2. Add "[local]" and "127.0.0.1" host where we want to run the script on to the `/etc/ansible/hosts` file.

3. Run the script using the following Ansible command:
 ```
    ansible-playbook apache_linux.yml
 ```

4. Access the website by visiting `http://localhost/hospital`