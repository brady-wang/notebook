

# 安装
- 安装
	- curl -sS https://getcomposer.org/installer | php
	- mv composer.phar /usr/local/bin/composer 
---



# 常见命令

1. 更新composer自身

   ``composer self-updat``

2. 更新composer 并查看更新过程

   ``composer update -vvv``
   
3. composer 更改为国际源

   `composer config -g repo.packagist composer https://repo.packagist.org`

4. composer设置阿里云镜像

   `composer config -g repo.packagist composer https://mirrors.aliyun.com/composer `

5. comopose单个项目设置镜像源

   修改composer.json 添加最后一个 阿里云镜像

   ```json
   "repositories": {
       "0": {
         "type": "composer",
         "url": "http://composer.diangoumall.com:8882"
       },
       "1": {
         "type": "git",
         "url": "http://gitlab.diangoumall.com:8881/business/dg-rpc.git"
       },
       "packagist": {
         "type": "composer",
         "url": "https://mirrors.aliyun.com/composer/"
       }
     }
   ```

---



# 报错 

1. `Failed to decode response: zlib_decode(): data error`

	`解决方案: composer diagnose`

	[原文地址](https://www.cnblogs.com/cxscode/p/7003756.html)


