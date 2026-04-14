# what is linux ? 
- open source operating system developed by linus torwald in 1991
- in linux everything is a process 


## ip address => ip addr

storage and RAM kitna free h => FREE

disk file system => df 

1. free command

👉 RAM (Memory) check karne ke liye

Batata hai: total, used, free RAM
Example use: system slow hai ya nahi check karna

👉 Use kab?

Jab tumhe memory usage (RAM) dekhna ho

👉 Exam keyword: Memory / RAM usage

🔹 2. df command (disk free)

👉 Disk space (filesystem level) check karne ke liye

Batata hai: total disk, used, free space (entire partition)
Example: /, /home ka storage kitna bacha hai

👉 Use kab?

Jab tumhe poori disk ka free space dekhna ho

👉 Exam keyword: Filesystem / Disk free

🔹 3. du command (disk usage)

👉 Folder/file ka size check karne ke liye

Batata hai: specific folder ya file kitni space le raha hai
Example: /var/log kitna heavy hai

👉 Use kab?

Jab tumhe konsi folder/file space kha rahi hai pata karna ho

👉 Exam keyword: Directory/File usage

```
POWER ON
   ||
BIOS(motherboard)
   ||
GRUB(linux kernel)
   ||
ubuntu loading
   ||
init process (systemd)
    ||
systemctl (status,start, enable,stop)
```

🔥 Final Trick (yaad rakhne ke liye):
free → RAM
df → Disk free (poora system)
du → Disk usage (folder/file)

``` KERNEL VERSION ==> uname -r ```

``` /etc/os-release  ==> ubuntu version```
