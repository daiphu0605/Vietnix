# Linux Command

## ping

![Ping result](../Resource/LinuxComand/Ping/ping.png)

ttl: Time to live chỉ số lượt hay hop của packet tồn tại trong network (Router, DDiscard) trước khi bị xóa.

time: Round-Trip Time là thời gian mà gói tin icmp thực một vòng trong network.

## ssh

### Dùng Password

```bash
ssh phu@172.16.207.130
```
![ssh password](../Resource/LinuxComand/SSH/ssh_password.png)

### Dùng key

Tạo key

```bash
ssh-keygen -t rsa -b 4096
```
![create keygen](../Resource/LinuxComand/SSH/ssh_keygen.png)

Copy Public Key cho Server

```bash
ssh-copy-id -i ~/.ssh/id_rsa.pub phu@172.16.207.130
```
![send public key](../Resource/LinuxComand/SSH/ssh_copy_ID.png)

Kết nối

```bash
ssh phu@172.16.207.130
```
![connection](../Resource/LinuxComand/SSH/ssh_connect_with_key.png)

### Dùng port custom

Cấu hình port ssh trên server

```bash
sudo vi /etc/ssh/sshd_config
```
![config](../Resource/LinuxComand/SSH/config_ssh-port.png)
Cấp phép firewall

```bash
sudo firewall-cmd --permanent --zone=public --add-port=3022/tcp
sudo firewall-cmd --reload
sudo firewall-cmd --list-port
```
![config](../Resource/LinuxComand/SSH/config_firewall.png)
Cấp phép Selinux

```bash
sudo dnf install policycoreutils-python-utils # sử dung khi semanage not found
sudo semanage port -a -t ssh_port_t -p tcp 3022
sudo semanage port -l | grep ssh_port_t
```
![config](../Resource/LinuxComand/SSH/selinux_permission.png)
Khơi động lại sshd

```bash
sudo systemctl restart sshd
sudo systemctl status sshd
```
![check](../Resource/LinuxComand/SSH/Check_config.png)

Kết nối

```bash
ssh -p 3022 phu@172.16.207.130
```
![fail](../Resource/LinuxComand/SSH/SSH_Fail_connection.png)

![success](../Resource/LinuxComand/SSH/Result_ssh_port_custom.png)

## scp

chuyển thư mục
```bash
scp -P 3022 -r test phu@172.16.207.130:/home/phu
```

## rsync

## cat

## echo

## tail/head

## sed

## tracroute/tracert

## netstat

## sort

## wc

## find

## cp

## mv

## cut

## dig

## tar/zip/unzip

## mount/unmount

## Symbolic links, Hard Links

## ls

## ps

## kill

## top

## free

## df