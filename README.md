#MyUbantuSolve
#MyUbantuSolve
#MyUbantuSolve
# MyUbantuSolve
Hello World
This is test
<h1>Ubantu下文件管理器卡死</h1>
·killall nautilus
<h1>Ubantu下设置clash开机自启</h1>
    1.将clash文件移动到/usr/local/bin/clash
         sudo mv /home/user_name/下载/clash /usr/local/bin
         //将user_name更改为本机
    2.bin内出现可执行文件clash
    3.此时在端口内输入
        clash
        启动成功则移动成功
    4.输入
        sudo gedit /etc/systemd/system/clash.service
        打开编辑器
        输入
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


        5.保存
        6.在端口内输入
        systemctl daemon-reload
        输入用户密码
        systemctl enable clash
        输入用户密码
        终端提示：Created symlink /etc/systemd/system/multi-user.target.wants/clash.service → /etc/systemd/system/clash.service.
        则启动项设置成功。
附：
service clash start # 启动
service clash stop # 停止
service clash restart # 重启
service clash status # 状态
