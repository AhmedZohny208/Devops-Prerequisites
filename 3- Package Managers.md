# Package Managers
Help you install various software on the linux system

When you go through devOps and cloud courses, you will install various softwares such as web servers, database servers etc. and most of these are installed using package managers

"Centos" uses an RPM based package manager

## RPM (Red Hat Package Manager)
a software is packaged into a bundle with the extension .rpm

#### Install Package
```bash
rpm -i telnet.rpm
```

#### Uninstall Package
```bash
rpm -e telnet.rpm
```

#### Query Package
Get details about the installed package
```bash
rpm -q telnet.rpm
```

So RPM requires you to point to the exact location where the RPM package is available. It does not care about any dependencies that this package may have.

So we need a solution that can query the package, find it's location and install all dependencies as well as the package it self.

## YUM
Is high level package manager that uses RPM underneath
```bash
yum install ansible
```
This command will install ansible and all of its dependent packages

#### To see a list of repositaries available on the system
```bash
yum repolist
```

```bash
ls /etc/yum.repos.d/
```

```bash
cat /etc/yum.repos.d/CentOS-Base.repo
```

#### To see a list of available packages
```bash
yum list ansible
```

#### To remove a package
```bash
yum remove ansible
```

#### To see all available version of a package
```bash
yum --showduplicates list ansible
```

#### To install a specific version of a package
```bash
yum install ansible-2.4.2.0
```