# Linux Architecture Notes

## 1. Core Components of Linux

### Kernel
- The core of the Linux operating system.
- Manages CPU, memory, storage, devices, and processes.
- Acts as a bridge between hardware and applications.

### User Space
- Area where user applications run.
- Examples: Bash, Vim, Nginx, Docker.
- Applications interact with the kernel through system calls.

### Init / systemd
- First process started by the kernel (PID 1).
- Responsible for starting and managing system services.
- Most modern Linux distributions use **systemd** as the init system.

---

## 2. Process Creation and Management

### How a Process is Created
1. A parent process creates a child process using `fork()`.
2. The child process loads a program using `exec()`.
3. The kernel schedules the process to run on the CPU.

### Process States
- **Running (R)** – Currently executing or ready to run.
- **Sleeping (S)** – Waiting for an event (disk, network, user input).
- **Stopped (T)** – Paused by a signal.
- **Zombie (Z)** – Process finished but parent has not collected its exit status.
- **Uninterruptible Sleep (D)** – Waiting for I/O operations.

### Useful Process Commands
- `ps aux` – View running processes.
- `top` – Monitor CPU and memory usage.
- `htop` – Interactive process viewer.
- `kill <PID>` – Terminate a process.
- `pgrep <name>` – Find process IDs by name.

---

## 3. What systemd Does

### Key Responsibilities
- Starts system services during boot.
- Tracks and manages service lifecycles.
- Restarts failed services automatically.
- Handles dependencies between services.
- Collects logs through `journald`.

### Why systemd Matters
- Faster and more reliable boot process.
- Simplifies service management.
- Helps troubleshoot application failures.
- Essential for managing production servers.

### Common systemd Commands
- `systemctl status <service>` – Check service status.
- `systemctl start <service>` – Start a service.
- `systemctl stop <service>` – Stop a service.
- `systemctl restart <service>` – Restart a service.
- `journalctl -u <service>` – View service logs.

---

## 4. Five Linux Commands Used Daily

1. `ls` – List files and directories.
2. `cd` – Change directory.
3. `ps aux` – View running processes.
4. `top` – Monitor system resources.
5. `systemctl status <service>` – Check service health.

---

## DevOps Takeaway

Understanding Linux architecture helps you:
- Debug crashed services quickly.
- Investigate CPU and memory issues.
- Analyze logs effectively.
- Manage application restarts and service failures.## Why This Matters for DevOps

### Debug Crashed Services Faster

* Check service status using:

  ```bash
  systemctl status <service>
  ```
* View service logs:

  ```bash
  journalctl -u <service>
  ```
* Identify the reason for service failure and restart if needed.

### Fix CPU and Memory Issues

* Monitor resource usage:

  ```bash
  top
  ```
* Find processes consuming high CPU or memory:

  ```bash
  ps aux --sort=-%cpu
  ps aux --sort=-%mem
  ```
* Stop or investigate problematic processes using:

  ```bash
  kill <PID>
  ```

### Understand Logs and Service Restarts

* View system logs:

  ```bash
  journalctl
  ```
* Check service restart history:

  ```bash
  systemctl status <service>
  ```
* Analyze error messages to determine root causes.

### Incident Example

If a web server becomes unavailable:

1. Check service status.
2. Review logs for errors.
3. Verify CPU and memory usage.
4. Restart the service if required.
5. Confirm the service is running normally.

Understanding Linux processes and systemd helps reduce troubleshooting time and improves incident response in production environments.

- Troubleshoot production incidents with confidence.

  
