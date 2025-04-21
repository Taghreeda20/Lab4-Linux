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


5-

