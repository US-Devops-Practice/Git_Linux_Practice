yum update -y
hostnamectl set-hostname namehere
exec bash
yum install vim wget tar make unzip -y
yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel -y
yum install gcc perl-ExtUtils-MakeMaker -y
cd /opt
wget https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.45.2.tar.gz
tar -xvf git-2.45.2.tar.gz
cd git-2.45.2
make prefix=/usr/local/git all
make prefix=/usr/local/git install

vim ~/.bashrc

#insert the next line inside the file
export PATH=$PATH:/usr/local/git/bin (temporary path, after reboot the git version will nit appear)
save and close the file :wq 

git --version
yum remove git -y
git --version
hash -r
git --version

git --version

source ~/.bashrc 
git --version
