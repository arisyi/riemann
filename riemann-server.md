Install dependency
>yum install bash-completion wget jre bzip2 gcc

Enable Auto Completion
>source /etc/profile.d/bash_completion.sh

Download Riemann Server
>wget https://github.com/riemann/riemann/releases/download/0.3.6/riemann-0.3.6.tar.bz2

Export the binary
>tar xjvf riemann-0.3.6.tar.bz2

Install repository for Ruby 2.7
>yum -y install centos-release-scl-rh centos-release-scl

Install Ruby 2.7
>yum --enablerepo=centos-sclo-rh -y install rh-ruby27 rh-ruby27-ruby-devel

Enable Ruby
>scl enable rh-ruby27 bash

Permanent 
>vi /etc/profile.d/rh-ruby27.sh>
>    source /opt/rh/rh-ruby27/enable>
    export X_SCLS="`scl enable rh-ruby27 'echo $X_SCLS'`"

Install Riemann-Tools
```gem install riemann-client riemann-tools riemann-dash```
