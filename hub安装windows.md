>> 官方文档地址:  https://gohugo.io/getting-started/quick-start/
>>
>> 主题网址: https://themes.gohugo.io/



## 下载

- 下载地址 https://github.com/gohugoio/hugo/releases
- 下载版本 hugo_0.76.5_Windows-64bit.zip

## 配置环境变量

- 新建目录 C:\Hugo\bin
- 解压exe放到bin目录
- 添加环境变量 
- win10 进入控制面板搜索环境变量 PATH添加目录   C:\Hugo\bin

- 验证是否成功
    ```
    E:\test>hugo -v
    INFO 2020/10/15 18:03:44 Using config file:
    Start building sites …
    INFO 2020/10/15 18:03:44 syncing static files to E:\test\public\
    
    | EN
    -------------------+-----
    Pages            | 38
    Paginator pages  |  0
    Non-page files   |  0
    Static files     |  7
    Processed images |  0
    Aliases          |  0
    Sitemaps         |  1
    Cleaned          |  0
    
    Total in 300 ms

    ```

## 安装启动网站 
- 进入e盘
- hugo new site test


## 添加主题 

- cd test
- git submodule add https://github.com/RainerChiang/simpleness.git themes/simpleness

- cp -r themes/simpleness/exampleSite/content .

- config.toml 添加 theme = "simpleness"
## 启动
hugo server
```
E:\test>hugo server
Start building sites …

                   | EN
-------------------+-----
  Pages            | 38
  Paginator pages  |  0
  Non-page files   |  0
  Static files     |  7
  Processed images |  0
  Aliases          |  0
  Sitemaps         |  1
  Cleaned          |  0

Built in 65 ms
Watching for changes in E:\test\{archetypes,content,data,layouts,static,themes}
Watching for config changes in E:\test\config.toml
Environment: "development"
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```