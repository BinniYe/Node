# Markdown学习笔记

markdown编辑器推荐两款：Atom[Github出品，开源]、Typora[目前免费]

## 基础功能

| 功能     | 效果                               | 语法                              |
| -------- | ---------------------------------- | --------------------------------- |
| 粗体     | **粗体**                           | 两边+**                           |
| 斜体     | _斜体_                             | 两边+_                            |
| 中划线   | ~~中划线~~                         | 两边+~~                           |
| 插入图片 | ![Image](url.pic)                  | [] 中间为占位符,() 中间为图片链接 |
| 单行代码 | `Log.i(TAG, "Hello!")`             | 两边+`                            |
| 多行代码 | ```java```                         | 两边+```                          |
| 链接     | [百度首页](https://www.baidu.com/) | [] 中间为显示文字,() 中间为链接   |
| 标题     | # ... ######                       | #+空格，6级                       |
| 有序列表 | 1.                                 | 数字 + . + 空格                   |
| 无序列表 | *                                  | * + 空格                          |
| 子项目   | tab*                               | tab + * + 空格                    |

## 示例

### 插入图片

[Image](https://image.baidu.com/search/detail?ct=503316480&z=0&ipn=d&word=markdown%E6%8F%92%E5%85%A5%E4%BB%A3%E7%A0%81%E5%9D%97&step_word=&hs=0&pn=2&spn=0&di=72160&pi=0&rn=1&tn=baiduimagedetail&is=0%2C0&istype=0&ie=utf-8&oe=utf-8&in=&cl=2&lm=-1&st=undefined&cs=835515464%2C3282062703&os=1358243294%2C3496893917&simid=4090754704%2C727062967&adpicid=0&lpn=0&ln=1548&fr=&fmq=1617426861294_R&fm=&ic=undefined&s=undefined&hd=undefined&latest=undefined&copyright=undefined&se=&sme=&tab=0&width=undefined&height=undefined&face=undefined&ist=&jit=&cg=&bdtype=0&oriquery=&objurl=https%3A%2F%2Fgimg2.baidu.com%2Fimage_search%2Fsrc%3Dhttp%3A%2F%2Fs2.sinaimg.cn%2Fmw690%2F004igrvszy75I1hBOk9f1%26690%26refer%3Dhttp%3A%2F%2Fs2.sinaimg.cn%26app%3D2002%26size%3Df9999%2C10000%26q%3Da80%26n%3D0%26g%3D0n%26fmt%3Djpeg%3Fsec%3D1620018879%26t%3D1c884eac4dc601a2b531f36d2dcb984b&fromurl=ippr_z2C%24qAzdH3FAzdH3Fks52_z%26e3Bftgw_z%26e3Bv54_z%26e3BvgAzdH3FfAzdH3Fks52_jwbdb1dwa8ado1go_z%26e3Bip4s&gsm=3&rpstart=0&rpnum=0&islist=&querylist=&force=undefined)

### 插入单行代码

`Log.i(TAG, "Hello markdown~")`

### 插入代码块

```java
if (status == 0) {
    Log.i(TAG, "success!");
} else {
    Log.i(TAG, "fail!");
}
```

### 插入链接

[百度首页](https://image.baidu.com/)

### 有序列表

1. 有序列表1
2. 有序列表2
3. 有序列表3

### 无序列表

* 无序列表1
* 无序列表2
* 无序列表3

### 子项目列表

1. 项目1
   1. 子项目1
   2. 子项目2
   3. 子项目3
2. 项目2
   1. 子项目1
   2. 子项目2
3. 项目3

