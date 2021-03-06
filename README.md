# Oriento/青
A new language designed by oriental way

欢迎您关注Oriento/青 语言项目。 

Zen of Oriento

最好的面向对象语言就是自然语言。
能用人话说清，就不说机器话。
能用一行话说清，就不用几行话。


## 前言
计算机语言的发展过程，是自然语言与机器语言，也即人与机器间互相配合、协调、平衡的过程。机器与人是如此的不同。要跨越这道鸿沟，我们要在层层复杂的封装与抽象过程中作出很多艰难的取舍和妥协。所幸的是，计算机语言发展日新月异，在最近的十数年里，我们取得了非凡的成就。面向对象思想的普及，为这个艰难的平衡指明了正确的方向；虚拟化思想的广泛应用，使得高性能语言兼顾了良好的移植性；JIT技术的发展，使得脚本语言在保持灵活的同时拥有了充足的性能。我们在渐渐逼近计算机语言的“黄金平衡点”  
回首过去曾经出现的每一门计算机语言，它们都或古朴，或优雅，或精美，或简洁，不仅是实用的工具，更完全当得起艺术品之称。但是我们可以发现一个普遍的现象，2019年，虽然程序的底层架构已经和以往截然不同，但是在代码的书写上，我们基本上仍然保留了半个世纪之前面向过程式的编码习惯：
- 以行为单位，每行仅完成简单的工作
- 多行语句构成函数或代码块，完成复杂过程，
- 多个函数或代码块组成程序

这种在全部信息密度集中在垂直维度的书写习惯，在现在看来，越来越显得非常奇怪，因为，这种习惯已经给程序的可读性带来了巨大的障碍，每个程序员心里应该都有所体会。大家也许都听过那个俄罗斯特工的笑话：一个不懂编程的俄罗斯特工冒死偷出了一段美国核安保程序的代码，结果发现是"}}}...}}}"。或许对于逻辑思维优秀的你来说，理解程序语法中层层的嵌套并不是什么问题，但对于那些逻辑思维不那么强的人来说，这成为了他们学习计算机路上最好的劝退。  

## 能不能不那么啰嗦？——一个提升面向对象程序可读性的思路 
自从面向对象思想被广泛接受，我认为计算机编程就发生了天翻地覆的变化，程序编写的重点，从关注过程本身转变为关注对象结构与关系的抽象，这无疑更加贴近现实，同时，也更加贴近自然语言，因为自然语言本身，就是对对象的一种叙述。然而，我们却没有创造出更加贴近自然语言的代码书写方式，反而一直在使用面向过程的书写方式来书写面向对象的程序。  
举个例子：
一个苹果长大，被小明吃掉了。
我们都知道，若要模拟这个过程，我们一般会写一个“苹果”类，它有若干属性，同时还拥有“长大”“被吃掉”这两个方法，然后我们再用这个类生成一个苹果对象，然后执行”长大“过程，然后将“小明”代入“被吃掉”这个过程执行
写成伪代码，就是：
```
//定义部分
苹果类：
属性 a；属性 b；
方法1 长大()：{如何长大}
方法2 被吃掉(某人)：{如何被吃掉}
//实例化部分
苹果a = new 苹果
苹果a.长大()
苹果a.被吃掉(小明)
```
即使用最简单的伪代码，还是至少需要七句话来描述清楚这个事情，每句话都只说了一点点的内容。然而，如果句子的内容丰富一些，其实是一个几句话就能说清楚的事情。
```
“长大” 就是：{长大的过程}
“被吃掉” 就是：{如何被吃掉}
苹果 这类东西，拥有 a，b 属性，能 长大，能 被吃掉
//
a 是一个 苹果，它 长大，它 被(小明) 吃掉。
```
每句话描述一件事，而不是将一件事拆成几句话来说。

固然，我们其实并没有缩减程序的逻辑，但是，换一种写法，其可读性是天壤之别。
我认为，这才是面向对象语言理应的书写方式。这样做的实质是：

- 重新分配水平方向与垂直方向的信息密度。面向过程时代的程序，单行语句包含的逻辑较复杂，同时程序结构上较简单，书写时水平方向与垂直方向的信息密度比较均衡。面向对象时代，函数封装变得十分普遍，单行语句往往是函数的调用，信息密度大幅减少，同时程序结构复杂度剧增，导致代码书写时垂直方向上的信息密度暴增。是时候建立新的代码习惯了。
- 自然语言本身就是面向对象的，贴近自然语言的代码形式，同时也更贴近了面向对象的实质，这就是面向对象思想的伟大之处。







