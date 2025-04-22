# Lab4-Linux

1- List all running processes and save the output to ~/processes.txt :

    ps
    ps >> ~/processes.txt

2- Find the PID (Process ID) of the sshd service : 

    ps aux | grep sshd

3- Run a sleep 500 command in the background, then kill it after 5 seconds : 

    sleep 500 &
    sleep_pid=$!
    sleep 5
    kill $sleep_pid

4- Install apache2 service, edit the default HTML file (/var/www/html/index.html), and verify changes in a web browser : 

    sudo apt update
    sudo apt install apache2 -y
    sudo systemctl status apache2
    sudo nano /var/www/html/index.html
![image](https://github.com/user-attachments/assets/04e1d4ae-f40d-448e-8d49-9c99b0fb10fe)


5- Check if sshd (SSH service) is running. If not, start and enable it : 

    sudo systemctl status ssh
    sudo systemctl enable ssh
![image](https://github.com/user-attachments/assets/42134854-d898-43cf-a665-0a11269742ac)

6- Restart the cron service and verify its status :

    sudo systemctl restart cron
    sudo systemctl status cron
![image](https://github.com/user-attachments/assets/3ed7476a-f2e2-4911-b244-711b060a619a)

7- Create a compressed tarball (archive.tar.gz) of /var/log and save it in your home directory : 

    tar -czvf ~/archive.tar.gz /var/log
![image](https://github.com/user-attachments/assets/f4115837-d8f5-45de-97fe-41e6aa17af45)

8- Extract the tarball into ~/logs_backup/ :

    mkdir -p ~/logs_backup/
    tar -xzvf ~/archive.tar.gz -C ~/logs_backup/

9- Create a non-compressed tarball (archive.tar) of /etc/ssh and save it in /tmp :

    tar -cvf /tmp/archive.tar /etc/ssh

10- Compress ~/processes.txt using gzip :

    gzip ~/processes.txt
    
11- Decompress it and compare file sizes using ls -lh : 

    gunzip ~/processes.txt.gz
    ls -lh ~ | grep processes.txt

12- Install htop (a process viewer) using your package manager :

    sudo apt update
    sudo apt install htop
    htop

13- Search for the package nginx (or httpd) but do not install it : 

    apt search nginx

14- Remove the vim editor (if installed) and then reinstall it : 

    sudo apt remove vim 
    sudo apt install vim

15- Use wget to download the Linux kernel source :

    wget https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.8.2.tar.xz

16- Use curl to fetch Google’s homepage and save it as google.html :

    curl https://www.google.com -o google.html

17- Create a new VM (e.g., VirtualBox/Cloud instance), add a user to the sudoers group, and run apt update && apt upgrade : 





