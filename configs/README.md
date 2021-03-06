## 1. Manual

If you want to deploy the above softwares on CentOS 7, you can follow the steps.

### 1.1 Prerequisite


1.1.1 disable selinux (vi /etc/selinux/config)

```
SELINUX=(enforcing --> disabled)
```

1.1.2 copy all the *.repo you needs to the path ``/etc/yum.repos.d/''

1.1.3 disable firewalld
```
systemctl stop firewalld
systemctl disable firewalld
```

### 1.2 Install Docker

```
yum install docker-ce-18.06*
systemctl start docker 
systemctl enable docker
```

### 1.3 Install Kubernetes

```
yum install kubeadm-1.14.3 kubectl-1.14.3 kubelet-1.14.3  
```

### 1.4 Install kvm （optional）

```
yum install libvirt qemu-kvm qemu-img
```

### 1.5 Install openvswitch （optional）

```
yum install openvswitch-2.11*
systemctl start openvswitch 
systemctl enable openvswitch
```

Next, please see project [pods](../pods) to complete installation.

## 2. Refeences

- https://mirrors.huaweicloud.com/centos-altarch
