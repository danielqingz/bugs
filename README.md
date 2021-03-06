# spider——爬虫基础合集
by Jiaqing Zhang

这是一组基础的网络爬虫python脚本，主要基于urllib及webdriver框架，适合初学者，灵活度高。

## Basic Function

### 百度百科中英词对

```
python baike_spider.py
```
用于爬取百度百科中的中外双语名词：中文通过定位head获取，外文通过定位百科中的['外文名', '英文名', '外文名称']等获取，也可修改为任意字符以定位其他元素。

### 东方财报网财报

```
python financial_report_spider.py
```
用于爬取东方财富网的研报,保存PDF到本地：基于webdriver，模拟人工操作网页的行为，不易被反爬虫。

### 医学NER中英双语名词对

```
python medical_corpus_spider.py
```
用于爬取医学NER名词的中英词对。

### Deepl自动翻译

```
python deepl_translator_spider.py input.txt output.txt 1 10000
```
用于自动翻译，并爬取结果保存到本地。

四个参数分别对应，一个`input.txt`文本中有`10000`行待翻译文件，从第`1`行开始翻译，并输出到文件`output.txt`。

注：Deepl的反爬虫机制设置了多次访问会暂时封禁IP地址，因此在脚本中设置了`retry`步骤等待直到IP解封，但若是想跳过等待，可尝试使用VPN等方法切换IP并重启脚本，起始行修改为上次截止位置即可继续爬取。

## Other tips

考虑到网页的更新，本代码中使用的定位Xpath等需自行确认，建议安装chrome插件`ChroPath`进行查看并修改。
