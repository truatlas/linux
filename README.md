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
>error: write /dev/stdout: permission denied

problem solution:
```
kubectl create deployment webserver --image=nginx:alpine --replicas=3 --port=80 --dry-run=client \
-o yaml > >(cat > webserver.yaml)
```  
  
