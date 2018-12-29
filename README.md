# shell-scripts
Linux Shell Scripts

#一键安装 BBR

## 安装
wget https://github.com/qian-jiahong/shell-scripts/blob/master/ovz-bbr/ovz-bbr-installer.sh
chmod +x ovz-bbr-installer.sh
./ovz-bbr-installer.sh

## 卸载
./ovz-bbr-installer.sh uninstall

## 多端口加速
安装的时候只配置了一个加速端口，但是你可以配置多端口加速，配置方法非常简单。 修改文件

    vi /usr/local/haproxy-lkl/etc/port-rules

在文件里添加需要加速的端口，每行一条，可以配置单个端口或者端口范围，以 # 开头的行将被忽略。 例如：8800 或者 8800-8810 配置完成之后，只需要重启 haproxy-lkl 即可。

## 判断 BBR 已正常工作

判断 bbr 是否正常启动可以尝试 ping 10.0.0.2，如果能通，说明 bbr 已经启动。
