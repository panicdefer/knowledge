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
  
### Install Typora in Ubuntu:

- 1. Add Typora Linux repository via command:
  ```
  sudo add-apt-repository 'deb https://typora.io linux/'
  ```

- 2. Setup the key:
  ```
  sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE
  ```
- 3. Finally update and install this simple markdown editor:
  ```
  sudo apt update

  sudo apt install typora
  ```
- 4. And the Typora markdown editor can be removed via command:
  ```
  sudo apt remove typora && sudo apt autoremove
  ```
