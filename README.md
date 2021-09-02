# DOM对象风格封装
也叫命名空间风格
window.dom是我们提供的全局对象
封装包括了增删改查四个方面
例如下一个就是封装用来创建节点
```javascript
window.dom = {
    create(string) {
        const container = document.createElement("template");
        container.innerHTML = string.trim();
        return container.content.firstChild;
    }
};
```
1. template可以容纳任何标签，作为容器。
2. string.trim();是为了去除字符串两端的空格。
可以通过以下方式调用
```javascript
const div = dom.create('<div><span></span></div>');
```
* 一个小技巧
git rm --cached -r 

