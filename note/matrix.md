### **矩阵乘法几何本质：**

第二个矩阵分解为多个列向量，每个列向量做第一个矩阵构成的线性变换，把变换后的向量拼接起来即可。

什么样的线性变换呢：第一个矩阵的列向量可以看做是把矩阵空间的基向量线性变换，如图中向量[ 3 , 1] , [ 1 ,  2 ]，组合生成新的向量，拼接向量即可。

![image-20220106201053266](https://s2.loli.net/2022/01/06/4LudiWFCMrvGZnS.png)

<img src="https://s2.loli.net/2022/01/06/qrNzFRWoTGexMip.png" alt="image-20220106201009176" style="zoom: 67%;" />

### **行列式:**  

只对行列数目相同的矩阵有意义，行列式的值有正有负，判断条件是是否满足右手螺旋定理。

二维：两个列向量组成的平行四边形的面积。

三维：三个列向量组成的平行六面体的体积。

### **矩阵点乘 :**



**矩阵叉乘 :**