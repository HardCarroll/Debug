# Debug
## 2018/12/17
### 一、初识markdown
> 1. 文本强调语法：
> > - 文本倾斜语法：\*要倾斜的文本\* 效果展示： *倾斜的文本*
> > - 文本加粗语法：\*\*要加粗的文本\*\* 效果展示：**加粗的文本**
> > - 文本删除线：\~\~带删除线的文本\~\~ 效果展示：~~删除线文本~~
> 2. 链接，行内式和参数式
> > - 行内式写法：\[我是链接文本\](https://www.webserv.cn "链接title说明") 效果展示：[我是链接文本](https://www.webserv.cn "链接title说明")
> > - 参数式写法：   
      \[param1\]: &lt;https://www.baidu.com&gt; "title文本"   
      \[param2\]: &lt;https://www.qq.com&gt; "title文本"   
      这是参数式的写法示例,就是把链接当成参数,适合多处使用相同链接的场景,这里是[param1],这里是[param2]
> 3. 图片，和链接写法差不多，需要在方括号前加上!，示例：!\[图片文本\](https://webserv.cn/favicon.ico "title属性")   
    效果展示：![图片文本](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1545029079389&di=b56756011ac014df29670290bff9c059&imgtype=0&src=http%3A%2F%2Ffscomps.fotosearch.com%2Fcompc%2FCSP%2FCSP703%2Fk40308705.jpg "title提示")
> 4. 代码块
> > - 单行：\`我是单行代码\`
> > - 多行：   
      \`\`\` 注释语句   
      第一行代码   
      第二行代码   
      第三行代码   
      ...   
      \`\`\`   
      效果展示：   
      `我是单行代码`   
> > ``` 多行代码注释语句
> > echo "hello world";
> > printf("hello world");
> > cout << "hello world" << endl;
> > ```
> 5. 表格
> > head：\|col1\|col2\|col3\|   
> > align：\|:--:\|:--\|--:\|,分别为居中对齐，左对齐和右对齐   
> > body：\|row1\|row1\|row1\|   
> > body：\|row2\|row2\|row2\|   
> > body：\|row3\|row3\|row3\|   
> > 效果展示：

|name|age|sex|
|:--:|:--|--:|
|jack|20|male|
|rose|18|female|


[param1]: <https://www.baidu.com> "title文本"
[param2]: <https://www.baidu.com> "title文本"

### 二、ubuntu以root身份远程ssh登录
> 1. 查看是否已安装ssh模块
> > ps -e|grep ssh
> 2. 安装open-ssh模块，开启远程登录
> > apt-get install openssh-server
> 3. 修改sshd_config文件
> > vi /etc/ssh/sshd_config   
    找到并注释掉这行：PermitRootLogin prohibit-password   
    新建一行：PermitRootLogin yes
> 4. 重启ssh服务
> > service ssh restart
