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
