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

编译adguardhome，从系统进入后，
先关闭dnsmasq并关闭开机启动，
