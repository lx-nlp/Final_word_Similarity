## 词语相似度高级版
综合词林扩展版与知网Hownet的相似度计算思想与策略，来自以下论文，代码为本人自己实现。
> 《基于知网与词林的词语语义相似度计算》朱新华,马润聪,孙 柳,陈宏朝,2016年7月《中文信息学报》</br>

采用混合计算方式，扩大了词汇覆盖面，也一定程度上改进了计算结果的合理性。不过该论文中改进知网方法因水平所限本人未能实现。本方法皮尔逊相关性系数为0.86，与参考论文中结果还有些差距。</br>
**具体算法的选择**：</br>
+ 词林扩展版</br>
（1）最初采用了[【词林相似度计算：参照3篇论文实现了3种算法】](https://github.com/ashengtx/CilinSimilarity)
中的2016版代码（文献1）。
（2）后来查阅文献发现作者团队发布了更新的计算方法，取得了更好的结果。于是按文献2进行实现。经检验，单纯词林扩展版的相似度计算，皮尔逊系数从0.7924提高0.8165。
> 《基于路径与深度的同义词词林词语相似度计算》陈宏朝, 李飞, 朱新华,马润聪. 2016年9月《中文信息学报》</br>

+ 知网Hownet</br>
（1）开源的代码有几款，但多数效果与主观感受有差距，且缺乏论文数据对照。表现稳定是:[【知网相似度计算】：基于刘群等人2002年论文。](https://github.com/240400968/hownet-similarity)</br>
（2）本人修改了其中读取词表遗漏的bug，改善了代码的风格，提高了可读性。

本系统所用的两个同义词/概念库：

|            |同义词词林| 知网 |二者并集|二者交集|
|------------|---------|------|------|------|
| 词汇量  | 77456| 53336| 85777|45015|

如果你想看看预训练词向量方式计算的中文词语相关度，可以参见：[中文近义词工具包Synonyms](https://github.com/huyingxi/Synonyms)
