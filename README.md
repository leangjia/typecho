高性能typecho下载
作者：雷鬼 • 2017-01-27
在入门级服务器上面测试（1G内存1核CPU），typecho大概可以支持30w左右的post，多于30w将出现明显的性能问题。
为此，本站开发者们，在typecho的基础上，优化了部分数据层的逻辑，将数据量（post数）提升到200w以上。

项目目的
由于Typecho是一个用于个人的博客系统，所以其设计之初就不支持过大的数据量。但最近不少朋友向我求助，希望用typecho来搭建数据量较大的商业网站（譬如外贸公司），于是将最近几个网站的优化策略，汇总在此HPTypecho（High Performance Typecho）中。

声明
HPTypecho在Typecho的基础上修改,原则上会尽可能兼容typecho原有的插件和模板。但在实际开发过程中，会通过修改表结构或者程序逻辑来提高性能，所以可能出现部分插件无法兼容的情况。

在表数据量较大的情况下，MySQL表可能会容易损坏，尤其是MyISAM引擎。这不是Typecho代码可以避免的，所以在使用HPTypecho的时候，谨记积极备份数据。

版本更新
v1.0-16.11.23-beta2 发布

修复tag查询时sql语句错误的bug
修复sitemap生成插件，域名错误的bug
下载地址：https://github.com/leimiu/typecho/releases/tag/v1.0-16.11.23-beta2
部署帮助：https://www.typechodev.com/index.php/archives/707/
v1.0-16.09.25-beta 发布

修复v0.9为优化翻页性能引入的bug
添加高性能基础插件：高性能sitemap插件、静态页面高速缓存插件、文章导入插件。
其他优化
下载地址：https://github.com/leimiu/typecho/archive/v1.0-16.09.25-beta.zip
部署帮助：https://www.typechodev.com/index.php/archives/707/
v0.9-16.09.04 发布

关掉按时间归档。此特性会全表扫描，性能太差
优化排序逻辑，改成按id排序，避免按时间排序存在性能问题以及乱序问题
优化翻页。翻页时删除offset查询，改用cid判断，副作用是翻页可能不正确。
下载地址：https://github.com/leimiu/typecho/archive/v0.9-16.09.04.zip
2016-07-16更新typecho到hptyecho的转换脚本

git克隆最新代码 https://github.com/leimiu/typecho
进入tools/update2hp目录，根据README.txt的说明，配置脚本并进行数据转换
v0.8-16.03.15-beta，测试版

建议配置：以200w post为标准，建议主机1G以上内存，50G以上硬盘。
优化分类加载的性能
优化搜索性能，注意目前仅支持英文搜索，暂不支持中文
优化post页加载性能
优化后台性能
请不要将测试版用于生产环境。性能测试报告整理好后再链出来
beta版试用地址：https://github.com/leimiu/typecho/archive/v0.8-16.03.15-beta.zip

版权声明:未经书面授权禁止转载、摘编、复制或建立镜像。对既成事实本站将保留所有的权利。

@TypechoDev


Typecho Blogging Platform
=========================

Typecho is a PHP Blogging Platform. Simple and Powerful.

#### Homepage
http://typecho.org/

#### Documents
http://docs.typecho.org/

#### Community
http://forum.typecho.org/

#### Download
http://typecho.org/download
