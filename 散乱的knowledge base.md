# 散乱的[knowledge base](javascript:;)

## HTML5学习

### 1.表格标签

有<table>,<tr>和<td>标签

其中table是表格的意思，而一个tr则代表 表格行（table row），td中则为表格数据（table data），<table>有borber的属性，功能是显示表格的边框，在此标签中一般都有border属性。

![alt 1](https://cdn.itxxb.top/DAODAO%2F%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-07-11%20003412.jpg)

```html
  <table border="1">
    <tr>
        <td>A</td>
        <td>A</td>
        <td>A</td>
    </tr>
    <tr>
        <td>B</td>
        <td>B</td>
        <td>B</td>
    </tr>
  </table>
```



> table的caption 的 属性  



 caption是表格的标题，一般用于table第一个子元素出现

```
<table border="1">
    <caption>一个无名标题</caption>
    <tr>
        <td>A</td>
        <td>A</td>
        <td>A</td>
    </tr>
    <tr>
        <td>B</td>
        <td>B</td>
        <td>B</td>
    </tr>
  </table>
```

![alt 3](https://cdn.itxxb.top/DAODAO%2F%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-07-11%20004529.jpg)

* 还有<th>是‘标题小格’，可以代替<td>使用，表示标题小格。

```
  <table border="1">
    <caption>一个无名标题</caption>
    <tr>
        <th>A</th>
        <th>A</th>
        <th>A</th>
    </tr>
    <tr>
        <td>B</td>
        <td>B</td>
        <td>B</td>
    </tr>
  </table>
```

![alt](C:\Users\daodao\AppData\Roaming\Typora\typora-user-images\image-20220711005146100.png)

## 2.表格的其他特性

> <thead>,<tbody>,<tfoot>标签

* thead为标签的表头

* tbody则是核心内容

* tfoot为定义表脚

## 3.单元格的合并

有着**colspan**和rowspan属性，前者用于设置td/th的列跨度（**向右**），后者用于设置td/th的行跨度，

```
  <table border="1">
    <caption>一个无名标题</caption>
    <tr>
        <th rowspan="2">A</th>
        <th>A</th>
        <th>A</th>
    </tr>
    <tr>
        <td>B</td>
        <td>B</td>
        <td>B</td>
    </tr>
  </table>
```

![alt 1](C:\Users\daodao\AppData\Roaming\Typora\typora-user-images\image-20220711012645268.png)

```
  <table border="1">
    <caption>一个无名标题</caption>
    <tr>
        <th colspan="2">A</th>
        <th>A</th>
        <th>A</th>
    </tr>
    <tr>
        <td>B</td>
        <td>B</td>
        <td>B</td>
    </tr>
  </table>
```

![](https://cdn.itxxb.top/DAODAO%2F%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-07-11%20012747.jpg)

而且可以同时使用：

```
 <table border="1">
    <caption>一个无名标题</caption>
    <tr>    
        <th>A</th>
        <th>A</th>
        <th>A</th>
        <th>A</th> 
    </tr>
    <tr>
        <td>B</td>
        <th rowspan="2">A</th>
        <td colspan="2" rowspan="3">B</td>
    </tr>
    <tr>
        <td>B</td>
    </tr>
    <tr>
        <td>B</td>
        <td>B</td> 
    </tr>
  </table>
```

![](https://cdn.itxxb.top/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202022-07-11%20013830.jpg)

总结：为单元格的合并，表格其他特性