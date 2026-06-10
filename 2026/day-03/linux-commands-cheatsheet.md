# Linux Commands Cheat Sheet

## 1. Process Management

| Command                   | Usage                                     |
| ------------------------- | ----------------------------------------- |
| `ps aux`                  | View all running processes                |
| `top`                     | Monitor CPU and memory usage in real time |
| `htop`                    | Interactive process viewer                |
| `pgrep nginx`             | Find process ID by name                   |
| `kill <PID>`              | Terminate a process                       |
| `kill -9 <PID>`           | Force kill a process                      |
| `pkill nginx`             | Kill process by name                      |
| `systemctl status nginx`  | Check service status                      |
| `systemctl restart nginx` | Restart a service                         |
| `journalctl -u nginx`     | View service logs                         |

### DevOps Scenario

A web application becomes slow. Use `top` to identify a Java process consuming 95% CPU. Check logs with `journalctl`, restart the service using `systemctl restart`, and verify recovery.

---

## 2. File System Commands

| Command                   | Usage                   |
| ------------------------- | ----------------------- |
| `pwd`                     | Show current directory  |
| `ls -lah`                 | List files with details |
| `cd <dir>`                | Change directory        |
| `mkdir project`           | Create directory        |
| `cp file1 file2`          | Copy files              |
| `mv old new`              | Move or rename files    |
| `rm file.txt`             | Delete file             |
| `find / -name nginx.conf` | Search for files        |
| `du -sh *`                | Check directory sizes   |
| `df -h`                   | Check disk usage        |

### DevOps Scenario

Users report application failures. `df -h` shows disk usage at 100%. Use `du -sh *` to find large log files and free space to restore service.

---

## 3. Log Analysis Commands

| Command              | Usage                     |
| -------------------- | ------------------------- |
| `tail -f app.log`    | Monitor logs in real time |
| `less app.log`       | Read large log files      |
| `grep ERROR app.log` | Search for errors         |
| `cat file.txt`       | Display file contents     |
| `head file.txt`      | View first lines          |
| `tail file.txt`      | View last lines           |

### DevOps Scenario

An API returns HTTP 500 errors. Use `tail -f` to watch logs live and `grep ERROR` to identify the root cause quickly.

---

## 4. Networking Troubleshooting

| Command                   | Usage                     |
| ------------------------- | ------------------------- |
| `ping google.com`         | Test network connectivity |
| `ip addr`                 | Show IP addresses         |
| `curl http://service-url` | Test web endpoints        |
| `dig google.com`          | DNS lookup                |
| `nslookup google.com`     | Query DNS records         |
| `ss -tulpn`               | View listening ports      |
| `netstat -tulpn`          | Check network connections |
| `traceroute google.com`   | Trace network path        |

### DevOps Scenario

Users cannot access a website.

1. Verify server IP using `ip addr`.
2. Check service port using `ss -tulpn`.
3. Test endpoint with `curl`.
4. Validate DNS resolution using `dig`.
5. Use `ping` and `traceroute` to identify network issues.

---

## 5. Quick Daily Commands

| Command    | Usage                       |
| ---------- | --------------------------- |
| `whoami`   | Show current user           |
| `uname -a` | Display system information  |
| `free -h`  | Check memory usage          |
| `uptime`   | Show system uptime and load |
| `history`  | View command history        |

---

## Why This Matters for DevOps

Most production incidents are solved from the command line.

### Example Incident: Website Down

1. Check if the service is running:

   ```bash
   systemctl status nginx
   ```

2. Review logs:

   ```bash
   journalctl -u nginx
   ```

3. Verify CPU and memory:

   ```bash
   top
   free -h
   ```

4. Check disk space:

   ```bash
   df -h
   ```

5. Test connectivity:

   ```bash
   curl localhost
   ping server-ip
   ```

6. Restart service if required:

   ```bash
   systemctl restart nginx
   ```

### Benefits

* Restore services faster
* Reduce downtime
* Troubleshoot confidently
* Improve reliability of production systems
* Build trust as a DevOps engineer
