# openwrt-编译 使用日常备忘录
选择好勾选需要编译的软件后，</br>
可以手动在lede根目录下创建dl文件夹，</br>
然后从github等其他地方下载，别人已经打包好的dl文件，</br>
或者是自己原先编译的dl文件夹，</br>

例如https://zhuanlan.zhihu.com/p/24403803</br>
但是上面这个地址是对整个源码文件夹进行提升权限，</br>

我们可以在lede上面一层文件夹输入：</br>
sudo chmod -R 777 lede</br>

也可以试试在lede目录下输入：</br>
sudo chmod -R 777 dl</br>

6.6内核编译不成功的时候，</br>
有时候别着急去github里问，</br>
先试着切换到6.1内核，</br>
切换内核的操作，晚些时候再补充，</br>

编译adguardhome，从系统进入后，</br>
先关闭dnsmasq并关闭开机启动，</br>
然后在页面段切换到编译adguardhome</br>

下图几个要点：</br>
1. 如果没核心版本号，且上面已经关闭了dnsmasq，</br>
要点击【网络】-【接口】-【LAN】-【高级设置】-【使用自定义的 DNS 服务器】中，输入8.8.8.8，保存</br>
然后再点击更新内核，基本上可以更新上了。</br>
2.重定向：我选择让adguardhome使用53端口，docker中的paopaodns占用54端口</br>
3.要给/usr/share/AdGuardHome目录修改权限，</br>
不然开启adguardhome，也会出现没有统计数据的情况</br>
chmod +x /usr/share/AdGuardHome/addhost.sh</br>
chmod +x /usr/share/AdGuardHome/</br>
我输入的是上面两条，然后重启AdGuardHome
![image](https://github.com/user-attachments/assets/f81d8663-aeaa-45f1-8b25-b0bdfe093ef0)

