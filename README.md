# sub-web-modify
[本项目](https://suburl.v1.mk)重制[原项目](https://github.com/CareyWang/sub-web)CSS样式，兼容nodejs最新版本（可直接一键部署至Vercel），解决大部分布局细节问题，增加“暗黑模式”，默认自动切换亮/暗模式（点击“太阳/月亮”图标可手动切换），增加“高级功能”点击显示/隐藏，添加短链接选择/自定义功能，增加近百条远程配置，新增[sub-web聚合API](https://github.com/youshandefeiyang/sub-web-api)，增加从短链接中获取订阅信息并返回至前端界面，增加上传自定义远程配置/JS进阶排序节点/JS进阶筛选节点等功能，感兴趣的朋友可以自建API服务，增加URL传参设置自定义后端<br/>
## 效果预览：
![avatar](https://raw.githubusercontent.com/youshandefeiyang/webcdn/main/sub-web-modify.GIF)
### 使用方法：
#### Docker构建、部署:
构建镜像：
```shell
git clone https://github.com/yhl452493373/sub-web-modify.git
cd sub-web-modify
docker build -t youshandefeiyang/sub-web-modify:latest .
```
运行：
```shell
docker run -d --restart unless-stopped --privileged=true -p 25550:80 --name sub-web-modify youshandefeiyang/sub-web-modify
```
#### Docker Compose一键启动
先在docker-compose.yml中，将端口改为自己需要的端口。默认情况下为25550，然后执行下面命令
```shell
sudo docker-compose up -d
```
访问地址举例:
```
http://192.168.10.1:25550/?backend=http://nps.yanghuanglin.cn:25500
```
