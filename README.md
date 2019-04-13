# raspberry-utils
Tools for embedded linux based on raspberry

enable ssh on raspbian:

systemctl enalble ssh

or

systemctl enable ssh.service

generate public rsa on the ssh-client:
ssh-keygen -t.rsa

save on ~/.ssh/id_rsa

copy ssh-key to rasp:
ssh-copy-id -i ~/.ssh/id_rsa pi@192.168.0.5
or manually:
copy the file ~/.ssh/id_rsa to ~/.ssh/authorized_keys		(client->server)

on the rasp:
add or edit the lines below, in the file /etc/ssh/sshd_config

PermitRootLogin no

PubkeyAuthentication yes

PasswordAuthentication no



