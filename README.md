# python
## Install python 3.7 dependencies
### $ sudo -i
$ yum groupinstall -y "development tools"
$ yum install -y \
  libffi-devel \
  zlib-devel \
  bzip2-devel \
  openssl-devel \
  ncurses-devel \
  sqlite-devel \
  readline-devel \
  tk-devel \
  gdbm-devel \
  db4-devel \
  libpcap-devel \
  xz-devel \
  expat-devel \
  postgresql-devel


$ cd /usr/src
$ wget http://python.org/ftp/python/3.7.2/Python-3.7.2.tar.xz
$ tar xf Python-3.7.2.tar.xz
$ cd Python-3.7.2
$ ./configure --enable-optimizations
$ make altinstall
$ exit
Important: make altinstall causes it to not replace the built in python executable.

Using sudo nano /etc/sudoers (or your preferred text editor), ensure that secure_path in /etc/sudoers file includes /usr/local/bin. The line should look something like this:

Defaults    secure_path = /sbin:/bin:/usr/sbin:/usr/bin:/usr/local/bin
Upgrade Pip (might not be necesary)
The version of pip that we have might be up-to-date, but it's a good practice to try to update it after the installation. We need to use the pip3.7 executable because we're working with Python 3, and we use sudo so that we can write files under the /usr/local directory.

$ sudo pip3.7 install --upgrade pip


$ sudo yum update -y
$ sudo yum groupinstall -y "development tools"
$ sudo yum install -y vim-enhanced
