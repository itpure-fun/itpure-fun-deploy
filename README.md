# ITPURE-FUN部署工具

## 环境

- PHP >= 8.1
- Swoole >= 5.0并关闭`Short Name`
- Node(推荐20.0)
- Mysql >= 5.7

## 安装

1. 下载部署工具代码

```shell
# 下载代码
git clone https://github.com/itpure-fun/itpure-fun-deploy.git

# 进入目录
cd ./itpure-fun-deploy
```

2. 下载前后端代码

```shell
# 后端
git clone https://github.com/itpure-fun/itpure-fun.git

# 前端
git clone https://github.com/itpure-fun/front-local.git
```

3. 后端配置

```shell
# 进入后端目录
cd ./itpure-fun

# 创建和配置`.env`, 没有特殊设置可以不用修改
cp .env.example .env

# 安装composer包
comopser install -vvv
```

4. 安装

```shell
# 返回部署工具项目根目录下,即上级目录
cd ..

# 执行
docker-compose up -d nginx hyperf node mysql redis
```

> 注意：构建过程需要几分钟，如遇到访问`500`稍等一会儿即可访问

4. 访问

> 前台：http://localhost/

> 后台：http://localhost/admin
  