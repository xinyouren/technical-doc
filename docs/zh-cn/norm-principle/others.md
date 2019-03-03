## Excel
&emsp;&emsp;Excel主要是用来存储数据和处理数据的工作，Excel从功能上分为据源表和数据报告表。由于数据报告表是由目的导向的，不同的目的要求就会有不同的处理方法和呈现形式。此处仅探讨作为数据源表时的Excel操作规范。  

`不要觉得简单，任何简单的事情乘以数据级都会变得不容易，而且会遇到超出预期的困难。`
#### 禁止
- 1、禁用合并单元格，因为：会被很多“大佬”吐槽。  
- 2、对于存储“编码”、“日期”、“数值”的列，禁止使用“常规”的单元格数据类型。
- 3、用作最终数据存档、数据流转的Excel表格，禁止含有公式的单元格。因为：下一个处理者无法知道哪些单元格会存有公式，如果观察不到就会很容易在下一步数据数量中出现错误。  
- 4、对于存储“数值”的列，禁用“无”或“-”代替空单元格。因为：如，在将Excle数据导入数据库时，数值类型的字段含有非数字类型时会导致错误。  
- 5、禁止使用如“20190208”、“2019.2.8”的日期类型，正确的日期格式：yyyy-MM-dd(推荐)、yyyy/MM/dd，同理，时间格式为：yyyy-MM-dd HH : mm : ss （24小时制）。  

![单元格数据类型](../_images/excel/单元格数据类型.jpg)
#### 建议
- 1、对于存储“编码”、“身份证号码”以及超过11位的数值列， 推荐使用文本格式，或输入英文单引号“'”。因为：Excel会将以“0”开头的数字被吃掉。  
- 2、删除多余的表头、空行、空列、合计行，因为这些在使用SQL或Python等其它工具处理时没有任何作用，只会增加负担甚至造成更大的错误。  
- 3、一个单元格记录只一个属性，避免出现“200吨”等，应当分为两列分别存为两列“200”、“吨”。
- 4、使用单层表头。
- 5、合理设计字段，如宁可分别设计“省”、“市/州”、“区/县”三列，也不要单独设计一列“省市区”。
- 6、数据处理以简单原则优先，避免过长的公式。
---

## 数据可视化

#### 数据展示
数据的展示分成比较、序列、构成、描述四种。

#### 原则
- 加法：信息完整性、易读性。
- 减法：排除视觉干扰。
- 布局：要注意对齐、对比、重复；
- 配色：基于红黄蓝三原色设计的色轮。将颜搭配分成下面四类：单色、类比色、补色、分裂补色。
![单元格数据类型](../_images/dataVisualization/数据可视化.jpg)

#### 避免
- 1、无度量单位；
- 2、数据位数太长；
- 3、无排序、重点不突出；
- 4、.相对差异不明显；