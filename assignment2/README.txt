1. 系统环境

   系统：Ubuntu16.04.1 64位 或 Windows 10 ， 内存8GB，酷睿i5-6500
   IDE：PyCharm 2016.2
   编程语言：Python 3.5.2 （Anaconda Python 4.1.1）
   使用到的第三方Python库 ： numpy:1.11.1(测试使用了scikit-learn:0.18)
   数据：原始数据在项目根目录下的data目录下，文件夹为BinaryDatasets，里面含四个文件：sonar-test.txt，sonar-train.txt，splice-test.txt，splice-train.txt

2. 运行

   1): 进入到code根目录,可看到项目文件
   2): 在终端中运行：python3 runAssignment2.py,等待一段时间左右后(ISOMAP比较耗时，测试了k=4,6,8,10四种情况)，待运行结束后便可以在终端上看到结果。
   3): 可选，作为对比，运行Scikit-learn：python3 -c "from tests import ReductionTest;ReductionTest.run()"
   3): 结果类似如下：
		====算法：PCA ====
		sonar文件测试结果：
		k=10,正确率：60/103=58.252427184466015%
		k=20,正确率：58/103=56.310679611650485%
		k=30,正确率：58/103=56.310679611650485%
		====算法：SVD ====
		sonar文件测试结果：
		k=10,正确率：61/103=59.22330097087378%
		k=20,正确率：60/103=58.252427184466015%
		k=30,正确率：58/103=56.310679611650485%
		===ISOMAP 文件:sonar:出现孤立点===
		训练集位置:[83, 84, 85, 86, 87, 88],测试集位置:[]
		====算法：ISOMAP-k4 ====
		sonar文件测试结果：
		k=10,正确率：48/103=46.601941747572816%
		k=20,正确率：56/103=54.36893203883495%
		k=30,正确率：56/103=54.36893203883495%
		====算法：ISOMAP-k6 ====
		sonar文件测试结果：
		k=10,正确率：43/103=41.74757281553398%
		k=20,正确率：43/103=41.74757281553398%
		k=30,正确率：45/103=43.689320388349515%
		...
