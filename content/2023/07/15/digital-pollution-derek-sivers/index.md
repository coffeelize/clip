---
title: "Digital pollution"
date: 2023-07-15T19:39:09+08:00
updated: 2023-07-15T19:39:09+08:00
taxonomies:
  tags: []
extra:
  source: https://sive.rs/polut
  hostname: sive.rs
  author: 
  original_title: "Digital pollution | Derek Sivers --"
  original_lang: en
---

2019-10-15

You couldn’t just roll down the street leaving huge piles of garbage everywhere you go, making life slower for everyone as they climb over your mountains of junk, just to get on with their life. You’d feel bad about it, right?  

你不能只是沿着街道滚下去，到处都留下大堆垃圾，让每个人的生活变得更慢，因为他们爬过你的垃圾山，只是为了继续他们的生活。你会为此感到难过，对吗？

That’s how I feel about the digital things we put out into the world: websites, apps, and files.  

这就是我对我们向世界推出的数字化事物的感受：网站、应用程序和文件。

I prefer coding everything by hand, because I don’t like the huge piles of garbage that the automated generators create. These programs that generate a website, app, or file for you spit out thousands of lines of unnecessary junk when really only 10 lines are needed. Then people wonder why their site is so slow, and they think it’s their phone or connection’s fault.  

我更喜欢手动编写所有内容，因为我不喜欢自动生成器产生的大量垃圾。这些为您生成网站、应用程序或文件的程序会吐出数千行不必要的垃圾，而实际上只需要 10 行。然后人们想知道为什么他们的网站这么慢，他们认为这是他们的手机或连接的问题。

Yesterday I needed to make a little vector logo. Two lines and two triangles. I tried to use a couple different vector drawing programs but they saved it as hundreds of lines. I knew it could be simpler, so I read up on SVG and made exactly what I wanted:  

昨天我需要制作一个小矢量标志。两条直线和两个三角形。我尝试使用几个不同的矢量绘图程序，但它们将其保存为数百行。我知道它可以更简单，所以我阅读了 SVG 并制作了我想要的东西：

```
<svg height="54" width="54">
<defs><style type="text/css"><![CDATA[line,polygon{stroke:black;stroke-width:4} polygon{fill:black}]]></style></defs>
<line x1="2" y1="2" x2="2" y2="52" />
<line x1="52" y1="2" x2="52" y2="52" />
<polygon points="2,2 27,27 2,27" />
<polygon points="52,2 27,27 52,27" />
</svg> 


```

![](HitMediaLogo-54.svg)

Much better! 95% smaller file size, and the joy of making something by hand instead of having it done for me. But I think my biggest joy is **eliminating the digital pollution** that the auto-generated one created. It makes everything faster, easier, and cleaner for anyone involved. 95% less junk over the wires.  

好多了！文件大小缩小了 95%，以及手工制作东西而不是别人为我完成的乐趣。但我认为我最大的快乐是消除自动生成的数字污染。对于任何相关人员来说，它使一切变得更快、更容易、更干净。电线上的垃圾减少 95%。

Same thing with the EPUB file for my new book. Today I spent the day creating the EPUB’s XML and XHTML by hand, instead of using a generator. I love the manual control and again - 90% smaller file size.  

我的新书的 EPUB 文件也是如此。今天我花了一天时间手动创建 EPUB 的 XML 和 XHTML，而不是使用生成器。我喜欢手动控制，而且文件大小减小了 90%。

This makes me unreasonably happy. It feels like cleaning up the neighborhood. Or at least my yard.  

这让我感到莫名的高兴。感觉就像清理邻居一样。或者至少是我的院子。

(And I love it when people notice how fast my site loads.)  

（当人们注意到我的网站加载速度有多快时，我很高兴。）

![](HitMediaLogo-54.png)
