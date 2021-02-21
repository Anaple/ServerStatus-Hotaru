# ServerStatus
云探针、多服务器探针、云监控、多服务器云监控

本分支基于ServerStatus-Hotaru最新版本重写前端！！后端内容几乎没动！！！。


For commercial use, please replace the images.

若本仓库用到的一些素材侵犯了您的版权，请联系我处理，谢谢。

If some of the assets used in this repo infringe your copyright, please contact me, thanks.

## 特性

前端基于 React17 和 Ant design制作


客户端支持Python版本：Python2.7 - Python3.7



服务端：

```bash
wget https://raw.githubusercontent.com/Anaple/ServerStatus-Hotaru/master/status.sh
bash status.sh s
```

客户端：

```
bash status.sh c
```

## 修改方法

如果你使用Toyo版本或原版本，请备份你的config文件并重新编译安装本版本服务端

配置文件：/usr/local/ServerStatus/server/config.json备份并自行添加Region

```json
{
   "username": "Name",
   "password": "Password",
   "name": "Your Servername",
   "type": "KVM",
   "host": "None",
   "location": "洛杉矶",
   "disabled": false,
   "region": "US"
  },
```

替换配置文件，重启ServerStatus

## 手动安装服务端

```
apt install wget unzip curl make build-essential
wget https://github.com/Anaple/ServerStatus-Hotaru/archive/master.zip
unzip master.zip
cd /root/ServerStatus-Hotaru-master/server
make #手动编译生成二进制文件
chmod +x sergate
vim config.json #修改配置文件
cp -r ../web/* /home/wwwroot/public #此为站点根目录，请自行设置
./sergate --config=config.json --web-dir=/home/wwwroot/public
```

## Psutil版

使用Psutil版即可使ServerStatus客户端在Windows等平台运行

```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py ::若未安装pip
python get-pip.py
python pip install psutil
%修改status-psutil.py%
python status-psutil.py
```

Linux：

```
apt install python3 python3-pip wget
pip3 install psutil
wget https://raw.githubusercontent.com/Anaple/ServerStatus-Hotaru/master/clients/status-psutil.py
vim status-psutil.py #修改客户端配置文件
python3 status-psutil.py
```



## 相关开源项目 ： 
* ServerStatus-Hotaru: https://github.com/CokeMine/ServerStatus-Hotaru
* ServerStatus-Toyo：https://github.com/ToyoDAdoubiBackup/ServerStatus-Toyo
* ServerStatus：https://github.com/BotoX/ServerStatus
* mojeda's ServerStatus: https://github.com/mojeda/ServerStatus
* BlueVM's project: http://www.lowendtalk.com/discussion/comment/169690#Comment_169690
