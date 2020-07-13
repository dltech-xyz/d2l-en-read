

<!--
 * @version:
 * @Author:  StevenJokes https://github.com/StevenJokes
 * @Date: 2020-07-08 19:12:24
 * @LastEditors:  StevenJokes https://github.com/StevenJokes
 * @LastEditTime: 2020-07-08 20:14:34
 * @Description:translate
 * @TODO::
 * @Reference:https://d2l.ai/chapter_appendix-mathematics-for-deep-learning/multivariable-calculus.html
-->

# 多元微积分

现在我们已经对单变量函数的导数有了相当深入的了解，让我们回到最初的问题，我们正在考虑一个可能有数十亿重量的损失函数。

## 高维微分

第18.3节告诉我们的是，如果我们改变这数十亿重量中的一个，而其他重量保持不变，我们就知道会发生什么！这只不过是一个单变量的函数，所以我们可以写

TODO:MATH

我们将一个变量中的导数称为*偏导数*，而另一个变量中的导数将被修正。在(18.4.1)中，我们将使用标记方法∂∂w1:

现在，让我们把 w 2 w2改成 w 2 + 2 w2 + 2:

我们再次使用了1212这个概念，它是一个高阶项，我们可以像上一节中抛弃22一样抛弃它，还有我们在(18.4.1)中看到的。以这种方式继续下去，我们可以这样写

TODO:MATH

然后

我们将向量 w l something wL 称为 l l 的梯度。

方程式(18.4.5)值得思考一会儿。它的格式和我们在一维空间中遇到的格式完全一样，只是我们把所有的东西都转换成了矢量和点积。它允许我们近似地告诉我们，在任何对输入的扰动情况下，函数 l 将如何变化。正如我们将在下一节中看到的，这将为我们提供一个重要的工具，帮助我们以几何学的方式理解如何使用梯度中包含的信息来学习。

但是首先，让我们用一个例子来看看这个近似，假设我们在处理函数

TODO:MATH

如果我们观察一个点，比如(0，log (2))(0，log (2)) ，我们可以看到

因此，如果我们想近似 f 在(1，log (2) + 2)(1，log (2) + 2)处，我们看到我们应该有(18.4.5)的具体实例:

我们可以在代码中测试这一点，看看这个近似有多好。

## 梯度和梯度下降的几何

TODO:电脑装机搞了一天，烧的不行。

