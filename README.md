# Symetric policy based routing using ansible
The purpose of this playbook is to create a default route for every interface that you specify making it reachable from outside of it`s network
##usage:
1. The controlled node must be reachable by the controller via ssh 
2. To establish ssh passwordless login , use the playbook prepare_host.yml 
```
ansible-playbook prepare_host.yml  -u root -k
```
this should setup passwordless ssh login automatically 
3. Run :

  ````
  ansible-playbook main_02.yml
  ```
  first you will be prompted to enter the number of interfaces you want to add
 ```
 How many interfaces you want to add ?
 ```
 enter 1 for example 
 
```
enter IP address: 
192.168.0.0

```
```
enter Gateway:
192.168.0.1
```
```
enter subnet
192.168.0.0
```
```
enter prefix:
24
```
```
enter Device name:
ens192
``` 
this is the name of the network interface 
