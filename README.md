#MyUbantuSolve
#MyUbantuSolve
#MyUbantuSolve
# MyUbantuSolve
Hello World
This is test
<h1>Ubantu下文件管理器卡死</h1>

`killall nautilus`

<h1>Ubantu下设置clash开机自启</h1>

1.将clash文件移动到/usr/local/bin/clash  </br>

`sudo mv /home/user_name/下载/clash /usr/local/bin`</br>

//将user_name更改为本机</br>
2.bin内出现可执行文件clash</br>
3.此时在端口内输入</br>

`clash`</br>

启动成功则移动成功</br>
4.输入</br>

`gnome-session-properties`

在弹出的选项中点击添加开机启动项，前两行均填入
`clash`
即可。