# linux
Some tips for linux


1. clean-snap.sh  
   How to remove unused snap packages in Ubuntu  
   It's easy to use:  
```sudo bash ./clean-snap.sh```

2. In Ubuntu get error kubectl permission denied  
   _error: write /dev/stdout: permission denied_
for example:
>kubectl create deployment webserver --image=nginx:alpine --replicas=3 --port=80 --dry-run=client -o yaml > webserver.yaml  
>**error: write /dev/stdout: permission denied**

problem solution:
```
kubectl create deployment webserver --image=nginx:alpine --replicas=3 --port=80 --dry-run=client \
-o yaml > >(cat > webserver.yaml)
```  
  
3. Uptime Kuma — free monitoring server.  
   HTTP(s)/TCP/Ping/DNS Record/Push/Steam Game Server/Docker  
   Can send messages to Telegram, Discord, Gotify, Slack, Pushover, Email (SMTP)  

4. OpenTofu is a fork of Terraform that is open source, community-driven, and managed by the Linux Foundation.
   
5. **Ventoy** is an open source tool to create bootable USB drive for ISO/WIM/IMG/VHD(x)/EFI files
6. **Talos** was made for bare-metal K8s  
7. If your Proxmox is too slow - just add _noatime_ into your /etc/fstab
8. Free smtp relay https://www.mailgun.com for 100 emails per day.
9. Network Policy Viewer Kubernetes  from yaml https://orca.tufin.io/netpol/
10.  Example how to deploy k8s on Hetzner with Talos and Terraform: https://github.com/masterbpro/mbrc
11.    
