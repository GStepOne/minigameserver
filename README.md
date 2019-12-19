# 目录结构
~/game/server/
├── xxxxxxxxxxxxxxx.key     域名 ssl 证书，在腾讯云控制台下载
├── xxxxxxxxxxxxxxx.crt     域名 私钥 文件，在腾讯云控制台下载
├── package.json
├── ecosystem.config.js     pm2 配置文件
├── db.js                   数据库
├── config.js               配置文件
├── index.js                入口文件
├── TicTacToe.js            井字大作战游戏逻辑
├── players.js              玩家相关逻辑
└── weapi.js                微信后台接口相关逻辑


复制 nginx 目录下后缀为 key 和 crt 的两个文件进行替换。
完成替换后，打开 config.js 并修改 appid 和 secret 为小游戏的真实值。这俩数据需要自己去申请。
此时执行 npm run dev 或 sudo npm start 即可运行服务器。

# 以开发模式运行（ 8080 端口，不加载证书，需完成下文配置）
npm run dev
# 以正式模式运行（ 443 端口且加载证书，需完成下文配置）
sudo npm start

