# POMP舆论分析面板

>POMP!砰！（POMP=Public Opinion Monitoring System）

**请注意，使用此面板请遵守相关法律，禁止违法行为，如有违法与作者无关！**  
**使用此代码，即代表您已同意上述规则。**

## 这是什么？

简而言之，这是一个可以轻松掌握**微博**方面的舆论动向的面板。你可以在上面浏览数据，对数据评级，一键更改爬虫模式，所有的这一切，都将在POMP中一站式轻松知晓。

## 我怎么用它？

### 使用方法

1. 下载源码并解压文件。
2. 在目标主机上创建一个**随意命名**的数据库。
3. （*可选*）创建一个自定义名称和密码的账号，账号必须**对该数据库有所有权限**（`ALL PRIVILEGES`）。
4. 或者也可使用root账号，**牢记使用账号的密码**。
5. 将目录下的`Structure.sql`导入该数据库，这将创建几个表。
6. 用任意文本编辑器打开`config.php`，并参照下表进行配置：

    |行|解释|建议配置|
    |:--|:--:|:--|
    |11（`username`）|面板账号|随意配置，不建议初始值|
    |12（`password`）|面板密码|随意配置，不建议初始值|
    |16（`dtbs_name`）|数据库主机|填写IP或`127.0.0.1/localhost`|
    |17（`dtbs_usrname`）|数据库账号|填写新增的数据库账号（不建议root）|
    |18（`dtbs_pswd`）|数据库密码|填写新增账号的密码或者root密码|
    |19（`dtbs_dtbs`）|数据库名|填写你刚刚创建的数据库名|

7. 将文件全部上传到主机中网站文件夹，它类似`www/wwwroot/a.test.com`（服务器请放行对应数据库连接端口，一般为`3306`），访问对应地址，看到“面板登录”即部署成功。

### 使用问题

+ 显示“登录失败（有参数填写错误）”？  
请先检查您的账号和密码输入是否正确，如果忘记了可在`config.php`进行更改。
+ 显示“连接数据库失败“？  
请检查您的config.php是否正确填写，以及主机是否开放对应端口，账号是否开放任意主机登录等。
+ 初始密码是什么？  
请于`config.php`内查看。

### 关于评级

|等级|状态|
|:---|:---:|
|0|*未定义*|
|1|特别轻（没有影响力）|
|2|尤其轻（影响力忽略不计）|
|3|比较轻（影响力很少）|
|4|有点轻（影响力较少）|
|5|一般（影响力一般）|
|6|有点重（影响力较多）|
|7|比较重（影响力很多）|
|8|尤其重（影响力特别多）|
|9|特别重（影响力是**爆炸性的**）|

遇到问题？请发issue（随缘修复），如果你有能力，可以自己动手改一改发pr。
