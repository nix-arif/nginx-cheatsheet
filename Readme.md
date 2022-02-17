# Installation

## Setup VirtualBox

- www.virtualbox.org

## Setup OS

- https://www.centos.org/download
- You will encounter problem with CentOS7 when running `yum update` or other command `Could not retrieve mirrorlist http://mirrorlist.centos.org/?release=7&arch=x86_64&repo=os&infra=stock error was `. Solve the with below command.

```
ONBOOT=on
dhclient
```

- After this 2 command, you can proceed with other command.
- Then install lynx (texteditor)

```
yum install lynx
```

- Install utilities

```
yum install wget
```

- Connect CentOS with nginx repository

1. Navigate to `/etc/yum.repos.d`

```
cd /etc/yum.repos.d
```

2. Create repo for nginx

```
vim nginx.repo
```

3. Content of `nginx.repo`

```
[nginx]
name=nginx repo
baseurl=http://nginx.org/packages/centos/$releasever/$basearch
gpgcheck=0
enable=1
```

4. Install nginx

```
yum install nginx
```

5. Start nginx

```
systemctl start nginx
```
