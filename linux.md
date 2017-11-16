### CentOS7 配置阿里云yum源
- 1）下载repo文件
  ```
  wget http://mirrors.aliyun.com/repo/Centos-7.repo
  ```
- 2）备份并替换系统的repo文件
  ```
  cp Centos-7.repo /etc/yum.repos.d/
  cd /etc/yum.repos.d/
  mv CentOS-Base.repo CentOS-Base.repo.bak
  mv Centos-7.repo CentOS-Base.repo
  ```
- 3）执行yum源更新命令
  ```
  yum clean all
  yum makecache
  yum update
  ```
