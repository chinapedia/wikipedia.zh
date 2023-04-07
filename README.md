# wikipedia.zh

本项目为导出[维基百科](https://www.wikipedia.org/)([镜像](https://wiki.chinapedia.org/))繁体中文内容。

目前用的数据源版本是[20230320](https://dumps.wikimedia.org/zhwiki/20230320/)。由于图片数据量太大，没有直接在Github上显示，而是保留维基百科链接；分类(Category)词条无法获取属于该分类的词条列表，也换成了维基百科的链接。

一些已知问题：

* 部分词条在转换过程中报错，一部分是因为`pandoc`容错率低，一部分因为是维基百科数据的确有语法错误。[liruqi/wikipedia](https://github.com/liruqi/wikipedia)项目在尝试自动规范语法，修复此类报错。
* 链接引用的位置不对，参考文献部分也有大量空白
* pandoc 无法解析 wikitext 模版
* 词条名中包含[Unicode扩展汉字](https://zh.wikipedia.org/wiki/Wikipedia:Unicode%E6%89%A9%E5%B1%95%E6%B1%89%E5%AD%97)时，在macOS上无法保存文件，如[Biángbiáng面](https://zh.wikipedia.org/wiki/%F0%B0%BB%9D%F0%B0%BB%9D%E9%9D%A2)

中文维基百科有若干词条同名，大小写不同，会导致macOS上无法正常checkout文件。因此本项目将停止展示部分冲突词条：
* [DREAMS COME TRUE](https://zh.wikipedia.org/wiki/DREAMS_COME_TRUE)
* [SHOW TIME](https://zh.wikipedia.org/wiki/Talk:SHOW_TIME)

本项目数据由[mediawiki-to-gfm](https://github.com/chinapedia/mediawiki-to-gfm)项目生产：`bash runcjkwp.sh zh`，其中用到的[pandoc](https://github.com/jgm/pandoc)以及其[过滤器](https://github.com/chinapedia/mediawiki-to-gfm/tree/master/filters)还有诸多问题，欢迎提PR改进数据生成工具。

如果你有意见或者建议，欢迎加入Telegram讨论群[Chinapedia](https://t.me/chinapedia)。
