# Firewalld

```
# 查看防火墙是否开启
systemctl status firewalld

# 若没有开启则是开启状态
systemctl start firewalld  关闭则start改为stop

# 查看已经开放的端口：
firewall-cmd --list-ports

# 开放端口
firewall-cmd --add-port=80/tcp --permanent
	--zone #作用域 
	--add-port=80/tcp #添加端口，格式为：端口/通讯协议    
	--permanent #永久生效，没有此参数重启后失效

# 重启防火墙:
systemctl reload firewalld
firewall-cmd --reload

## 其他常用命令：
# 查看防火墙状态，是否是running
firewall-cmd --state

# 重新载入配置，比如添加规则之后，需要执行此命令
firewall-cmd --reload

# 列出支持的zone
firewall-cmd --get-zones

# 列出支持的服务，在列表中的服务是放行的
firewall-cmd --get-services

# 查看ftp服务是否支持，返回yes或者no
firewall-cmd --query-service ftp

# 临时开放ftp服务
firewall-cmd --add-service=ftp

# 永久开放ftp服务
firewall-cmd --add-service=ftp --permanent

# 永久移除ftp服务
firewall-cmd --remove-service=ftp --permanent

# 永久添加80端口 
firewall-cmd --add-port=80/tcp --permanent

# 永久移除80端口 
firewall-cmd --remove-port=80/tcp --permanent

# 查看已开放的端口
firewall-cmd --zone=public --list-ports
```

