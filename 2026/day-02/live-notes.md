# devops 
- operating system - windows macos linux 
- devops used linux because more than 90% of application are work on linux

LINUX - operating system
HEART -kernel (core of linux) - linux kernel


# ----------- linux architecture-------------
 hardware - kernel - shell - application
    |        |          |            |
    |        |          |          end  user 
    |        |         Interactive way to talk to kernel (command k through kernel se baat krega)
    |    computer program machine samajta hai 
    |     linux kernel c program m hai => 0101  aur yeh harware se baat krega 
RAM,CPU 


LINUX FLAVOURS/DISTRIBUTION
- ubuntu (mostly used)
- Fedora
- Centos(generally used)
- RHEL

# what is linux 
- Linux is a operating system developed by linus torwald in 1991
- everything in linux is file or directory
- everything in linux is a process
# why linux
- 90% of application are running on linux
# how do i learn linux?
- local system / aws account

=========================FILE SYSTEM Hierarchy===============================
      / => root 
      user=> system file (usr/bin)
      bin=> binaries [ ex=> cd (shell command ) -> c program -> 10100010) ]
      sbin -> system binaries (kernel level binaries) example jese lvm 
      /mnt => external disk ko mount krna 


      Exam keyword: Directory/File usage

POWER ON
   ||
BIOS(motherboard m power supply joh hardware ko load kr deta hai)
   ||
GRUB(linux kernel ko load krdo )
   ||
ubuntu loading (logo)
   ||
init process (systemd PID no. 1)
    ||
systemctl (status,start, enable,stop)


      example jese -> cp src destination hai
      cp-> bin-> c program -> computer language(process)

      
uname -r => kernel ka version
cat /etc/os-release => operating system info 

kill -9 => SIGKILL
ps -> active resources batat hai 
htop -> real time resource usage
nohup => background m script ko chalane k liye use hota hai
background m operator use hota hai -> &
pipe(|) is used for 2 command k output ko merge krne ke liye hota hai










       l=> link
       d=> directory(folder)
       - => file
       

    
