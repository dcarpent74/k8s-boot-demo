To query local osinfo-db for VM setup using virt-install:

```
# osinfo-query os --fields="short-id,name,version" | \  
    grep Fedora | grep -v "Silverblue" | \  
    cut -d "|" -f 1,3 | sort -nk 3  
```
