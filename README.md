# ansible-automates-F5-lab
Laboratory to manage F5 (bigIP) load balancer

## How to start 

- Clone this repo in your VM instance for F5 lab.
- Check if the directory /tmp/tower_install exist.
- Copy the files tower-backup to /tmp/tower_install
```
sudo cp -v f5lab/tower-backup* /tmp/tower_install
```
- Load the backup in Tower. 
```
sudo /tmp/tower_install/setup.sh -r 
```
- Using your browser, connect to Tower and login with f5admin/ansible
- Use the license file to license your Ansible Tower. 
- Refresh your inventory 
```
sudo awx-manage inventory_import --inventory-name Inventory --source ~/networking-workshop/lab_inventory/hosts
```
- Refresh the SSH Private Key for the Web Servers, using the file: 
```
/home/student1/.ssh/aws-private.pem
```
- Check the connection with your Web Servers running a command from Tower.
- Go to your templates, and check that runs OK. 
- If you have any question, please raise your hand and ask to your instructors.
- Enjoy!!! :)
