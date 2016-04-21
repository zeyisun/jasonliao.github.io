---
layout: post
category: interview
title: Tencent Phone Interview II
date: 2016-03-31
summary: 腾讯内推第二轮电话面试题目和总结
---

30 号那天的晚上，在等了半个月之后，腾讯竟然打来了二面的电话，真是让我又惊又喜。

虽然这次面试并没有问太多的技术问题，但更多的时候都是我在说，把我的理解和我所知道的都说出来。因为这次面试来得毫无准备，所以面试之后还是很懵逼的，所以问题也没有记得很清楚

一开始还是问了一下我投的时候，希望工作的城市是广州，如果到深圳来有没有问题。那当然是没有问题啦。接着就开始正式的技术问题了

 1. **HTML，CSS 和 JavaScript，5 分满分，你分别给自己打多少分呢**

    我觉得我的 HTML 可以有 3 分，CSS 只有 2 分，JavaScript 可以有 3.5 分

 2. **所以你觉得你的 JavaScript 是比较好的是吧**

    嗯嗯，其他相对 CSS，我更喜欢 JavaScript，所以会发更多时间在 JavaScript 的基础上，例如原型呀，继承呀，闭包和作用域这些，其实你可以问问我关于这些的知识的

 3. **哦哦哦，不需要了，我知道你基础挺好的，那我来问问你 HTML 的第一句是什么**

    `<!DOCTYPE html>`

 4. **那为什么要写这句话呢**

    因为浏览器会有标准模式和怪异模式，当它解析这个 HTML 的时候，看到这个的时候，就会知道要使用标准模式去解析我们这个页面

 5. **那如果 IE6 遇到这句会怎么样呢**

    可能会忽略吧，我也不太清楚，因为我们平时做项目的时候，都不需要支持 IE6 了，因为它实在是太坑了我觉得。我们的项目都是只需要兼容到 IE10 或以上就可以了

 6. **那你有写过 HTML5 吗？**

    你说的是移动端的页面是吗？其实我很少说去特意写所谓的 H5 页面，因为我平时如果做项目或者自己的小应用都会考虑到适配响应的问题。但我们实验室的项目更多的是以 Web App 为主，所以其实在移动端应用这方面还是比较欠缺的，但是我对 HTML5 的新特性还是有一些了解的

 7. **那你说说 HTML5 有哪些新增的东西吧**

    然后我就根据我之前总结的一些 [关于 HTML5](https://github.com/L-movingon/prepare-for-interview/blob/master/HTML/something-about-html5.md) 的东西给他说，主要从语义化的标签和新的 API 讲，这部分讲得还挺久的。

    *(我忘记是不是这个时候了，我讲完之后。面试官突然停止发问了，可能在做其他事情)*

 8. **我看到你在之前的面试中，有问到快排，但是为什么不会呢，你们是什么时候学习数据结构的**

    哦哦，我是大二的时候学习的数据结构，其实不可以说不会吧，因为那是第一次的面试，非常紧张，如果你有看到的话，上面问我 HTTP 的时候，我也是说不懂的，但事实上从我们平时做项目来说，对于 HTTP 的请求方法还有状态码这些，都是知道的，只是没有说上来。

    *(这时我还以后他会问我数据结构，但结果没有，他开始往网络方面转了)*

 9. **这样，那现在我有一个这样的情况，一台全新的笔记本，在浏览器里访问百度的时候，返回的状态码是什么？**

    200
    
    *(其他一开始问的时候，我还以为他会问我从地址栏输入网址到页面渲染出来，之间做了什么，但最后并没有，当他说状态码的时候，我就知道他想问缓存了)*

10. **那当我按 F5 刷新页面的时候呢**

    我觉得部分请求是 200，部分是 304

11. **为什么会返回 304 呢，304 是什么意思**

    304 是 Not Modified 的意思，就是这个资源没有修改过的意思。其实这是一种缓存机制。然后我就把我自己对 **强缓存** 和 **协商缓存** 的理解说出来

12. **那我们更深入一点吧，可能会比较难，服务器端是怎么知道这个资源是没有修改过的呢**

    因为我们再次请求的时候，会把上一次返回资源的时候，会在返回报文里拿到一个 ETag 的头信息，当我再次请求这个资源的时候，就会把这个 ETag 放在请求头里发送过去，服务器就会对这个 ETag 进行 Match，如果服务器端没有修改过这个资源，那么就会相同，就会返回 304，告诉浏览器可以在本地缓存里获取，而如果服务器端对这个资源修改过，那么就会不相同，那么就会正常返回该资源，状态码为 200

13. **嗯嗯，好，我看到你还总结了一下性能优化，那你说说网站性能优化都有哪些方式**

    然后就开始说了，由于有了上一次的总结，所以这次并没有入坑
    
    但是面试官拼命的问我然后呢然后呢，不是有 35 条吗？你一直说就好了

    最后说得差不多了，面试官才接着问，真是吓死我了

14. **那怎么优化移动端的性能呢**

    我说的第一个是把样式尽可能的放在 `<head>` 标签里，把脚步放在 `</body>` 前，这样可以加快 DOM tree 和 CSSOM 的构造，有肋于第一屏的加载速度。第二个是减少 DOM 的操作，因为 DOM 的操作会造成 repaint 或 reflow，因为手机本来可视范围就小，一次 repaint 或 reflow 就有可能使整个页面重新排列，就有可能出现白屏的现象

15. **你对你以后的职业规划是怎样的**

    我其实还是挺重视这次实习的机会的，我想把我学的前端的技术落实下去，因为我知道像我学的 React 呀，Node 呀，如果没有一些大的项目真正实践的话，是很难发现它的一些真正的魅力或者说问题

16. **那如果你进去之后发现不是这样呢，和你想像的不一样呢**

    没关系呀，我觉得我还在做前端的话，我就很开心

17. **你现在在 GitHub 上维护多少个项目呢**

    活跃的有 4，5 个吧，然后就开始吹 GitHub 的 repo

18. **那你有没有学过 C++ 呢**

    没有，没有学过 C++

19. **为什么不学 C++，以后会不会学 C++**

    现阶段不会吧，现在我还是比较专注于前端。

20. **那你有没有其他后台语言的经验，像 PHP，Python，Ruby**

    我们工作室考核的时候，我学过 Java，会做一些小型的管理系统，还有我对 Node 也有一定的了解

21. **那你 Node 去到哪里呢**

    不会写 npm 包，但是会用 Express，Koa 这些框架构建一些小型应用

22. **好的，明白，那你还有什么想要问我的吗**

    我还是不知道我今天表现得怎么样

23. **可以的，可以的，那我们下次有机会再聊**

    好的，十分感谢，再见

个人感觉这次面试比上一次要好，因为放得更开，很多自己想说，可以扩展的都表达了出来，但还是太过紧张，其实可以把握一下节奏。还有两天腾讯就要正式校招的笔试了，不知道会不会在最后关头接到 HR 的电话呢，加油吧！