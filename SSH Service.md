
1. Install the OpenSSH Server

```bash
  sudo apt install openssh-server

```

2. Check the SSH service status
```bash
  sudo systemctl status ssh

```

If the SSH service is not active, you can start it using:


```bash
  sudo systemctl start ssh

```

3. Enable SSH to start on boot
```bash
  sudo systemctl enable ssh
```
You can now connect to your Ubuntu machine using an SSH client by running: (checking purpose)
```bash
  ssh username@ip_address

```
