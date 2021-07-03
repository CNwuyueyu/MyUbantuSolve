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

`sudo gedit /etc/systemd/system/clash.service`</br>

打开编辑器</br>
输入</br>



```
[Unit]

Description=clash service

After=network.target

[Service]

Type=simple

User=root

ExecStart=/usr/local/bin/clash

Restart=on-failure # or always, on-abort, etc

 

[Install]

WantedBy=multi-user.target
```


5.保存</br>
6.在端口内输入</br>
`systemctl daemon-reload`</br>
 输入用户密码</br>
        `systemctl enable clash`</br>
        输入用户密码</br>
        终端提示：Created symlink /etc/systemd/system/multi-user.target.wants/clash.service → /etc/systemd/system/clash.service.</br>
        则启动项设置成功。</br>



附：</br>
`service clash start`# 启动</br>
`service clash stop` # 停止</br>
`service clash restart `# 重启</br>
`service clash status`# 状态
