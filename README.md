# classic theme

## 使用说明

### 设置数据源地址

在`_config.yml`中，将`http://i.91wedding.com/sites/classic/data`修改为你自己网站的数据源。

比如，如果你的子域名为forever，那么相应的地址应该为`http://i.91wedding.com/sites/forever/data`

### 设置评论功能

本模板默认使用[友言](http://www.uyan.cc/)评论系统。你需要在友言上面注册帐号，然后将帐号id设置在`_config.yml`的`youyan`字段。

## 高级功能

### 使用disqus评论系统

你也可以选择使用[disqus](http://disqus.com/)评论系统。你可以在disqus上注册帐号，建立站点，并按照其帮助提示在模板中嵌入相关代码。

在本模板中，已经包含有`_includes/disqus.html`。你只需要将`{{site.disqus_shortname}}`替换为你在disqus中建立网站的short name即可。

同时，你需要修改`index.html`，将下面的行：

```
{% include comments.html %}
```

改为：

```
{% include disqus.html %}
```

### 本地编译和调试

如果进行本地的编译和调试，你需要如下知识：

- html/css基本知识
- git的安装和使用
- 安装ruby解释器(在linux和mac系统中默认就带有ruby解释器)

有了上面的基础，先安装本模板使用的一个静态站点生成器Monad:

```
gem install monad
```

安装后，你就可以通过命令`monad serve`来运行站点了。命令`monad build`可以编译站点。
