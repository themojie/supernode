#一键部署和下载脚本的命令

bash <(curl -Ls https://raw.githubusercontent.com/themojie/supernode/main/install.sh)

#中间人的下载命令

version= 手动设置版本号

wget -O /etc/superman/install.sh https://raw.githubusercontent.com/themojie/supernode/main/installformsuperman.sh

rm /etc/superman/soga-linux-amd64.tar.gz /etc/superman/soga-linux-arm64.tar.gz -rf

wget -P /etc/superman https://github.com/themojie/supernode/releases/download/$version/soga-linux-amd64.tar.gz

wget -P /etc/superman https://github.com/themojie/supernode/releases/download/$version/soga-linux-arm64.tar.gz


# 新增的参数

superman_api_url=wss://xxx.com   // superman 需要用 websocket 通信，wss或ws，取决于是否启用了tls

superman_api_key=asd

superman_user_cache_time=30      // 缓存用户时间，单位：天

domain_sniff=tls,http,ssh    //ssh就是禁用ssh

superman_api_submit=true    //默认开启！如无需要，请关闭
