# About
这个仓库是网上看到的一些前端的小技巧的实践集合
## 1. H5 唤起本地app
通过url scheme 唤起本地app
常用的 URL scheme  
https://github.com/dzlixu/Inbox.git doc/1.md
demo:
https://github.com/dzlixu/Inbox.git src/1.html

## 你写的 height:100% 不起作用
Web浏览器在计算有效宽度时会考虑浏览器窗口的打开宽度。我们不设置宽，会自动填满整个横向宽度.
但是高度的计算方式完全不一样。事实上，浏览器根本就不计算内容的高度，除非内容超出了视窗范围(导致滚动条出现)。或者你给整个页面设置一个绝对高度。否则，浏览器就会简单的让内容往下堆砌，页面的高度根本就无需考虑。

因为页面并没有缺省的高度值，所以，当你让一个元素的高度设定为百分比高度时，无法根据获取父元素的高度，也就无法计算自己的高度。

即父元素的高度只是一个缺省值：height: auto;我们设置height：100%时，是要求浏览器根据这样一个缺省值来计算百分比高度时，只能得到undefined的结果。也就是一个null值，浏览器不会对这个值有任何的反应。

demo:
https://github.com/dzlixu/Inbox.git src/2.html

