#DHL-BLOG

![pic](https://raw.githubusercontent.com/DHLUI/DHL-Blog-designer/master/short02.jpg)




> Ported Theme of [Kaijun](https://github.com/kaijun/hexo-theme-huxblog/),Thanks him for making this hexo theme.

>The original author of this theme is  [Huxpro](https://github.com/Huxpro),Thanks for his talent.




If you wanna use this theme, you can use the following steps：

#### 1.Init


```
git clone https://github.com/DHLUI/DHL-Blog-designer.git
cd DHL-Blog-designer
npm install
```



#### 2.Modify

Modify _config.yml file with your own info. Especially the section:


```
deploy:
  type: git
  repo: https://github.com/DHLUI/DHL-Blog-designer
  branch: gh-pages    
```

#### 3.Writting/Serve/Deploy


```
hexo new post IMAPOST
hexo clean		//清除缓存文件 (db.json) 和已生成的静态文件 (public)
hexo g			//生成缓存和静态文件
hexo d			//重新部署到服务器
   ```
   
   


Above steps are designed with reference to Kaijun's blog. Big thanks to him!


## License

Apache License 2.0. Copyright (c) 2016-2017 DHL

DHL Blog is derived from [Huxpro](https://github.com/Huxpro/huxpro.github.io)&[Kaijun](https://github.com/kaijun/hexo-theme-huxblog/)
Copyright (c) 2013-2016 Blackrock Digital LLC.


