# linux 自己參考用


//查看系統時間

date

//修改系統時區

ln -sf /usr/share/zoneinfo/Asia/Taipei /etc/localtime

//nginx

systemctl enable nginx


# port

netstat -lptu

netstat -tulpn



sed -i "s/.*PasswordAuthentication.*/PasswordAuthentication no/g" /etc/ssh/sshd_config

sed -i "s/#*PasswordAuthentication.*/PasswordAuthentication no/g" /etc/ssh/sshd_config

sed -i "s/#*UsePAM.*/UsePAM no/g" /etc/ssh/sshd_config



https://dotblogs.com.tw/Echo/2017/06/28/Linux_AuthorizedKeys_Setting


find . -type f -print0 | xargs -0 dos2unix

# 清 30 天前log
find /opt/soft/log/ -mtime +30 -name "*.log" -exec rm -rf {} /;
