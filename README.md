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
