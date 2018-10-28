###File Browser配置教程
![图1](https://blog.e9china.net/wp-content/uploads/2018/10/1-2-1024x1012.jpg)  ![图2](https://blog.e9china.net/wp-content/uploads/2018/10/2-1.jpg)
####1. 安装说明

    curl -fsSL https://filebrowser.github.io/get.sh |
      
####2. 配置文件
#####创建配置目录
    mkdir /etc/filemanager

#####创建网盘目录

    mkdir /home/data

#####下载配置文件

    wget -O /etc/filemanager/config.json https://blog.e9china.net/ssh/filemanager-config.json

####3. 运行命令
#####测试能不能允许
    filebrowser -c /etc/filemanager/config.json

#####后台运行命令

    nohup filebrowser -c /etc/filemanager/config.json >/dev/null 2>&1 &

#####管理密码
> user:admin  
> pass:admin

####4.配置rclone来链接网络硬盘
[利用Google Drive的无限网盘做数据定时备份](https://blog.e9china.net/lesson/liyonggoogledrivedewuxianwangpanzuoshujudingshibeifen.html)  
仔细看这篇文章,我们就不在这里细说教程了   
配置好rclone,然后我们在编辑File Browser的配置文件,把目录指向那个文件夹  
>vi /etc/filemanager/config.json  
>"scope":"/home/data", #找到这个修改成你网盘挂载的目录

####5.配置关于命令
我们这里就不复制粘贴官方的说明自己去看吧!  [filebrowser.github.io](https://filebrowser.github.io/)

####6.另外一种配置
本站战略合作炮友:[芳姐](https://www.xiaofengsky.com/)给我们提供了OneDrive的办法[Aria2+Aria2Ng+OneIndex一键安装脚本,离线下载自动上传至OneDrive](https://www.xiaofengsky.com/82975.html)
