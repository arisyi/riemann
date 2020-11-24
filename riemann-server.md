```yum install bash-completion wget jre bzip2 gcc```
```source /etc/profile.d/bash_completion.sh```
```wget https://github.com/riemann/riemann/releases/download/0.3.6/riemann-0.3.6.tar.bz2```
```tar xjvf riemann-0.3.6.tar.bz2```


```yum -y install centos-release-scl-rh centos-release-scl```
```yum --enablerepo=centos-sclo-rh -y install rh-ruby27 rh-ruby27-ruby-devel```
```scl enable rh-ruby27 bash```

```vi /etc/profile.d/rh-ruby27.sh
    source /opt/rh/rh-ruby27/enable
    export X_SCLS="`scl enable rh-ruby27 'echo $X_SCLS'`"```

```gem install riemann-client riemann-tools riemann-dash```
