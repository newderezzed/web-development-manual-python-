# web 开发者实战



## 第一章、初始web开发

### 1.web开发介绍

**服务端编程介绍**：

> 大多数的大型网站采用服务器端编程来在需要的时候动态展示不同的信息，这些信息通常会从服务器上的数据库中取出，然后发送给客户端，并通过一些代码（比如HTML和Javascript）展示在客户端。 
>
> 或许服务器端编程的最大益处在于它允许你对不同的用户个体展示不同的网站信息。动态网站可以高亮基于用户喜好和习惯的与用户相关度更高的内容。服务器端编程可以通过存储偏好设置和其他个人信息来让网站更加简洁——比如通过重复使用信用卡的详细信息来简化后续付款流程。 
>
> 它甚至可以允许和用户的线下互动，比如通过邮件或者其他渠道发送通知和更新信息。服务器端的所有的这些能力使得网站可以与用户有更深的联系。
>
> 在当今这样一个网络发达的时代，学习服务器端编程是很被推荐的。

**服务端编程是什么**？

> 网络浏览器通过**超文本传输协议** ([HTTP](https://developer.mozilla.org/en-US/docs/Glossary/HTTP))来和[网络服务器](https://developer.mozilla.org/zh-CN/docs/Learn/Common_questions/What_is_a_web_server) 进行通信。当你在网页上点击一个链接，或提交一个表单，再或进行一次搜索时，一个**HTTP请求**就从你的浏览器发送到了目标服务器。 
>
> 这个请求包括一个标识所请求资源的URL，一个定义所需操作的方法(比如获取，删除或者发布资源)，还可以包括编码在URL参数中的附加信息。附加信息以键值对（参数和它的值）的形式，通过一个[查询字符串](https://en.wikipedia.org/wiki/Query_string)，作为POST数据（由[HTTP POST方法](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Methods/POST)发送）或存放在 [associated cookies](https://developer.mozilla.org/en-US/docs/Glossary/Cookie)中。 
>
> 网络服务器等待客户端的请求信息，在它们到达的时候处理它们，并且回复网络浏览器一个**HTTP回应**信息。这个回应包含一个提示请求是否成功的状态码（比如“HTTP/1.1 200 OK”代表请求成功）。 
>
> 相应一个请求的成功回应包含被请求的资源（比如一个新的HTML页面，或者图片等），然后这些会被展示在客户端的网络浏览器上。 

**服务器端编程和客户端编程是一样的吗**？

> 让我们将注意力转向涉及服务器端编程和客户端编程的代码。在每一个情况下，代码都是显然不同的：
>
> - 它们有不同的目的和关注点。
> - 它们通常不会使用相同的编程语言（Javascript是一个特例，它既可以被用在服务器端也可以被用在客户端）。
> - 它们在不同的操作系统环境中运行。
>
> 在浏览器端运行的代码被称为**客户端代码**，并且主要涉及所呈现的网页的外观和行为的改进。这就包括选择和设计UI元素、布局、导航、表单验证等。相反的，服务器端网站编程主要涉及，对于相应的请求，选择所要返回给浏览器的内容。服务器端代码解决这样一些问题，比如验证提交的数据和请求、使用数据库来存储和检索信息及发送给用户正如他们所请求的的正确内容。 
>
> 客户端代码使用 [HTML](https://developer.mozilla.org/zh-CN/docs/Learn/HTML)，[CSS](https://developer.mozilla.org/zh-CN/docs/Learn/CSS)，和[JavaScript](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript) 来编写——这些代码直接在网络浏览器中运行，并且几乎没有访问底层操作系统的路径（包括访问文件系统的被限制的权限）。网络开发者无法掌控每一个用户可能使用的用来浏览网页的浏览器——不同的浏览器对客户端代码的性能提供不一致的的兼容性，然后客户端编程的一个挑战就是如何妥善处理不同浏览器的兼容性差异。 
>
> 服务器端代码可以用任何一种编程语言进行编写——比较受欢迎的服务器端编程语言包括PHP、Python、Ruby和C#。服务器端代码有充分的权限访问服务器的操作系统，并且开发者可以选择他们乐意使用的编程语言（和特定版本的语言）。 
>
> 开发者们通常会使用web框架来编写他们的代码。web框架是一个各种函数、对象、方法和其他代码结构的集合体，web框架被设计用来解决一些普遍问题，从而加速开发，并且简化在一个特定域中面临的不同类型的任务。同样的，当客户端和服务器端代码使用框架时，它们的域是不同的，因此框架也会不同。客户端web框架简化布局和演示任务，然而服务器端web框架提供大量的普通网络服务功能，不然的话你可能需要自己来实现这些功能（比如支持会话、支持用户和身份验证、简单的数据访问、模板库等）。 
>
> > **注意事项**：客户端框架通常被用来帮助加速客户端代码的开发，但是你也可以选择手写所有的代码；事实上，如果你只需要一个小型的、简单的网站UI，手写自己的代码可能更快并且更高效。相反的，你应该从来没有考虑过不使用框架而直接编写web应用程序的服务器端组件——实现一个重要的功能比如HTTP服务器真的很难直接从头开始用Python语言构建，但是一些用Python语言写的web框架，比如Django提供了开箱即用的功能，同时还包含其他很多有用的工具。 

【详解】：https://developer.mozilla.org/zh-CN/docs/learn/Server-side/First_steps/Introduction

### 2.web框架介绍

【很好的科普文-通俗易懂】：https://q1mi.github.io/Blog/2017/09/10/aboutWebframework/

【知乎】： https://zhuanlan.zhihu.com/p/32327786 

***关键词***：

[websocket](http://www.ruanyifeng.com/blog/2017/05/websocket.html)

[gevent](http://www.bjhee.com/gevent.html)

[greenlet](http://www.bjhee.com/greenlet.html)

[单元测试](https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/00143191629979802b566644aa84656b50cd484ec4a7838000)