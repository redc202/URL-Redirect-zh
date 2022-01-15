# 通过Github实现URL转发
有时，你注册了一个域名，但是你没有搭建服务器。你希望这个域名能指向你的主页/博客/微博等。但是，很多域名注册商不提供这种服务，或者这是一项收费服务。这时你可以使用GitHub来实现这一功能。

第一步，创建一个空的repo，命名为redc202.github.io（刚开始我直接fork，所以没有成功），并把这个repo导入其中(只需要CNAME和index.html两个文件就可以了，内容很短)。

第二步，在你域名的dns中添加如下的`CNAME`记录:（我使用过的是阿里云，新手引导用的A记录，点它左边的添加记录，选择CNAME记录，记录值填上面创建的repo名XXX.github.io）
```
主机名: 按你的需求设置，比如"www"或者“@”
记录值: redc202.github.io.
TTL: 10 分钟
```

第三步，将[CNAME](./CNAME)文件的内容改为你的域名。

第四步， 在[index.html](./index.html)文件中，将URL改为你希望跳转的地址。

这个repo也有[英文版本](https://github.com/y2l/URL-Redirect/)。
