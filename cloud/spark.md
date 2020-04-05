## Spark

[单机用python写spark处理20G的数据](https://zhuanlan.zhihu.com/p/61970650)

#### examples

https://sparkbyexamples.com/

https://docs.databricks.com/

#### udf

##### 輸入多個column到udf
https://stackoverflow.com/questions/42540169/pyspark-pass-multiple-columns-in-udf

##### udf輸出多個column
https://stackoverflow.com/questions/47669895/how-to-add-multiple-columns-using-udf

https://stackoverflow.com/questions/35322764/apache-spark-assign-the-result-of-udf-to-multiple-dataframe-columns

https://stackoverflow.com/questions/48979440/how-to-use-udf-to-return-multiple-columns/48981218

##### drop duplicate

https://stackoverflow.com/questions/50948245/spark-dropduplicates-source-code

https://stackoverflow.com/questions/56076487/how-to-get-the-last-value-with-dropduplicates

https://stackoverflow.com/questions/36623889/spark-how-to-do-a-dropduplicates-on-a-dataframe-while-keeping-the-highest-times

https://stackoverflow.com/questions/35218882/find-maximum-row-per-group-in-spark-dataframe


#### client mode和cluster mode的区别

https://blog.csdn.net/Trigl/article/details/72732241

https://baixin.ink/2018/04/28/spark-mode/

[看了之后不再迷糊-Spark多种运行模式](https://www.jianshu.com/p/65a3476757a5)

[Spark on Kubernetes原生支持浅析](https://www.jishuwen.com/d/23wg)

#### 一些視頻

https://www.youtube.com/watch?v=TDi9YFaw3ic

一些命令

https://www.youtube.com/watch?v=RVNud7tO2hA&list=PLfXXwftXUhTqeLCbIZiFfC_yOEbmn_gJw

29:00左右，memory management

31:00 best practice

https://www.youtube.com/watch?v=5O03Q4UetnA&list=PLfXXwftXUhTqeLCbIZiFfC_yOEbmn_gJw&index=3

13:28, 在facebook，大部分spark程序使用少於600M內存

https://www.youtube.com/watch?v=c4MAgdriJzY&list=PLfXXwftXUhTqeLCbIZiFfC_yOEbmn_gJw&index=11

spark streaming

19:48, streaming example
38:16，spark streaming code

#### spark dataframe and functions

[pyspark读写dataframe](https://zhuanlan.zhihu.com/p/34901558)
[pyspark系列--日期函数](https://zhuanlan.zhihu.com/p/34901927)
[在spark中使用UDF函数](https://zhuanlan.zhihu.com/p/64410979)

#### ETL

https://www.cnblogs.com/yjd_hycf_space/p/7772722.html

https://www.xplenty.com/blog/python-etl-2019-a-list-and-comparison-of-the-top-python-etl-tools/

https://towardsdatascience.com/python-data-transformation-tools-for-etl-2cb20d76fcd0

https://blog.panoply.io/top-9-python-etl-tools-and-when-to-use-them

https://towardsdatascience.com/create-your-first-etl-pipeline-in-apache-spark-and-python-ec3d12e2c169

an example to write mysql

https://spark.apache.org/docs/latest/sql-data-sources-jdbc.html

[使用Spark集群进行ETL的架构介绍](https://blog.csdn.net/zbc1090549839/article/details/54407876)

[Spark 数据ETL](https://blog.csdn.net/u011204847/article/details/51247306)

講了一些machine learning 的data cleaning

https://www.helicaltech.com/basic-etl-spark/

some code

https://databricks.com/session/building-robust-etl-pipelines-with-apache-spark

good, some concepts

spark.read.json("/src/path").printSchema() get the schema of json

一些示例代碼很有用

#### spark packages

https://spark-packages.org/

#### pytest

https://www.sicara.ai/blog/2019-01-14-tutorial-test-pyspark-project-pytest

https://towardsdatascience.com/stop-mocking-me-unit-tests-in-pyspark-using-pythons-mock-library-a4b5cd019d7e

https://stackoverflow.com/questions/33811882/how-do-i-unit-test-pyspark-programs

https://engblog.nextdoor.com/unit-testing-apache-spark-with-py-test-3b8970dc013b

#### spark streaming

https://zhuanlan.zhihu.com/p/51883927

介紹了structured streaming

https://hackersandslackers.com/structured-streaming-in-pyspark/

some code

[Write DataFrame to mysql table using pySpark]https://stackoverflow.com/questions/46552161/write-dataframe-to-mysql-table-using-pyspark)

https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html


#### minikube

https://computingforgeeks.com/how-to-install-apache-spark-on-ubuntu-debian/

https://www.jishuwen.com/d/23wg


#### debug spark

https://stackoverflow.com/questions/30403685/how-can-i-debug-spark-application-locally

#### spark on k8s
[Spark on Kubernetes在Mac的Demo](https://zhuanlan.zhihu.com/p/64242678)

https://medium.com/@aelbuni/apache-spark-2-4-3-running-jobs-in-kubernetes-cluster-ebd7a28b99cd

#### dataframe
[pyspark系列--pyspark读写dataframe](https://zhuanlan.zhihu.com/p/34901558)

https://stackoverflow.com/questions/31385363/how-to-export-a-table-dataframe-in-pyspark-to-csv

#### spark 優化

https://zhuanlan.zhihu.com/p/79543031

[从一段代码浅谈pyspark性能优化](从一段代码浅谈pyspark性能优化)

https://tech.meituan.com/2016/04/29/spark-tuning-basic.html

http://sharkdtu.com/posts/pyspark-internal.html

https://dongkelun.com/2018/06/03/sparkCacheAndPersist/

[Spark的RDD持久化详解](https://zhuanlan.zhihu.com/p/61555283)

[spark内存模型调优](https://zhuanlan.zhihu.com/p/86297292)

[Spark之开发调优以及资源调优](https://zhuanlan.zhihu.com/p/61598086)







