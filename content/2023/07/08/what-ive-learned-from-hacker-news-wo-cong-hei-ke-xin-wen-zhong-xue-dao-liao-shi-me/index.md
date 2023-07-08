---
title: "What I've Learned from Hacker News"
date: 2023-07-08T11:48:26+08:00
updated: 2023-07-08T11:48:26+08:00
taxonomies:
  tags: []
extra:
  source: http://www.paulgraham.com/hackernews.html
  hostname: www.paulgraham.com
  author: 
  original_title: "What I've Learned from Hacker News --- 我从黑客新闻中学到了什么"
  original_lang: en
---

February 2009 2009年2月

Hacker News was two years old last week. Initially it was supposed to be a side project—an application to sharpen Arc on, and a place for current and future Y Combinator founders to exchange news. It's grown bigger and taken up more time than I expected, but I don't regret that because I've learned so much from working on it.  

《黑客新闻》上周两周岁了。最初，它被认为是一个业余项目——一个增强 Arc 的应用程序，以及当前和未来 Y Combinator 创始人交换新闻的地方。它变得越来越大，占用的时间比我预期的要多，但我并不后悔，因为我从它的工作中学到了很多东西。

**Growth 生长**

When we launched in February 2007, weekday traffic was around 1600 daily uniques. It's since [grown](http://ycombinator.com/images/2yeartraffic.png) to around 22,000. This growth rate is a bit higher than I'd like. I'd like the site to grow, since a site that isn't growing at least slowly is probably dead. But I wouldn't want it to grow as large as Digg or Reddit—mainly because that would dilute the character of the site, but also because I don't want to spend all my time dealing with scaling.  

当我们于 2007 年 2 月推出时，工作日的每日独立访问量约为 1600 人。此后已增至约 22,000 个。这个增长率比我想要的要高一些。我希望该网站能够增长，因为一个至少不缓慢增长的网站可能已经死了。但我不希望它发展得像 Digg 或 Reddit 一样大，主要是因为这会淡化网站的特色，但也因为我不想把所有时间都花在处理扩展上。

I already have problems enough with that. Remember, the original motivation for HN was to test a new programming language, and moreover one that's focused on experimenting with language design, not performance. Every time the site gets slow, I fortify myself by recalling McIlroy and Bentley's famous quote  

我已经有足够多的问题了。请记住，HN 的最初动机是测试一种新的编程语言，而且该语言的重点是试验语言设计，而不是性能。每当网站变慢时，我都会通过回忆麦克罗伊和本特利的名言来增强自己

The key to performance is elegance, not battalions of special cases.  

性能的关键是优雅，而不是大量的特殊情况。 and look for the bottleneck I can remove with least code. So far I've been able to keep up, in the sense that performance has remained consistently mediocre despite 14x growth. I don't know what I'll do next, but I'll probably think of something.  

并寻找我可以用最少的代码消除的瓶颈。到目前为止，我已经能够跟上，尽管增长了 14 倍，但性能仍然平庸。我不知道接下来要做什么，但我可能会想到一些事情。

This is my attitude to the site generally. Hacker News is an experiment, and an experiment in a very young field. Sites of this type are only a few years old. Internet conversation generally is only a few decades old. So we've probably only discovered a fraction of what we eventually will.  

这是我对网站的总体态度。 《黑客新闻》是一项实验，而且是在一个非常年轻的领域进行的实验。此类网站只有几年的历史。互联网对话一般只有几十年的历史。所以我们可能只发现了我们最终发现的一小部分。

That's why I'm so optimistic about HN. When a technology is this young, the existing solutions are usually terrible; which means it must be possible to do much better; which means many problems that seem insoluble aren't. Including, I hope, the problem that has afflicted so many previous communities: being ruined by growth.  

这就是为什么我对HN如此乐观。当一项技术如此年轻时，现有的解决方案通常很糟糕；这意味着一定有可能做得更好；这意味着许多看似无法解决的问题其实并非如此。我希望包括困扰许多以前社区的问题：被增长毁掉。

**Dilution 稀释**

Users have worried about that since the site was a few months old. So far these alarms have been false, but they may not always be. Dilution is a hard problem. But probably soluble; it doesn't mean much that open conversations have "always" been destroyed by growth when "always" equals 20 instances.  

自从该网站成立几个月以来，用户就一直担心这一点。到目前为止，这些警报都是假的，但也可能并非总是如此。稀释是一个难题。但可能是可溶的；当“总是”等于 20 个实例时，开放对话“总是”被增长所破坏并没有多大意义。

But it's important to remember we're trying to solve a new problem, because that means we're going to have to try new things, most of which probably won't work. A couple weeks ago I tried displaying the names of users with the highest average comment scores in orange.  

但重要的是要记住我们正在尝试解决一个新问题，因为这意味着我们将不得不尝试新事物，其中大多数可能行不通。几周前，我尝试用橙色显示平均评论得分最高的用户姓名。

\[[1](http://www.paulgraham.com/hackernews.html#f1n)\] That was a mistake. Suddenly a culture that had been more or less united was divided into haves and have-nots. I didn't realize how united the culture had been till I saw it divided. It was painful to watch. \[[2](http://www.paulgraham.com/hackernews.html#f2n)\]  

那是个错误。突然之间，一种或多或少统一的文化被分为富人和穷人。直到我看到文化的分裂，我才意识到它是多么团结。看着很痛苦。 \[2\]

So orange usernames won't be back. (Sorry about that.) But there will be other equally broken-seeming ideas in the future, and the ones that turn out to work will probably seem just as broken as those that don't.  

所以橙色用户名不会再回来了。 （对此感到抱歉。）但是将来还会有其他看似同样破碎的想法，而那些被证明可行的想法可能看起来和那些不可行的想法一样破碎。

Probably the most important thing I've learned about dilution is that it's measured more in behavior than users. It's bad behavior you want to keep out more than bad people. User behavior turns out to be surprisingly malleable. If people are [expected](http://ycombinator.com/newswelcome.html) to behave well, they tend to; and vice versa.  

关于稀释，我学到的最重要的一点可能是，它更多地通过行为来衡量，而不是通过用户来衡量。与坏人相比，您更希望将不良行为拒之门外。事实证明，用户行为具有惊人的可塑性。如果人们期望表现良好，他们就会倾向于；反之亦然。

Though of course forbidding bad behavior does tend to keep away bad people, because they feel uncomfortably constrained in a place where they have to behave well. But this way of keeping them out is gentler and probably also more effective than overt barriers.  

当然，禁止不良行为确实会让坏人远离，因为他们在必须表现良好的地方感到不舒服。但这种将他们拒之门外的方式比明显的障碍更温和，也可能更有效。

It's pretty clear now that the broken windows theory applies to community sites as well. The theory is that minor forms of bad behavior encourage worse ones: that a neighborhood with lots of graffiti and broken windows becomes one where robberies occur. I was living in New York when Giuliani introduced the reforms that made the broken windows theory famous, and the transformation was miraculous. And I was a Reddit user when the opposite happened there, and the transformation was equally dramatic.  

现在很清楚，破窗理论也适用于社区网站。该理论认为，轻微的不良行为会引发更严重的行为：一个有大量涂鸦和破损窗户的社区就会成为抢劫发生的地方。当朱利安尼推出使破窗理论著名的改革时，我住在纽约，这种转变是奇迹般的。当我是 Reddit 用户时，那里发生了相反的情况，而且转变同样引人注目。

I'm not criticizing Steve and Alexis. What happened to Reddit didn't happen out of neglect. From the start they had a policy of censoring nothing except spam. Plus Reddit had different goals from Hacker News. Reddit was a startup, not a side project; its goal was to grow as fast as possible. Combine rapid growth and zero censorship, and the result is a free for all. But I don't think they'd do much differently if they were doing it again. Measured by traffic, Reddit is much more successful than Hacker News.  

我不是在批评史蒂夫和亚历克西斯。 Reddit 发生的事情并不是因为疏忽而发生的。从一开始，他们就制定了除了垃圾邮件之外不审查任何内容的政策。另外，Reddit 与 Hacker News 有着不同的目标。 Reddit 是一家初创公司，而不是一个业余项目；它的目标是尽可能快地增长。将快速增长和零审查制度结合起来，结果就是所有人免费。但我认为，如果他们再做一次，他们的做法不会有太大不同。从流量来看，Reddit 比 Hacker News 成功得多。

But what happened to Reddit won't inevitably happen to HN. There are several local maxima. There can be places that are free for alls and places that are more thoughtful, just as there are in the real world; and people will behave differently depending on which they're in, just as they do in the real world.  

但 Reddit 发生的事情并不一定会发生在 HN 身上。有几个局部最大值。可以有对所有人免费的地方，也可以有更贴心的地方，就像现实世界一样；人们的行为会根据所处环境的不同而有所不同，就像在现实世界中一样。

I've observed this in the wild. I've seen people cross-posting on Reddit and Hacker News who actually took the trouble to write two versions, a flame for Reddit and a more subdued version for HN.  

我在野外观察到了这一点。我见过有人在 Reddit 和 Hacker News 上交叉发帖，他们实际上不厌其烦地写了两个版本，Reddit 的火焰版本和 HN 的更柔和的版本。

**Submissions 意见书**

There are two major types of problems a site like Hacker News needs to avoid: bad stories and bad comments. So far the danger of bad stories seems smaller. The stories on the frontpage now are still roughly the ones that would have been there when HN started.  

像 Hacker News 这样的网站需要避免两种主要类型的问题：糟糕的故事和糟糕的评论。到目前为止，坏故事的危险似乎较小。现在头版上的故事仍然大致是 HN 成立时的内容。

I once thought I'd have to weight votes to keep crap off the frontpage, but I haven't had to yet. I wouldn't have predicted the frontpage would hold up so well, and I'm not sure why it has. Perhaps only the more thoughtful users care enough to submit and upvote links, so the marginal cost of one random new user approaches zero. Or perhaps the frontpage protects itself, by advertising what type of submission is expected.  

我曾经以为我必须对选票进行权衡，以防止垃圾内容出现在头版上，但我还没有这样做。我没想到首页会保持得这么好，我也不知道为什么会这样。也许只有更有思想的用户才会足够关心提交和投票链接，因此一个随机新用户的边际成本接近于零。或者首页可能会通过宣传预期提交的类型来保护自己。

The most dangerous thing for the frontpage is stuff that's too easy to upvote. If someone proves a new theorem, it takes some work by the reader to decide whether or not to upvote it. An amusing cartoon takes less. A rant with a rallying cry as the title takes zero, because people vote it up without even reading it.  

对于首页来说，最危险的事情是太容易投票的内容。如果有人证明了一个新定理，读者需要花一些功夫来决定是否投票。一部有趣的动画片需要更少的时间。标题中带有战斗口号的咆哮为零，因为人们甚至没有阅读它就投票了。

Hence what I call the Fluff Principle: on a user-voted news site, the links that are easiest to judge will take over unless you take specific measures to prevent it.  

因此，我称之为“绒毛原则”：在用户投票的新闻网站上，最容易判断的链接将接管，除非您采取具体措施来防止它。

Hacker News has two kinds of protections against fluff. The most common types of fluff links are banned as off-topic. Pictures of kittens, political diatribes, and so on are explicitly banned. This keeps out most fluff, but not all of it. Some links are both fluff, in the sense of being very short, and also on topic.  

黑客新闻有两种针对绒毛的保护措施。最常见的绒毛链接类型因偏离主题而被禁止。小猫的照片、政治谩骂等等都是明确禁止的。这可以阻挡大部分绒毛，但不是全部。有些链接既简短又切题，毫无意义。

There's no single solution to that. If a link is just an empty rant, editors will sometimes kill it even if it's on topic in the sense of being about hacking, because it's not on topic by the real standard, which is to engage one's intellectual curiosity. If the posts on a site are characteristically of this type I sometimes ban it, which means new stuff at that url is auto-killed. If a post has a linkbait title, editors sometimes rephrase it to be more matter-of-fact. This is especially necessary with links whose titles are rallying cries, because otherwise they become implicit "vote up if you believe such-and-such" posts, which are the most extreme form of fluff.  

对此没有单一的解决方案。如果一个链接只是空洞的咆哮，编辑有时会删除它，即使它是关于黑客的主题，因为它不是真正的标准，即激发人们的求知欲。如果网站上的帖子具有这种类型的特点，我有时会禁止它，这意味着该网址上的新内容会被自动删除。如果一篇文章有一个链接诱饵标题，编辑有时会改写它，使其更实际。对于标题为战斗口号的链接来说，这一点尤其必要，因为否则它们就会变成隐含的“如果你相信某事就投票”的帖子，这是最极端的废话形式。

The techniques for dealing with links have to evolve, because the links do. The existence of aggregators has already affected what they aggregate. Writers now deliberately write things to draw traffic from aggregators—sometimes even specific ones. (No, the irony of this statement is not lost on me.) Then there are the more sinister mutations, like linkjacking—posting a paraphrase of someone else's article and submitting that instead of the original. These can get a lot of upvotes, because a lot of what's good in an article often survives; indeed, the closer the paraphrase is to plagiarism, the more survives.  

处理链接的技术必须不断发展，因为链接也在不断发展。聚合器的存在已经影响了它们聚合的内容。作家现在故意写一些东西来吸引聚合器的流量——有时甚至是特定的流量。 （不，我并没有忽视这句话的讽刺意味。）然后还有更险恶的突变，比如链接劫持——发布别人文章的释义并提交它而不是原文。这些可以得到很多点赞，因为一篇文章中的很多好东西往往会被保留下来；事实上，释义越接近抄袭，流传下来的就越多。

\[[3](http://www.paulgraham.com/hackernews.html#f3n)\]

I think it's important that a site that kills submissions provide a way for users to see what got killed if they want to. That keeps editors honest, and just as importantly, makes users confident they'd know if the editors stopped being honest. HN users can do this by flipping a switch called showdead in their profile.  

我认为删除提交的网站必须为用户提供一种方式，让他们可以根据需要查看哪些内容被删除，这一点很重要。这让编辑保持诚实，同样重要的是，让用户相信他们会知道编辑是否不再诚实。 HN 用户可以通过点击其个人资料中名为 showdead 的开关来完成此操作。

\[[4](http://www.paulgraham.com/hackernews.html#f4n)\]

**Comments 评论**

Bad comments seem to be a harder problem than bad submissions. While the quality of links on the frontpage of HN hasn't changed much, the quality of the median comment may have decreased somewhat.  

不良评论似乎比不良提交更难解决。虽然 HN 首页上的链接质量没有太大变化，但中值评论的质量可能有所下降。

There are two main kinds of badness in comments: meanness and stupidity. There is a lot of overlap between the two—mean comments are disproportionately likely also to be dumb—but the strategies for dealing with them are different. Meanness is easier to control. You can have rules saying one shouldn't be mean, and if you enforce them it seems possible to keep a lid on meanness.  

评论中的坏处主要有两种：卑鄙和愚蠢。两者之间有很多重叠之处——刻薄的评论也很可能是愚蠢的——但处理它们的策略是不同的。卑鄙更容易控制。你可以制定规则，规定一个人不应该卑鄙，如果你执行这些规则，似乎就有可能限制卑鄙行为。

Keeping a lid on stupidity is harder, perhaps because stupidity is not so easily distinguishable. Mean people are more likely to know they're being mean than stupid people are to know they're being stupid.  

控制愚蠢行为更加困难，也许是因为愚蠢行为并不那么容易区分。卑鄙的人比愚蠢的人更有可能知道自己卑鄙。

The most dangerous form of stupid comment is not the long but mistaken argument, but the dumb joke. Long but mistaken arguments are actually quite rare. There is a strong correlation between comment quality and length; if you wanted to compare the quality of comments on community sites, average length would be a good predictor. Probably the cause is human nature rather than anything specific to comment threads. Probably it's simply that stupidity more often takes the form of having few ideas than wrong ones.  

最危险的愚蠢评论不是冗长但错误的论点，而是愚蠢的笑话。冗长但错误的论证实际上很少见。评论质量和评论长度之间存在很强的相关性；如果您想比较社区网站上评论的质量，平均长度将是一个很好的预测指标。原因可能是人性，而不是评论线程的任何特定原因。也许只是因为愚蠢更多地表现为想法很少，而不是错误的想法。

Whatever the cause, stupid comments tend to be short. And since it's hard to write a short comment that's distinguished for the amount of information it conveys, people try to distinguish them instead by being funny. The most tempting format for stupid comments is the supposedly witty put-down, probably because put-downs are the easiest form of humor.  

不管出于什么原因，愚蠢的评论往往很短。由于很难写出一条简短的评论来区分其所传达的信息量，因此人们试图通过搞笑来区分它们。愚蠢评论最诱人的形式是所谓的诙谐的贬低，可能是因为贬低是最简单的幽默形式。

\[[5](http://www.paulgraham.com/hackernews.html#f5n)\] So one advantage of forbidding meanness is that it also cuts down on these.  

因此，禁止卑鄙行为的好处之一就是它也可以减少这些行为。

Bad comments are like kudzu: they take over rapidly. Comments have much more effect on new comments than submissions have on new submissions. If someone submits a lame article, the other submissions don't all become lame. But if someone posts a stupid comment on a thread, that sets the tone for the region around it. People reply to dumb jokes with dumb jokes.  

不好的评论就像野葛一样：它们会迅速占据主导地位。评论对新评论的影响比提交对新提交的影响大得多。如果有人提交了一篇蹩脚的文章，其他提交的文章不会全部变得蹩脚。但如果有人在某个话题上发表了愚蠢的评论，就会为该话题周围的地区定下基调。人们用愚蠢的笑话来回答愚蠢的笑话。

Maybe the solution is to add a delay before people can respond to a comment, and make the length of the delay inversely proportional to some prediction of its quality. Then dumb threads would grow slower.  

也许解决方案是在人们回复评论之前添加延迟，并使延迟的长度与对其质量的某些预测成反比。那么哑线程就会增长得更慢。

\[[6](http://www.paulgraham.com/hackernews.html#f6n)\]

**People 人们**

I notice most of the techniques I've described are conservative: they're aimed at preserving the character of the site rather than enhancing it. I don't think that's a bias of mine. It's due to the shape of the problem. Hacker News had the good fortune to start out good, so in this case it's literally a matter of preservation. But I think this principle would also apply to sites with different origins.  

我注意到我所描述的大多数技术都是保守的：它们的目的是保留网站的特征而不是增强它。我不认为这是我的偏见。这是由于问题的形状造成的。 《黑客新闻》有幸一开始就很好，所以在这种情况下，这实际上是一个保存问题。但我认为这个原则也适用于不同来源的网站。

The good things in a community site come from people more than technology; it's mainly in the prevention of bad things that technology comes into play. Technology certainly can enhance discussion. Nested comments do, for example. But I'd rather use a site with primitive features and smart, nice users than a more advanced one whose users were idiots or [trolls](http://www.paulgraham.com/trolls.html).  

社区网站中的好东西更多来自于人而不是技术；技术的作用主要是在预防坏事方面发挥作用。技术当然可以加强讨论。例如，嵌套注释就是如此。但我宁愿使用一个具有原始功能和聪明、友善的用户的网站，也不愿使用一个用户是白痴或巨魔的更高级的网站。

So the most important thing a community site can do is attract the kind of people it wants. A site trying to be as big as possible wants to attract everyone. But a site aiming at a particular subset of users has to attract just those—and just as importantly, repel everyone else. I've made a conscious effort to do this on HN. The graphic design is as plain as possible, and the site rules discourage dramatic link titles. The goal is that the only thing to interest someone arriving at HN for the first time should be the ideas expressed there.  

因此，社区网站最重要的事情就是吸引它想要的人。一个试图尽可能大的网站想要吸引所有人。但针对特定用户群体的网站必须吸引这些用户，而且同样重要的是，排斥其他用户。我在 HN 上有意识地努力做到这一点。图形设计尽可能简单，并且站点规则不鼓励戏剧性的链接标题。我们的目标是，让第一次来到 HN 的人感兴趣的唯一事情就是那里表达的想法。

The downside of tuning a site to attract certain people is that, to those people, it can be too attractive. I'm all too aware how addictive Hacker News can be. For me, as for many users, it's a kind of virtual town square. When I want to take a break from working, I walk into the square, just as I might into Harvard Square or University Ave in the physical world.  

调整网站以吸引某些人的缺点是，对于这些人来说，它可能太有吸引力。我非常清楚黑客新闻是多么让人上瘾。对于我和许多用户来说，这是一种虚拟的城镇广场。当我想在工作之余休息一下时，我就会走进广场，就像我走进现实世界中的哈佛广场或大学大道一样。

\[[7](http://www.paulgraham.com/hackernews.html#f7n)\] But an online square is more dangerous than a physical one. If I spent half the day loitering on University Ave, I'd notice. I have to walk a mile to get there, and sitting in a cafe feels different from working. But visiting an online forum takes just a click, and feels superficially very much like working. You may be wasting your time, but you're not idle. Someone is [wrong](http://xkcd.com/386/) on the Internet, and you're fixing the problem.  

但网上广场比实体广场更危险。如果我在大学大街闲逛半天，我就会注意到。我必须步行一英里才能到达那里，坐在咖啡馆里的感觉与工作不同。但访问在线论坛只需点击一下，表面上感觉非常像工作。你可能在浪费时间，但你并没有闲着。互联网上有人犯了错误，而你正在解决问题。

Hacker News is definitely useful. I've learned a lot from things I've read on HN. I've written several essays that began as comments there. So I wouldn't want the site to go away. But I would like to be sure it's not a net drag on productivity. What a disaster that would be, to attract thousands of smart people to a site that caused them to waste lots of time. I wish I could be 100% sure that's not a description of HN.  

黑客新闻绝对有用。我从 HN 上读到的东西中学到了很多东西。我写了几篇文章，都是以评论开始的。所以我不希望这个网站消失。但我想确定这不会对生产力造成净拖累。如果吸引了成千上万的聪明人来到一个导致他们浪费大量时间的网站，那将是一场多么大的灾难啊。我希望我能 100% 确定这不是对 HN 的描述。

I feel like the addictiveness of games and social applications is still a mostly unsolved problem. The situation now is like it was with crack in the 1980s: we've invented terribly addictive new things, and we haven't yet evolved ways to protect ourselves from them. We will eventually, and that's one of the problems I hope to focus on next.  

我觉得游戏和社交应用程序的成瘾性仍然是一个尚未解决的问题。现在的情况就像 20 世纪 80 年代的情况一样：我们发明了非常容易上瘾的新事物，但我们还没有进化出保护自己免受它们侵害的方法。我们最终会的，这是我希望接下来关注的问题之一。

**Notes 笔记**

\[

1\] I tried ranking users by both average and median comment score, and average (with the high score thrown out) seemed the more accurate predictor of high quality. Median may be the more accurate predictor of low quality though.  

\] 我尝试根据平均评论分数和中位数评论分数对用户进行排名，平均分数（排除高分）似乎更准确地预测高质量。不过，中位数可能是低质量的更准确的预测指标。

\[

2\] Another thing I learned from this experiment is that if you're going to distinguish between people, you better be sure you do it right. This is one problem where rapid prototyping doesn't work.  

\] 我从这个实验中学到的另一件事是，如果你要区分不同的人，你最好确保你做得正确。这是快速原型设计无法解决的问题之一。

Indeed, that's the intellectually honest argument for not discriminating between various types of people. The reason not to do it is not that everyone's the same, but that it's bad to do wrong and hard to do right.  

事实上，这是不歧视不同类型的人的理智上诚实的论点。不这样做的原因并不是每个人都一样，而是做错了不好，做对了很难。

\[

3\] When I catch egregiously linkjacked posts I replace the url with that of whatever they copied. Sites that habitually linkjack get banned.  

\] 当我发现严重被链接劫持的帖子时，我会将网址替换为他们复制的内容。习惯性链接劫持的网站会被禁止。

\[

4\] Digg is notorious for its lack of transparency. The root of the problem is not that the guys running Digg are especially sneaky, but that they use the wrong algorithm for generating their frontpage. Instead of bubbling up from the bottom as they get more votes, as on Reddit, stories start at the top and get pushed down by new arrivals.  

\] Digg 因缺乏透明度而臭名昭著。问题的根源并不在于运行 Digg 的人特别狡猾，而是他们使用了错误的算法来生成首页。故事不像 Reddit 那样，随着获得更多选票而从底部冒出来，而是从顶部开始，然后被新来的人推到下面。

The reason for the difference is that Digg is derived from Slashdot, while Reddit is derived from Delicious/popular. Digg is Slashdot with voting instead of editors, and Reddit is Delicious/popular with voting instead of bookmarking. (You can still see fossils of their origins in their graphic design.)  

造成差异的原因是 Digg 源自 Slashdot，而 Reddit 源自 Delicious/popular。 Digg 是 Slashdot，用投票代替编辑，Reddit 是美味/流行，用投票代替书签。 （您仍然可以在其图形设计中看到其起源的化石。）

Digg's algorithm is very vulnerable to gaming, because any story that makes it onto the frontpage is the new top story. Which in turn forces Digg to respond with extreme countermeasures. A lot of startups have some kind of secret about the subterfuges they had to resort to in the early days, and I suspect Digg's is the extent to which the top stories were de facto chosen by human editors.  

Digg 的算法很容易受到游戏的影响，因为任何登上首页的故事都是新的头条新闻。这反过来又迫使 Digg 采取极端的应对措施。许多初创公司对他们在早期不得不采取的诡计都有某种秘密，我怀疑 Digg 的秘密是头条新闻实际上是由人类编辑选择的程度。

\[

5\] The dialog on Beavis and Butthead was composed largely of these, and when I read comments on really bad sites I can hear them in their voices.  

\] Beavis 和 Butthead 的对话主要由这些内容组成，当我读到非常糟糕的网站上的评论时，我可以从他们的声音中听到他们的声音。

\[

6\] I suspect most of the techniques for discouraging stupid comments have yet to be discovered. Xkcd implemented a particularly clever one in its IRC channel: don't allow the same thing twice. Once someone has said "fail," no one can ever say it again. This would penalize short comments especially, because they have less room to avoid collisions in.  

\] 我怀疑大多数阻止愚蠢评论的技术尚未被发现。 Xkcd 在其 IRC 频道中实现了一个特别聪明的功能：不允许同一件事两次。一旦有人说过“失败”，就没有人可以再说一遍。这将特别惩罚短评论，因为它们避免冲突的空间较小。

Another promising idea is the [stupid filter](http://stupidfilter.org/), which is just like a probabilistic spam filter, but trained on corpora of stupid and non-stupid comments instead.  

另一个有前途的想法是愚蠢的过滤器，它就像概率垃圾邮件过滤器一样，但是是在愚蠢和非愚蠢评论的语料库上进行训练的。

You may not have to kill bad comments to solve the problem. Comments at the bottom of a long thread are rarely seen, so it may be enough to incorporate a prediction of quality in the comment sorting algorithm.  

您可能不必删除不好的评论来解决问题。长线程底部的评论很少见，因此在评论排序算法中纳入质量预测可能就足够了。

\[

7\] What makes most suburbs so demoralizing is that there's no center to walk to.  

\] 大多数郊区之所以如此令人沮丧，是因为没有中心可以步行到达。

**Thanks** to Justin Kan, Jessica Livingston, Robert Morris, Alexis Ohanian, Emmet Shear, and Fred Wilson for reading drafts of this.  

感谢 Justin Kan、Jessica Livingston、Robert Morris、Alexis Ohanian、Emmet Shear 和 Fred Wilson 阅读本文的草稿。



[Comment  评论](http://news.ycombinator.com/item?id=495053) on this essay.  关于这篇论文。
