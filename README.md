## 私聊 Telegram Bot 的 Python 实现

### Git
```
sudo apt install --upgrade git -y
```

### Clone
```
cd /var/lib && git clone https://github.com/ThekingMX1998/PM-Forward-Bot.git PMFB && cd PMFB
```

### Pip
``` 
sudo apt install python3-pip -y
```

### 安装依赖
```
pip3 install -r requirements.txt
```

### 填写变量
```
vi config.json
```
<code>TOKEN</code> 处填入自己的 <code>botToken</code> ，可以去 [@BotFather](https://t.me/BotFather) 处获取

<code>ADMIN</code> 处填入自己的 <code>userid</code> ，可以去 [@userinfobot](https://t.me/userinfobot) 处获取

### 启动！！！
```
python3 main.py
```

### 进程守护
```
cat <<'TEXT' > /etc/systemd/system/PMFB.service
[Unit]
Description=A telegram pm foward bot by GreenFish
After=network.target

[Install]
WantedBy=multi-user.target

[Service]
Type=simple
WorkingDirectory=/var/lib/PMFB
ExecStart=/usr/bin/python3 main.py
Restart=always
TEXT
```

启动程序：`systemctl start PMFB`

设置为开机自启：`systemctl enable PMFB`

停止程序：`systemctl stop PMFB`


Bot 演示 : [@chenjranyang_bot](https://t.me/chenjranyang_bot)
