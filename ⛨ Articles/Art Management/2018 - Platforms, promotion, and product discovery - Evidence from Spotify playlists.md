# **Platforms, promotion, and product discovery：Evidence from Spotify playlists**
**平台、推广与产品发现：来自 Spotify 播放列表的证据**

> LUIS AGUIAR, JOEL WALDFOGEL

© 2018 by Luis Aguiar and Joel Waldfogel. All rights reserved. Short sections of text, not to exceed two paragraphs, may be quoted without explicit permission provided that full credit, including © notice, is given to the source.

# ABSTRACT

Digitization has vastly increased the amount of new music produced and available directly to consumers. While this has levelled the playing field between already-prominent and new artists, creators may now be dependent on platform decisions about which songs and artist to promote. With Spotify emerging as a major interactive streaming platform, this paper explores the effect of Spotify's playlists on both the promotion of songs and the discovery of music by new artists, using four approaches. First, we examine songs' streaming volumes before and after their addition to, and removal from, major global playlists. Second, we compare streaming volumes for songs just on, and just off, algorithmic top 50 playlists. Third, we make use of cross-country differences in inclusion on New Music Friday lists, using song fixed effects to explain differences in streaming. Fourth, we develop an instrumental variables approach to explaining cross-country New Music Friday rank differentials based on home bias. Being added to Today's Top Hits, a list with 18.5 million followers during the sample period, raises streams by almost 20 million and is worth between $123,400 and $163,000. Inclusion on New Music Friday lists substantially raises the probability of song success, including for new artists.

> 数字化极大地增加了新音乐的制作数量，并使其能够直接触达消费者。尽管这缩小了知名艺人与新兴艺人之间的竞争差距，但创作者如今可能依赖于平台关于推广哪些歌曲和艺人的决策。随着 Spotify 崛起为主要互动流媒体平台，本文通过四种方法探讨了 Spotify 播放列表对歌曲推广和新艺人音乐发现的影响。首先，我们考察了歌曲在加入和移出主要全球播放列表前后的流媒体播放量变化。其次，我们比较了恰好进入算法生成的热门 50 播放列表与恰好未进入该列表的歌曲的流媒体播放量。第三，我们利用《新音乐星期五》列表在不同国家的收录差异，结合歌曲固定效应来解释流媒体播放量的区别。第四，我们开发了一种工具变量方法，基于本土偏好来解释跨国《新音乐星期五》排名差异。被加入《今日热门歌曲》列表（该列表在样本期内拥有 1850 万关注者）可使歌曲流量增加近 2000 万次，价值介于 123,400 美元至 163,000 美元之间。入选《新音乐星期五》列表能显著提高歌曲成功的概率，对新艺人而言亦是如此。

# 1 INTRODUCTION

Digitization has stimulated substantial growth in new song production and has, with the development of online music streaming, also broken the traditional promotion and distribution bottlenecks inherent in terrestrial radio and traditional music retailing.[^1] During 2016, Spotify added over half a million (567,693) songs to its catalog and during 2017 nearly an additional million (934,265).[^2] As a result, Spotify users have access to 35 million tracks via any Internet-connected device.[^3] Consumers' access to large catalogs, and the converse - that creators, not just those from established record labels, have access to large audiences - are on their face a substantial levelling of the playing field, holding out the promise of deconcentrating consumption toward a long tail of products hailing from diverse sources such as independent record labels and foreign producers.[^4]

> 数字化刺激了新歌曲产量的显著增长，并且随着在线音乐流媒体技术的发展，也打破了地面广播与传统音乐零售中固有的推广及分销瓶颈。[^1] 在 2016 年，Spotify 向其曲库中添加了超过五十万（567,693）首歌曲，并于 2017 年再次增加了近一百万（934,265）首。[^2] 因此，Spotify 用户能够通过任何联网设备访问 3500 万首曲目。[^3] 消费者能够获取庞大的曲库，反之亦然——创作者，不仅限于那些来自知名唱片公司的创作者，也能够接触到广大听众——这表面上显著平衡了竞争环境，并展现出将消费分散化、转向来自独立唱片公司及外国制作人等多元来源的长尾产品的潜力。[^4]

Access to an increasingly large catalog creates a daunting problem of product discovery, however. Beyond getting consumers access to a large catalog, a major value-creating function of a platform is helping consumers to discover music that they like. Broadly speaking, platforms do this in two ways. First, they create personalized music suggestions, via individual playlists such as Spotify's Discover Weekly, or Pandora's song- or artist-seeded individual stations. These systems have been the subject of much research on recommender systems and music taxonomy (see, for example, Adomavicius and Tuzhilin, 2005). Second, platforms promote discovery via general, i.e. one-to-many, playlists. Some of these lists - like Spotify's Today's Top Hits - are curated using human discretion and are often used to promote songs and artists that are already widely known. Other curated lists - like Spotify's New Music Friday - are more specifically dedicated to the discovery of new songs and artists. Algorithmic playlists - like the Global Top 50 or the U.S. Viral Top 50 - are, on the other hand, based algorithmically on streaming charts rather than human curators.

> 然而，访问日益增大的目录带来了产品发现的艰巨问题。除了让消费者访问大型目录外，平台的一个主要价值创造功能是帮助消费者发现他们喜欢的音乐。广义上说，平台通过两种方式做到这一点。首先，他们通过个性化播放列表创建个性化的音乐建议，例如 Spotify 的 Discover Weekly，或 Pandora 的基于歌曲或艺术家的个人电台。这些系统一直是推荐系统和音乐分类学大量研究的主题（例如，参见 Adomavicius 和 Tuzhilin，2005年）。其次，平台通过通用，即一对多，播放列表来促进发现。其中一些列表——比如 Spotify 的 Today's Top Hits——是使用人工判断策划的，通常用于推广已经广为人知的歌曲和艺术家。其他策划列表——比如 Spotify 的 New Music Friday——更专门致力于新歌曲和艺术家的发现。算法播放列表——比如 Global Top 50 或 U.S. Viral Top 50——另一方面，是基于算法的流媒体图表，而非人工策划者。

The interactive music streaming market has a number of major participants, including Spotify as well as services from Apple Music and Google.[^5] Spotify is growing quickly, and in 2017 Spotify was reported to have a 37 percent share of the subscription streaming market.[^6]

> 交互式音乐流媒体市场有多个主要参与者，包括 Spotify 以及来自 Apple Music 和 Google.[^5] 的服务。Spotify 增长迅速，并且在 2017 年，据报道 Spotify 占据了订阅流媒体市场的 37% 份额。[^6]

With Spotify emerging as the leading interactive streaming service, it is interesting to explore whether Spotify influences consumption choices through its general playlists, which function in two ways. First, playlists are potentially informative lists of songs that can simply make users aware of particular songs. Second, playlists are utilities for listening to music: a user who subscribes to a playlist can select it, then automatically play its songs in either rank or random order. Users opt into playlists by subscribing to them at no cost, and the most popular playlists have nearly 20 million subscribers. These developments raise questions about how and whether playlists affect consumption choices and promote the discovery of new songs and artists.

> 随着 Spotify 崛起成为领先的交互式流媒体服务，探讨其通用播放列表是否影响消费选择显得尤为有趣，这些播放列表主要通过两种方式发挥作用。首先，播放列表作为潜在的歌曲信息列表，能够使用户了解特定歌曲的存在。其次，播放列表是收听音乐的实用工具：订阅播放列表的用户可以选择列表，然后按排名或随机顺序自动播放其中的歌曲。用户可通过免费订阅的方式选择加入播放列表，其中最受欢迎的播放列表拥有近 2000 万订阅者。这些发展引发了关于播放列表如何以及是否影响消费选择、并促进新歌曲与新艺术家被发现的问题。

Growing concentration in the streaming market puts streaming platforms among the handful of online platforms that have come to dominate, or nearly dominate, their respective markets in search advertising (Google), social networking (Facebook), online retailing (Amazon), and others. Some observers warn of a new era of "Internet monopoly" and call for heightened antitrust enforcement.[^7] The usual concern about market dominance is that firms with market power will harm consumers by charging high prices. While the major platforms do not charge consumers high prices - and in many cases do not charge consumers at all - dominant platforms warrant attention even if they do not deliver high prices to consumers.[^8] Platforms are sometimes alleged to affect the fortunes of their suppliers, and in the music context, platforms can play important roles in determining song and artist success, including the determination of which songs and artists are discovered in the first place.[^8] While Spotify is not a music producer, the major record labels have substantial ownership stakes in Spotify. Sony BMG owns 5.8 percent, Universal owns 4.8 percent, Warner Music owns 3.8 percent, and EMI has 1.9 percent. Merlin, which represents many independent record labels, owns 1 percent.[^10] It is therefore of interest to understand the extent of a prominent platform's ability to influence which songs and artists succeed.

> 流媒体市场日益集中的态势，使流媒体平台跻身于少数几家主导或近乎主导各自市场的在线平台之列，这些市场涵盖搜索广告（Google）、社交网络（Facebook）、在线零售（Amazon）等领域。部分观察者警示“互联网垄断”新时代的来临，并呼吁加强反垄断执法。[^7] 关于市场主导地位的常见担忧在于，拥有市场力量的企业可能通过收取高价损害消费者利益。尽管主要平台并未向消费者收取过高费用——甚至多数情况下完全免费——但即使未导致高价格，主导平台仍值得关注。[^8] 平台有时被指会影响其供应商的命运，在音乐领域，平台对歌曲和艺术家的成功起着关键作用，甚至能决定哪些歌曲与艺术家得以被发掘。[^9] 虽然 Spotify 并非音乐制作方，但主要唱片公司在 Spotify 持有大量所有权股份。其中索尼 BMG 持股 5.8%，环球音乐持股 4.8%，华纳音乐持股 3.8%，百代唱片持股 1.9%。代表众多独立唱片公司的 Merlin 则持有 1% 股份。[^10] 因此，探究知名平台能在多大程度上影响歌曲与艺术家的成功，具有重要研究价值。

Against this backdrop, this paper explores whether Spotify has the ability to influence users' listening decisions. First, we ask whether playlist inclusion affects the number of streams that songs receive. Second, we ask the related but distinct question of whether playlist inclusion decisions affect consumers' discovery of new songs and artists. These questions recall the traditional question of whether promotion on radio stimulates music sales, one that is empirically challenging to address because playlist and airplay decisions are endogenous: curators choose songs they expect will be popular. We employ four empirical approaches to measure the impact of playlist inclusion on song performance. (1) We use the discontinuous jumps in the number of songs' playlists followers when widely followed lists add a song. (2) For algorithmic playlists where we know the inclusion criterion, we compare streams of songs just making the list with songs just off the list to measure the impact of list inclusion on streams. (3) We exploit differential song rankings on equivalent (New Music Friday) playlists across countries to measure the impact of list rankings on product discovery and streams. (4) We develop an instrumental variables approach to explain cross-country differences in New Music Friday rankings based on home bias in New Music Friday lists, along with the size of domestic music markets. Larger markets have more domestic music, giving rise to worse ranks for foreign songs in larger markets. Finally, we also explore who benefits from Spotify playlists, i.e. the sorts of songs - according to label type and artist national origin - that are included on playlists.

> 在此背景下，本文探讨了 Spotify 是否具备影响用户收听决策的能力。首先，我们探究播放列表的收录是否会改变歌曲获得的流媒体播放量。其次，我们提出一个相关但不同的问题：播放列表的收录决策是否会影响消费者对新歌曲和新艺术家的发现。这些问题呼应了传统研究中关于电台推广是否刺激音乐销售的议题，而其实证研究面临挑战，因为播放列表和电台播放决策具有内生性：策展人会选择他们预期会受欢迎的歌曲。我们采用四种实证方法来衡量播放列表收录对歌曲表现的影响。
> 
> (１) 利用被广泛关注的播放列表在添加歌曲时，其关注者数量出现的间断性跃升。
> 
> (２) 针对我们已知收录标准的算法播放列表，通过比较刚刚入选列表的歌曲与刚刚落选的歌曲的流媒体播放量，来衡量列表收录的影响。
> 
> (３) 我们利用等效播放列表（如 New Music Friday）在不同国家间的歌曲排名差异，来衡量列表排名对产品发现和流媒体播放量的影响。
> 
> (４) 我们开发了一种工具变量方法，基于 New Music Friday 列表中的本土偏好以及国内音乐市场的规模，来解释 New Music Friday 排名在跨国间的差异。市场规模越大，本土音乐越多，导致外国歌曲在较大市场中的排名更靠后。
> 
> 最后，我们也探讨了谁从 Spotify 播放列表中受益，即根据厂牌类型和艺术家国籍，哪些类型的歌曲被收录进播放列表。

We have three broad findings. First, the major platform-operated playlists have large and significant causal impacts on streaming, so the platform has power to influence consumption decisions, even among songs and artists that are already widely known. Appearing on Today's Top Hits, a list with 18.5 million followers during the sample period, raises a song's eventual streams by almost 20 million, which is almost a quarter of the average value of streams for songs that make that playlist. Being on the Global Top 50 list raises a song's streams by about 3 million, or by about 3.3 percent of the average streams for songs that make the Global Top 50. Second, Spotify also has substantial effects on which new artists and songs become discovered. Being ranked #1 on the U.S. New Music Friday list raises a song's streams by about 14 million. Third, most of the benefit of the global lists accrues to US-origin major-label songs, while the New Music Friday lists have larger representation from domestic and independent-label music.

> 我们有三项主要发现。首先，主要平台运营的播放列表对流媒体有巨大且显著的因果影响，因此平台有能力影响消费决策，即使是那些已经广为人知的歌曲和艺术家。出现在 Today's Top Hits 上（在样本期间拥有 18.5 百万关注者），会使一首歌曲的最终流媒体播放量增加近 20 百万，这几乎是进入该播放列表歌曲平均流媒体值的四分之一。进入 Global Top 50 列表会使一首歌曲的流媒体播放量增加约 3 百万，或约为进入 Global Top 50 歌曲平均流媒体播放量的 3.3 %。其次，Spotify 也对哪些新艺术家和歌曲被发现产生重大影响。在 U.S. New Music Friday 列表中排名第一会使一首歌曲的流媒体播放量增加约 14 百万。第三，全球列表的大部分好处归于美国起源的主流唱片公司歌曲，而 New Music Friday 列表则更多地代表国内和独立唱片公司的音乐。

This paper proceeds in 6 sections after the introduction. Section 2 provides background on the various types of playlists as well as their functions; and the section discusses the literature related to our study. Section 3 describes our data sources. Section 4 presents estimates of the effects of inclusion on Spotify's major global playlists on streams. Section 5 describes our various identification strategies for measuring the effects of the New Music Friday lists on product and artist discovery and discusses estimation results. Section 6 descriptively explores the types of songs - by label type and national origin - that are included in various playlists. Section 7 concludes.

> 本文在引言之后分为 6 个部分展开。第 2 节介绍了各类播放列表及其功能的背景；同时该节讨论了与本研究相关的文献。第 3 节描述了我们的数据来源。第 4 节展示了入选 Spotify 全球主要播放列表对流媒体播放量的影响估计。第 5 节阐述了我们衡量“新音乐星期五”列表对作品与艺人发现效果的各种识别策略，并讨论了估计结果。第 6 节通过描述性分析探讨了各类播放列表中收录的歌曲类型——按厂牌类型与国家来源划分。第 7 节为结论部分。

## Notes

[^1]: See, for example, Waldfogel, 2017.

[^2]: See [http://everynoise.com/sorting_hat_closet/](http://everynoise.com/sorting_hat_closet/) for weekly lists of songs added to Spotify.

[^3]: See United States Securities and Exchange Commission (2018).

[^4]: See, for example, Zentner et al. (2013) showing that video consumption deconcentrates when consumers have access to an online selection.

[^5]: See [http://www.businessinsider.com/google-reshuffles-its-music-products-2017-2](http://www.businessinsider.com/google-reshuffles-its-music-products-2017-2).

[^6]: See [https://www.statista.com/statistics/653926/music-streaming-service-subscriber-sha](https://www.statista.com/statistics/653926/music-streaming-service-subscriber-sha)

[^7]: For example the Open Markets Institute argues that "Online intermediaries have emerged as the railroad monopolies of the 21st century, controlling access to market and increasingly determining who wins and who loses in today's economy." See [https://openmarketsinstitute.org/issues/tech-platforms/](https://openmarketsinstitute.org/issues/tech-platforms/). George Soros has argued that the "fact that they are near-monopoly distributors makes them public utilities and should subject them to more stringent regulations, aimed at preserving competition, innovation, and fair and open universal access." See Porzecanski (2018).

[^8]: See Ip (2018).

[^9]: See Edelman (2011) and Zhu and Liu (2016).

[^10]: See Lindvall (2009) and Arrington (2009).

# 2 BACKGROUND ON PLAYLISTS
**播放列表背景信息**
## 2.1 The Types and Functions of Playlists
**播放列表的类型与功能**

Playlists have two broad functions. They are both potentially informative lists of songs, as well as utilities for playing the songs on those lists. Anyone is free to create and share playlists, and many individuals do so. For example, Napster co-founder and early Facebook investor Sean Parker maintains an influential list called "Hipster International," which is widely credited with making New Zealand-based artist Lorde into an international superstar.[^11] In addition to independent individuals, various other kinds of entities maintain playlists. For example, the major record labels, Warner, Universal, and Sony, operate playlists through Digster, Topsify, and Filtr brands respectively.

> 播放列表有两个主要功能。它们既是潜在的信息性歌曲列表，也是播放这些列表中歌曲的工具。任何人都可以自由创建和分享播放列表，许多人确实这样做。例如，Napster 联合创始人和早期 Facebook 投资者 Sean Parker 维护着一个名为“Hipster International”的有影响力的列表，它被广泛认为使新西兰艺术家 Lorde 成为国际巨星。[^11] 除了独立的个人之外，各种其他类型的实体也维护播放列表。例如，主要唱片公司 Warner、Universal 和 Sony 分别通过 Digster、Topsify 和 Filtr 品牌运营播放列表。

Spotify itself maintains both curated and chart-based algorithmic general playlists, as well as playlists that are customized to each user. These different playlists work in different ways. Among the lists that are not tailored to individual users, lists vary along two dimensions: whether they are algorithmic or curated by humans and whether they are global or countryspecific. These dimensions in turn determine the empirical strategy that we use to identify the causal effects of list inclusion.

> Spotify 平台自身既维护着由人工精选和基于排行榜算法生成的通用播放列表，也维护着为每位用户个性化定制的播放列表。这些不同类型的播放列表以不同的方式运作。在非针对个人用户定制的列表中，列表在两个维度上存在差异：一是基于算法生成还是由人工策划，二是全球通用还是针对特定国家。这些维度进而决定了我们用于识别列表收录因果效应的实证研究策略。

Playlists like Today's Top Hits, RapCaviar, Baila Reggaeton, and Viva Latino are all global lists that are curated by Spotify employees, who choose songs for inclusion on the lists. These lists generally add songs that have been streamed on Spotify for some period of time and include songs and artists that are already widely known. These playlists are therefore likely to be used as utilities for listening to the songs that they include, rather than as sources of information revealing heretofore obscure songs or artists. (The fact that songs appearing on these lists have already been streamed on Spotify nevertheless has the advantage that one may be able to measure the impact of appearing on one of these lists from the changes in streams right around the time that the song appears on the list.) Spotify tests songs on playlists with smaller followings, then promotes promising songs to the major global lists with wide followings. "By the time a song lands on Today's Top Hits or other equally popular sets, Spotify has so relentlessly tested it that it almost can't fail."[^12] The day that a song appears on a particular playlist, the list's followers now can see the song on a playlist to which they subscribe. Hence, the number of the song's followers rises by the number of playlist follower when the add occurs. Other playlists, too, can add the song at or around the same date, so the number of playlist followers that a song has can jump by more than the number of followers of the list in question.

> 诸如 Today's Top Hits、RapCaviar、Baila Reggaeton 以及 Viva Latino 等播放列表均属于全球性榜单，由 Spotify 员工负责策划并筛选收录曲目。这些列表通常添加已在 Spotify 平台积累一定时期播放量的歌曲，其中包含的曲目与艺人往往已具备较高知名度。因此，此类播放列表更可能被用作收听所含歌曲的实用工具，而非用于发掘此前鲜为人知的歌曲或艺人的信息来源。（尽管如此，出现在这些列表中的歌曲此前已在 Spotify 上产生播放记录的事实仍具优势——人们或许能通过歌曲上榜前后播放量的变化，来衡量登上此类列表所产生的影响。）Spotify 会先在粉丝基数较小的播放列表上测试歌曲，随后将表现优异的作品推广至粉丝量庞大的主流全球榜单。“当一首歌登上 Today's Top Hits 或其他同等热度的歌单时，Spotify 已对其进行过如此严苛的测试，以至于它几乎不可能失败。”[^12] 当歌曲在某日被添加至特定播放列表时，该列表的关注者便能在其订阅的歌单中看到这首作品。因此，歌曲被添加当日，其关注者数量将增加相当于该播放列表关注人数的数值。其他播放列表亦可能在相同或相近日期添加此歌曲，故一首歌的播放列表关注总量可能远超单一列表的关注人数。

The New Music Friday playlists are also curated by Spotify but are country-specific and are updated every Friday, when 50 new songs are added to the list for each country. Because songs are added to the New Music Friday list for only a week - and because the added songs are generally added when they are literally new to Spotify - these playlists bring new information in addition to functioning as utilities for listening to the new music that they present. From that perspective, the New Music Friday lists have the possibility of promoting the discovery of new songs and artists. The drawback is that there is generally no streaming history for dates prior to the songs' inclusion on the lists, which makes it impossible to measure the impact of list inclusion from examining how streams change as the songs move to these lists.

> New Music Friday 播放列表同样由 Spotify 策划，但针对不同国家定制，并于每周五更新，每个国家的列表将添加 50 首新歌曲。由于歌曲仅在 New Music Friday 列表中存在一周——且添加的歌曲通常是在其刚登陆 Spotify 时即被收录——这些播放列表除了作为收听新音乐的工具外，还带来了新的信息。从这一角度来看，New Music Friday 列表有可能促进新歌曲和艺术家的发现。其不足之处在于，歌曲在列入列表之前的日期通常没有流媒体历史记录，这使得通过观察歌曲进入列表后流量的变化来衡量列表收录的影响变得不可能。

Spotify has a widely followed Global Top 50 list, which algorithmically includes the top 50 songs of the previous day according to streams. Spotify also maintains the corresponding Top 50 lists for each country, which are based on the country-specific streams from the previous day. Because the inclusion criteria for these lists is transparent, one can compare streams of songs just making the list to identify the effect of inclusion on the Top 50 lists.

> Spotify 有一个广受关注的 Global Top 50 榜单，该榜单根据流媒体数据算法性地包含前一天的 前 50 首歌曲。Spotify 还为每个国家维护相应的 Top 50 榜单，这些榜单基于前一天的国家特定流媒体数据。由于这些榜单的纳入标准是透明的，人们可以比较刚刚上榜的歌曲的流媒体数据，以识别纳入对 Top 50 榜单的影响。

## 2.2 Challenges in Getting on Lists
**进入榜单面临的挑战**

Music from diverse sources such as independent recording labels has little difficulty getting included in the catalogs of streaming services carrying tens of millions of songs. But getting noticed by a wide audience is harder, and getting a song onto a major playlist may be subject to the same pressures traditionally surrounding radio airplay. As the Guardian puts it, "Getting songs on to popular playlists is increasingly important to labels, but there may be potential for shenanigans."[^13] According to Vulture, "The most influential playlist in music is Spotify's RapCaviar, which turns mixtape rappers into megastars. And it's all curated by one man."[^14] The curator, Tuma Basa, was born in Zaire and raised in Iowa. A 2017 Billboard article described its curator, Tuma Basa as "one popular dude."[^15]

> 来自独立唱片公司等多元渠道的音乐作品，被纳入收录数千万首歌曲的流媒体服务曲库并非难事。然而，要获得广泛听众的关注则更为困难，而让歌曲登上主流播放列表，可能与传统电台播放所面临的压力如出一辙。正如《卫报》所言：“让歌曲进入热门播放列表对唱片公司日益重要，但其中可能存在暗箱操作的空间。”[^13] 据《Vulture》杂志报道：“音乐领域最具影响力的播放列表是 Spotify 的‘RapCaviar’，它能让混音带说唱歌手蜕变为超级巨星。而这一切均由一人策划。”[^14] 该列表的策展人 Tuma Basa 出生于扎伊尔，在爱荷华州长大。2017 年《Billboard》杂志的一篇文章将其策展人 Tuma Basa 描述为“一位备受瞩目的人物”。[^15]

Radio regulation in the U.S. has traditionally frowned upon content owners' influence on programming choices. When labels' payments to disc jockeys came to light in the late 1950s, Congressional hearings ensued, Alan Freed's career was ruined, and Dick Clark's was tarnished.[^16] Decisions about which songs to promote are instead viewed like editorial content decisions at journalistic outlets, with an expectation that these decisions be unbiased. Critics of payola argue that listeners "want to know that the music they hear on the radio is chosen because of its artistic merit or popularity."[^17] Under U.S. law, "When a broadcast licensee has received or been promised payment for airing program material, then the station must disclose that fact at the time material is aired and identify who is paying for it."[^18] These laws do not apply to streaming services, although Spotify has pledged not to take payola.[^19] Pandora has negotiated an agreement with Merlin to pay lower royalties in exchange for more frequent streams, which some observers have likened to payola (Peoples, 2016).

> U.S. 的广播监管传统上不赞成内容所有者对节目选择的影响。当唱片公司向唱片骑师支付款项在 1950 年代末曝光时，Congressional 听证会随之而来，Alan Freed 的事业被毁，Dick Clark 的事业也受损。[^16] 关于推广哪些歌曲的决定反而被视为像新闻机构的编辑内容决策，期望这些决定是公正的。付费播放的批评者认为，听众“想知道他们在广播中听到的音乐是因为其艺术价值或流行度而被选中的。”[^17] 根据 U.S. 法律，“当广播被许可方收到或承诺支付播放节目材料的费用时，电台必须在材料播放时披露这一事实并指明支付者。”[^18] 这些法律不适用于流媒体服务，尽管 Spotify 承诺不接受付费播放。[^19] Pandora 已与 Merlin 谈判达成协议，支付较低版税以换取更频繁的流媒体播放，一些观察家将其比作付费播放 (Peoples, 2016)。

Spotify operates in multiple countries and is not constrained by national borders. While many countries, including Canada, France, and Australia, have traditionally mandated domestic content shares on radio, no such regulations exist for Spotify (see Richardson and Wilkie, 2015). To the extent that playlists are influential in determining which countries' repertoires are consumed, playlist decisions will be of some interest to those concerned about cultural trade.

> Spotify 在多个国家运营，且不受国界限制。尽管许多国家，包括 Canada、France 和 Australia，传统上在广播中强制规定国内内容份额，但 Spotify 并无此类规定（参见 Richardson and Wilkie，2015）。在播放列表对决定消费哪些国家的曲目具有影响力的程度上，播放列表的决策将引起那些关注文化贸易的人的兴趣。

## 2.3 Playlist Concentration
**播放列表集中度**

Thousands of playlists are available to users at Spotify. While we will discuss data in detail below, we note here that we have obtained the names, owners, and number of playlists followers for the top 1,000 lists at Spotontrack.com, a website that tracks Spotify playlists. The top list is Today's Top Hits, a curated list maintained by Spotify with 18.5 million followers as of December 2017. The next-most followed list is the algorithmic Global Top 50, with 11.5 million followers. Next are RapCaviar with 8.6 million, Viva Latino with 6.9 million, and Baila Reggaeton with 6.3 million. A few things are noteworthy. First, all of the 25 most-followed playlists are maintained by Spotify, and all but one of them (Global Top 50) are curated and therefore discretionary rather than algorithmic. Second, the number of followers drops off fairly quickly, particularly after the top 25: The $2 0 0 ^ { t h }$ list has 166,000 followers. The $5 0 0 ^ { t h }$ has 43,000, and the $1 0 0 0 ^ { t h }$ has under 11,000, fewer than one percent of the top list's followers.

> Spotify 为用户提供了数千个播放列表。虽然我们将在下文详细讨论数据，但我们在此指出，我们已经从 Spotontrack.com 获取了前 1,000 个列表的名称、所有者和播放列表关注者数量，该网站跟踪 Spotify 播放列表。排名第一的列表是 Today's Top Hits，这是一个由 Spotify 维护的精选列表，截至 2017 年 12 月拥有 1850 万关注者。其次是算法生成的 Global Top 50，拥有 1150 万关注者。接下来是 RapCaviar 拥有 860 万，Viva Latino 拥有 690 万，以及 Baila Reggaeton 拥有 630 万。有几点值得注意。首先，所有 25 个最受关注的播放列表都由 Spotify 维护，除其中一个（Global Top 50）外，其余都是精选的，因此是自由裁量的而非算法生成的。其次，关注者数量下降得相当快，特别是在前 25 名之后：第 200 个列表有 166,000 名关注者。第 500 个列表有 43,000 名，第 1000 个列表有不到 11,000 名，不到排名第一列表关注者的百分之一。

By list owner, the concentration is large. Spotify's curated lists have over three quarters of the followers of the top 1,000 playlists; Spotify's algorithmic lists have another 9.3 percent. The lists operated by the major record labels, Filtr, Digster, and Topsify, have 3.1, 2.7, and 0.9 percent of the top 1000's cumulative followers. The remaining list owners have negligible shares. It is clear that Spotify dominates playlists at Spotify. If playlists influence listening choices, then Spotify's curated lists are well-positioned to wield influence.

> 按列表所有者划分，集中度很高。Spotify 的精选列表拥有超过四分之三的顶级 1,000 播放列表的粉丝；Spotify 的算法列表另有 9.3%。由主要唱片公司运营的列表，Filtr、Digster 和 Topsify，拥有顶级 1000 累计粉丝的 3.1%、2.7% 和 0.9%。其余列表所有者的份额可以忽略不计。很明显，Spotify 在 Spotify 上主导播放列表。如果播放列表影响收听选择，那么 Spotify 的精选列表处于有利位置以施加影响。

## 2.4 Relationship to Existing Literature
**与现有文献的关系**

Our questions - how do playlists affect song success and artist discovery, as well as whether platform operators have preferences and biases - have antecedents in a number of existing literatures. There is a large theoretical literature on platforms (see Rysman, 2009 for a summary) and a growing body of theoretical work on platform incentives to bias (Hagiu and Jullien, 2011; Corniere and Taylor, 2014), but empirical work on the question of whether platforms are biased in their treatment of suppliers is less common. Some examples include Edelman (2011) on whether Google biases its search results in favor of its own properties and Zhu and Liu (2016) on whether Amazon enters the markets for products established by its marketplace vendors.

> 我们的问题——播放列表如何影响歌曲成功和艺术家发现，以及平台运营商是否有偏好和偏见——在现有文献中有先例。关于平台有大量的理论文献（参见 “Rysman, 2009” 的综述），以及关于平台偏袒激励的理论研究日益增多（“Hagiu and Jullien, 2011; Corniere and Taylor, 2014”），但关于平台在处理供应商时是否存在偏见的实证研究较少见。一些例子包括 “Edelman (2011)” 关于 Google 是否偏袒其自身属性的搜索结果，以及 “Zhu and Liu (2016)” 关于 Amazon 是否进入其市场供应商建立的产品市场。

While we are aware of no existing work on playlists per se, the questions raised here resemble the question in a number of existing literatures. There is some work on music discovery at Spotify (Datta et al., 2017) and Deezer (Aguiar, 2017). Moreover, curated playlists contain critics' assessments, so studying the impact of playlists on subsequent streams resembles work like Reinstein and Snyder (2005) on the impact of critical assessments on movie box office revenue. Playlists are in some ways like radio stations, and playlist inclusion resembles a radio station's decision to air a song, so the study of playlist impacts on streaming resembles the question addressed in studies of the impact of airplay on recorded music sales (Liebowitz, 2004; Dertouzos, 2008; McBride, 2014). Algorithmic playlists are literally most-streamed lists, so measuring their impact on streams is very related to existing work on the impact of best-seller lists on sales and product variety (Sorensen, 2007). Salganik et al. (2006) find evidence that signals of popularity such as best-seller lists lead to a "self-fulfilling prophecy."

> 尽管我们意识到没有关于播放列表本身的研究，但这里提出的问题类似于许多现有文献中的问题。有一些关于 Spotify (Datta et al., 2017) 和 Deezer (Aguiar, 2017) 上音乐发现的研究。此外，策划的播放列表包含批评家的评估，因此研究播放列表对后续流媒体的影响类似于 Reinstein and Snyder (2005) 关于批评评估对电影票房收入影响的工作。播放列表在某些方面类似于广播电台，播放列表的包含类似于广播电台播放歌曲的决定，因此研究播放列表对流媒体的影响类似于研究中广播播放对录制音乐销售影响的问题 (Liebowitz, 2004; Dertouzos, 2008; McBride, 2014)。算法播放列表字面上是最多流媒体播放的列表，因此测量它们对流媒体的影响与现有关于畅销列表对销售和产品多样性影响的研究非常相关 (Sorensen, 2007)。Salganik et al. (2006) 发现证据表明，流行信号如畅销列表会导致一种“自我实现的预言”。

Playlists resemble advertising, and some of the empirical challenges in measuring their impact recalls the challenges described in the new literature on advertising effectiveness (see, e.g. Lewis et al., 2015). The question of whether playlists at a streaming service partially owned by some of the underlying rights holders would favor certain kinds of repertoires in its playlists echoes some questions pursued in the literature on media bias (Reuter and Zitzewitz, 2006; DellaVigna and Hermle, 2017).

> 播放列表与广告具有相似性，其在影响力测量方面所面临的部分实证挑战，令人联想到新兴广告效果研究文献中所述的难题（参见，例如 Lewis 等人，2015）。关于部分由底层版权方共同持股的流媒体服务平台，是否会在其播放列表中偏袒特定类型曲库的问题，呼应了媒体偏见研究领域探讨的一些议题（Reuter 与 Zitzewitz，2006；DellaVigna 与 Hermle，2017）。

## Notes

[^11]: See Bertoni (2013).

[^12]: See [https://www.wired.com/2017/05/secret-hit-making-power-spotify-playlist/](https://www.wired.com/2017/05/secret-hit-making-power-spotify-playlist/).

[^13]: See [https://www.theguardian.com/technology/2015/apr/10/things-we-learned-indie-labels](https://www.theguardian.com/technology/2015/apr/10/things-we-learned-indie-labels) -digital.

[^14]: See [http://www.vulture.com/2017/09/spotify-rapcaviar-most-influential-playlist-in-mus](http://www.vulture.com/2017/09/spotify-rapcaviar-most-influential-playlist-in-mus) ic.html.

[^15]: See [https://www.billboard.com/articles/business/7865934/spotify-tuma-basa-curating-ra](https://www.billboard.com/articles/business/7865934/spotify-tuma-basa-curating-ra) pcaviar-pitching-playlists.

[^16]: See Nayman (2012).

[^17]: See [http://futureofmusic.org/blog/2015/05/13/music-community-unites-against-radio-pay](http://futureofmusic.org/blog/2015/05/13/music-community-unites-against-radio-pay) ola.

[^18]: See [https://www.fcc.gov/consumers/guides/fccs-payola-rules](https://www.fcc.gov/consumers/guides/fccs-payola-rules).

[^19]: Spotify claims to be "absolutely against any kind of 'pay to playlist', or sale of playlists . . . It's bad for artists and it's bad for fans." See Cookson (2015).

# 3 DATA
**数据**

The underlying data for this study come from three separate sources and consist of two distinct datasets. The first dataset includes streaming data at Spotify. In particular, we observe the daily top 200 songs on Spotify, by country, for 26 countries, during 2016 and 2017.[^20] The 2017 country-specific streaming data are available directly from Spotify, which provides daily streaming totals for each of the top 200 songs by country, back to the start of 2017.[^21] The 2016 streaming data are from Spotontrack.com, which tracks streams, playlists, and followers on Spotify.[^22] The 2017 country-level streaming data contain 1,847,615 daily song observations and a total of 48,731 song-countries and 19,055 distinct tracks.[^23] In addition to country-specific top 200 daily streams, we also have the daily global top 200 streams, which cover all countries where Spotify operates and include 1,764 distinct songs during 2017. Table 1 reports the total number of streams, by country, in the 2017 countrylevel data.

> 这项研究的基础数据来自三个独立的来源，并包含两个不同的数据集。第一个数据集包括 Spotify 的流媒体数据。特别是，我们观察了 Spotify 上的每日 top 200 歌曲，按国家，针对 26 个国家，在 2016 年和 2017 年。[^20] 2017 年国家特定的流媒体数据可直接从 Spotify 获取，该平台提供每个国家 top 200 歌曲的每日流媒体总数，回溯到 2017 年初。[^21] 2016 年的流媒体数据来自 Spotontrack.com，该网站追踪 Spotify 上的流媒体、播放列表和关注者。[^22] 2017 年国家层面的流媒体数据包含 1,847,615 个每日歌曲观察值，总计 48,731 个歌曲-国家和 19,055 个独特曲目。[^23] 除了国家特定的每日 top 200 流媒体，我们还有每日全球 top 200 流媒体，这些覆盖了 Spotify 运营的所有国家，并在 2017 年包括 1,764 首独特歌曲。表 1 报告了 2017 年国家层面数据中按国家划分的流媒体总数。

![[Pasted image 20260315013244.png]]

Our second dataset also comes from Spotontrack.com and corresponds to the songs that appear on various playlists, including their ranks and the dates the songs enter and leave the lists. We focus on the five most-followed Spotify-owned global playlists, as well as three country-specific Spotify-owned playlists. The global lists are the four global curated lists (Today's Top Hits, RapCaviar, Viva Latino, and Baila Reggaeton) and the algorithmic Global Top 50. The country-specific list is New Music Friday, which is available separately for each country. The New Music Friday playlists for 2017 include 52,851 distinct song-countries and 20,621 distinct songs (because many songs appear on multiple countries' recommendation lists). While we have New Music Friday playlists for all of 2017, our data on the global curated playlists begins at different dates during 2017, with the latest in May, 2017. Table 2 summarizes the information, with both the number of followers for the lists, as well as the dates we start observing the lists.

> 我们的第二个数据集也来自 Spotontrack.com，对应于出现在各种播放列表中的歌曲，包括它们的排名和歌曲进入和离开列表的日期。我们关注五个最受关注的 Spotify-owned 全球播放列表，以及三个特定国家的 Spotify-owned 播放列表。全球列表是四个全球策划列表（ Today's Top Hits, RapCaviar, Viva Latino, 和 Baila Reggaeton ）以及算法生成的 Global Top 50。特定国家的列表是 New Music Friday，它在每个国家单独可用。2017 年的 New Music Friday 播放列表包括 52,851 个不同的歌曲-国家和 20,621 首不同的歌曲（因为许多歌曲出现在多个国家的推荐列表中）。虽然我们有 2017 年全年的 New Music Friday 播放列表，但我们对全球策划播放列表的数据始于 2017 年的不同日期，最晚在 2017 年 5 月。Table 2 总结了这些信息，包括列表的关注者数量，以及我们开始观察列表的日期。


![[Pasted image 20260315013312.png]]

We also obtain song and artist characteristics for each song streaming in the country-level and global streaming sample in 2017, as well as for each song on the playlists we study. In particular, we observe the record label and the International Standard Recording Code (ISRC) for each song.[^24]

> 我们还在 2017 年的国家级和全球流媒体样本中，以及我们研究的播放列表中的每首歌曲，获取了歌曲和艺术家的特征。特别是，我们观察了每首歌曲的唱片公司和 International Standard Recording Code (ISRC)。[^24]

The label identity allows us to create of measure of whether songs are released by major or independent record labels. There is a total of 6,577 distinct labels in our combined datasets, and no clear way of classifying them into major and independent. Using their names, however, we are able to identify some of the obvious major labels.[^25] While this method guarantees that all the labels that we classify in the major category are indeed majors, some of the non-obvious majors may end up being identified as independent labels. Since the main goal of this classification is to make comparisons, for instance, between the major composition of different playlists, our measure nevertheless remains informative.

> 标签身份使我们能够创建衡量标准，以判断歌曲是否由主要或独立唱片公司发行。在我们的合并数据集中，总共有 6,577 个不同的标签，但没有明确的方法将它们分类为主要或独立。然而，通过使用它们的名称，我们能够识别一些明显的主要标签。[^25] 虽然这种方法保证我们将所有分类为主要类别的标签确实是主要公司，但一些不明显的主要公司可能最终被识别为独立标签。由于这种分类的主要目的是进行比较，例如，不同播放列表的主要构成之间的比较，因此我们的衡量标准仍然具有信息性。

The ISRC code provides us with measures of the national origin of each song, as well as its release vintage. We are also interested in separately studying the new artists on the New Music Friday lists. To determine which artists are new among those whose songs are in the 2017 country-level streaming data, we start with artists whose songs are on the 2017 New Music Friday playlists, then remove the artists with songs observed streaming during the previous year 2016. For each of the remaining artists, we obtain recording release histories from Musicbrainz, an open music encyclopedia that collects music metadata and makes it available to the public.[^26] Using these histories, we discard artists whose first release predates 2017. This leaves us with a set of 670 new artists whose songs appear on the New Music Friday playlists during 2017.

> ISRC 代码为我们提供了每首歌的国家来源衡量标准，以及其发行年份。我们还对单独研究 New Music Friday 列表上的新艺术家感兴趣。为了确定在 2017 年国家级流媒体数据中哪些艺术家是新的，我们从歌曲在 2017 年 New Music Friday 播放列表上的艺术家开始，然后移除在之前一年 2016 年观察到有歌曲流媒体的艺术家。对于剩余的每位艺术家，我们从 Musicbrainz 获取录音发行历史，Musicbrainz 是一个开放的音乐百科全书，收集音乐元数据并向公众提供。[^26] 使用这些历史记录，我们丢弃首次发行早于 2017 年的艺术家。这使我们得到一组 670 位新艺术家，他们的歌曲在 2017 年出现在 New Music Friday 播放列表上。

We use these underlying datasets to create our main analysis samples, which consist of the songs from a playlist, merged with the streaming data. With this sort of dataset we can do two broad things. For songs already appearing on the streaming charts when they appear on a playlist - from the global curated playlists - we can construct time series on their streaming, before and after their chart appearance. We also observe when the songs leave the chart, so we can also examine the evolution of their daily streaming before and after they leave the chart.

> 我们利用这些基础数据集构建了主要分析样本，该样本由播放列表中的歌曲与流媒体数据合并而成。基于此类数据集，我们可开展两大维度的分析：对于已在流媒体榜单上的歌曲（源自全球精选播放列表），当其出现在榜单时，我们能够构建其上榜前后流媒体表现的时间序列数据。同时，我们亦能捕捉歌曲下榜的时间节点，从而探究其下榜前后每日流媒体量的演变趋势。

The second broad dataset, for the New Music Friday playlists, resembles the first, except that we lack any pre-listing streaming data. We link dates and ranks for appearances on a country's New Music Friday lists with subsequent daily appearances on the country's daily top 200 streaming chart. Because songs remain on the New Music Friday lists for 7 days, there is no variation in the timing of removal.

> 第二个广泛的数据集，针对 New Music Friday 播放列表，类似于第一个，除了我们缺乏任何上市前的流媒体数据。我们将一个国家 New Music Friday 列表上的出现日期和排名与该国每日前 200 流媒体榜上的后续每日出现联系起来。因为歌曲在 New Music Friday 列表上保留 7 天，所以移除时间没有变化。

We use a different approach for the analysis of the impact of inclusion in the Global Top 50 algorithmic playlist. Because we observe the top 200 streaming songs in each day of our sample - and because the Global Top 50 playlist is based on the song’s past streaming ranking - we can replicate the Global Top 50 playlist and additionally observe the level of streams for songs that are ranked $5 1 ^ { s t }$ and lower. We can therefore pay particular attention to a possible discontinuity in streams around the $5 1 ^ { s t }$ ranked song. In empirically exploring the determinants of the Global Top 50, we noticed that playlist matched the previous day’s streaming ranking for 133 days during 2017 and matched the streaming ranking of two days earlier for 218 days. We use only these 351 of 365 days in our estimation, where we know not only the Global Top 50 but also which songs would have been listed next had the Global Top 50 list been longer.

> 我们采用一种不同的方法来分析被纳入 Global Top 50 算法播放列表的影响。因为我们观察样本中每天的前 200 首流媒体歌曲——并且因为 Global Top 50 播放列表基于歌曲过去的流媒体排名——我们可以复制 Global Top 50 播放列表，并额外观察排名第 51 名及更低的歌曲的流媒体水平。因此，我们可以特别关注围绕第 51 名排名歌曲的流媒体可能的不连续性。在实证探索 Global Top 50 的决定因素时，我们注意到该播放列表在 2017 年有 133 天匹配前一天的流媒体排名，并有 218 天匹配两天前的流媒体排名。在我们的估计中，我们仅使用这 351 天中的 365 天，其中我们不仅知道 Global Top 50，还知道如果 Global Top 50 列表更长，哪些歌曲会被列出。

For calculating the effect of playlist inclusion on streaming, we will ultimately be interested in the time that songs spend on the playlists. Measuring this is complicated by two facts. First, songs can enter and leave the playlists more than once. This is rare, except for the Global Top 50, where songs can enter and leave the playlist according to the vagaries of the streaming charts. Songs on this list have an average of 1.38 spells. Table 2 describes the duration of the song spells on various Spotify lists in our data. For example, the mean spell on Today's Top Hits is 54.2 days, and the average number of spells per song is 1.004. The mean spell on RapCaviar is 39 days (with an average of 1.07 spells per song), and the mean spell for Viva Latino is 111 days (with 1.03 spells per song). A second complication arises from the fact that some songs are already on the list when our playlist data begin, and some are still on the lists as our data end, so our duration measures are censored. We can use censored regression to estimate the underlying mean spell length. Table 2 reports these, and as expected they are longer than the raw averages. Finally, we multiply the underlying mean spell lengths by the number of spells per song.

> 为了计算播放列表包含对流媒体的影响，我们最终会对歌曲在播放列表上花费的时间感兴趣。测量这一点因两个事实而变得复杂。首先，歌曲可以多次进入和离开播放列表。这很罕见，除了 Global Top 50 ，其中歌曲可以根据流媒体排行榜的波动进入和离开播放列表。此列表上的歌曲平均有 1.38 次播放期。表 2 描述了我们的数据中各种 Spotify 列表上歌曲播放期的持续时间。例如，Today's Top Hits 上的平均播放期为 54.2 天，每首歌曲的平均播放期次数为 1.004 。RapCaviar 上的平均播放期为 39 天（每首歌曲平均 1.07 次播放期），而 Viva Latino 的平均播放期为 111 天（每首歌曲 1.03 次播放期）。第二个复杂因素源于这样一个事实：当我们的播放列表数据开始时，一些歌曲已经在列表上；当我们的数据结束时，一些歌曲仍然在列表上，因此我们的持续时间测量是截尾的。我们可以使用截尾回归来估计潜在的平均播放期长度。表 2 报告了这些，正如预期，它们比原始平均值更长。最后，我们将潜在的平均播放期长度乘以每首歌曲的播放期次数。

## Notes

[^20]: We include these 26 countries because we can obtain the New Music Friday lists for these countries. See below.

[^21]: See [https://spotifycharts.com/regional](https://spotifycharts.com/regional).

[^22]: See Seehttp://[www.spotontrack.com](http://www.spotontrack.com/).

[^23]: Countries included in the sample are Brazil, Canada, Switzerland, Colombia, Germany, Denmark, Spain, Finland, France, Great Britain, Hong Kong, Indonesia, Iceland, Italy, Malaysia, Mexico, Netherlands, Norway, Philippines, Portugal, Sweden, Singapore, Turkey, Taiwan, and the United States.

[^24]: The ISRC is the internationally recognized identification tool for sound and music video recordings. See [https://www.usisrc.org/](https://www.usisrc.org/).

[^25]: We classify as major any record label containing the following names: Asylum, Atlantic, Capitol, Epic, Interscope, Warner, Motown, Virgin, Parlophone, Republic, Big Machine, Sony, Polydor, Big Beat, Def Jam, MCA, Universal, Astralwerks, WM, Trinidad & Tobago, RCA, Columbia.

[^26]: See [https://musicbrainz.org/](https://musicbrainz.org/).


# 4 EFFECT OF LIST INCLUSION ON STREAMS
**入选榜单对流量的影响**

This section examines the effects of the Spotify's largest global curated playlists, which tend to include already-established songs and artists, on the volumes of streaming experienced by included songs. We turn in Section 5 to effects of the New Music Friday playlists on the performance of new songs, or product discovery.

> 本节探讨了 Spotify 最大的全球歌单对歌曲的流媒体播放量的影响，这些播放列表往往包括已经成名的歌曲和艺术家。在 Section 5 中，我们将转向 New Music Friday 播放列表对新歌曲表现或产品发现的影响。

## 4.1 Effect of Inclusion on Global Playlists
**在全球榜单上入选的影响**

Before turning to regression approaches, a simple look at some data is instructive. Figure 1 shows the evolution of playlist followers and U.S. daily streams for a song added to Today's Top Hits during 2017. The song "What Ifs" by Kane Brown was added to the Today's Top Hits playlist on October 5, 2017. On or about that date, the number of playlist followers for the song jumped from 11.6 to 29.2 million. The number of playlist followers then fluctuated about 30 million for about a month. On November 2, the song was removed from Today's Top Hits, and its number of followers fell from 30.8 million to just 10.8 million. In subsequent months the number of followers continued to generally decline, sometimes rapidly as particular playlists removed the song.

> 在转向回归分析方法之前，初步审视数据颇具启发性。图 1 展示了 2017 年间一首被加入 Today's Top Hits 的歌单追随者数量与美国每日流媒体播放量的演变趋势。Kane Brown 的歌曲《What Ifs》于 2017 年 10 月 5 日被添加到 Today's Top Hits 播放列表中。大约在该日期前后，该歌曲的歌单追随者数量从 1160 万跃升至 2920 万。随后约一个月内，歌单追随者数量在 3000 万左右波动。11 月 2 日，该歌曲从 Today's Top Hits 中移除，其追随者数量从 3080 万骤降至仅 1080 万。在接下来的几个月中，追随者数量总体呈下降趋势，有时因特定播放列表移除该歌曲而迅速减少。

![[Pasted image 20260315012751.png]]
`Figure 1: Daily Followers and US Streams for a Song added to Today's Top Hits.`

The large and discontinuous jumps in followers for the Kane Brown song above, which was added then removed from the most followed playlist on Spotify, suggest a method for measuring the impact of playlist inclusion on streams for the global playlists. We can look at the streams in countries where the song was already observable among the streaming songs (among the top 200 daily songs for the country) prior to the song's inclusion on the list. We can then examine whether the streams change with the discontinuous change in followers.

> 上述 Kane Brown 歌曲的粉丝数量出现大幅且不连续的跳跃，该歌曲曾被添加到 Spotify 上最受关注的播放列表中，随后又被移除，这提出了一种测量播放列表收录对全球播放列表流媒体量影响的方法。我们可以查看在歌曲被列入播放列表之前，已经在流媒体歌曲中（在该国每日 top 200 歌曲中）可观察到的国家的流媒体量。然后，我们可以检查流媒体量是否随着粉丝数量的不连续变化而变化。

The idea here borrows from the regression discontinuity approach (Lee and Lemieux, 2010). Our assumption here is that a song's underlying popularity evolves smoothly after release as people hear of the song, and some little-followed playlists add the song. But when a list with many followers adds the song, the song is "treated," and the number of users exposed to the song via playlists jumps discontinuously. Figure 1, which overlays U.S. daily streams against the number of the song's daily followers, provides much of the answer for this song. In June 2017, the song has nearly 200,000 daily streams, and the number rises steadily (around day of the week fluctuations) to October. On October 5, when the number of followers jumps from about 12 to nearly 30 million, the number of daily streams rises by roughly 100,000. Later, on November 2, when the number of followers falls by almost 20 million, the number of daily streams falls by about 100,000.

> 此处的思路借鉴了回归断点方法（Lee and Lemieux，2010）。我们的基本假设是：歌曲发布后，随着听众知晓度的提升及少量关注者播放列表的收录，其内在流行度会平稳演进。但当拥有大量关注者的播放列表收录该歌曲时，歌曲便受到“处理”，通过播放列表接触该歌曲的用户数量将发生断点式跃升。图 1 将美国地区每日流媒体数据与该歌曲每日新增关注者数量进行叠合展示，为此歌曲提供了关键解释。2017年6月，该歌曲每日流媒体量接近 200,000 次，并保持稳定上升趋势（剔除周内波动影响）直至10月。10月5日，当关注者数量从约 1,200 万跃升至近 3,000 万时，每日流媒体量同步激增约 100,000 次。随后在11月2日，当关注者数量骤降近 2,000 万时，每日流媒体量亦相应下降约 100,000 次。

Approaching this systematically, we can pool song-countries and flexibly characterize streams around the event via the following model:

$$ s _ {i c t} = \gamma_ {\tau} + \mu_ {i c} + \pi_ {d} + \varepsilon_ {i c t} \tag {1} $$

Here, $s _ { i c t }$ is a measure of streaming for song $i$ in country $c$ on day $t$ , $\pi _ { d }$ is a day of the week effect, $\mu _ { i c }$ is a country-specific song fixed effect, and $\varepsilon _ { i c t }$ is an error term. Finally, $\tau$ refers to the days since the event (or until the event when $\tau < 0$ ). We can then plot the coefficients $\gamma _ { \tau }$ against $\tau$ .

> 系统性地处理这个问题，我们可以汇总歌曲-国家数据，并通过以下模型灵活地描述事件周围的流媒体情况：
> $$ s _ {i c t} = \gamma_ {\tau} + \mu_ {i c} + \pi_ {d} + \varepsilon_ {i c t} \tag {1} $$
> 这里， $s _ { i c t }$ 是歌曲 $i$ 在国家 $c$ 第  t  天的流媒体度量，$\pi _ { d }$ 是星期几效应，$\mu _ { i c }$ 是国家特定歌曲固定效应， $\varepsilon _ { i c t }$ 是误差项。最后，$\tau$ 指的是事件发生后的天数（或事件前的天数，当 $\tau < 0$ 时）。然后，我们可以绘制系数 $\gamma _ { \tau }$ 相对于 $\tau$ 的图。

Before turning to estimates, we need to clarify the designation of the event day. We observe the date that a song enters a playlist, but we do not know what time the song entered. This creates some challenges in defining the last untreated and first treated days, i.e. the last full day in which the song is not on the playlist and the first day in which the song is on the playlist all day. Our data are updated every 24 hours, so the appearance of a song on a playlist on a particular day means that the song may have entered the list any time during the previous 24 hours. This in turn leaves two possibilities. One is that the song entered today, so that the apparent entry day is actually partially treated, while the day before its appearance was fully untreated. The second possibility is that the song entered the list the previous day. In that case, the entry day would be fully treated, while the previous day would be partially treated. We cannot distinguish these two cases. We can be confident, however, that two days before the entry day is fully untreated, while the day after the entry day is fully treated. Hence, our shortest window for effect estimation compares two days prior to the entry day to one day after. In our estimation below we set $\gamma _ { \tau } = 0$ on the last definitely fully untreated day and $\tau = 3$ for the first definitely fully treated day. We define the drop window analogously.

> 在转向估计之前，我们需要澄清事件日的指定。我们观察到歌曲进入播放列表的日期，但我们不知道歌曲进入的具体时间。这给定义最后未处理日和首次处理日带来了一些挑战，即歌曲不在播放列表上的最后一个完整日，以及歌曲全天在播放列表上的第一天。我们的数据每 24 小时更新一次，因此歌曲在特定日期出现在播放列表上意味着歌曲可能在前 24 小时内的任何时间进入列表。这反过来留下了两种可能性。一种是歌曲今天进入，因此明显的进入日实际上是部分处理的，而出现前一天是完全未处理的。第二种可能性是歌曲在前一天进入列表。在这种情况下，进入日将是完全处理的，而前一天将是部分处理的。我们无法区分这两种情况。然而，我们可以确信，进入日的前两天是完全未处理的，而进入日的后一天是完全处理的。因此，我们用于效应估计的最短窗口比较进入日的前两天和后一天。在下面的估计中，我们在最后一个确定完全未处理日设置 $\gamma _ { \tau } = 0$ ，在第一个确定完全处理日设置 $\tau = 3$ 。我们类似地定义下降窗口。

The left panel of Figure 2 reports the results of this estimation for the event of addition to Today's Top Hits. A few things are clear. First, there is a pre-event trend: streams are rising when songs are added to the playlist, although streams fall on the last pre-treatment day. Second, while there is no apparent effect on the first potentially partially treated day (the day prior to the song’s appearance on the list, with $\tau = 1$ ), streaming rises somewhat on the (potentially partially treated) entry day ( $\tau = 2$ ) and substantially by the first fully treated day ( $\tau = 3$ ). Streams continue to rise for two more days, then begin rising at a steady rate. The right panel of Figure 2 reports the analogous model for the removal events from Today's Top Hits.

> 图 2 的左面板报告了对于添加到 Today's Top Hits 事件的结果估计。有几件事情是清楚的。首先，存在一个事前趋势：当歌曲被添加到播放列表时，流媒体播放量在上升，尽管在最后一个预处理日流媒体播放量下降。其次，虽然在第一个可能部分处理日（歌曲出现在列表前一天，$\tau = 1$ ）没有明显效果，但在（可能部分处理的）进入日（ $\tau = 2$  ）流媒体播放量有所上升，并在第一个完全处理日（ $\tau = 3$ ）大幅上升。流媒体播放量继续上升两天，然后开始以稳定速率上升。图 2 的右面板报告了对于从 Today's Top Hits 移除事件的类似模型。


![[Pasted image 20260315012852.png]]
`Figure 2: Normalized streams before and after add and removal events at Today's Top Hits.`
`表2：Today's Top Hits 歌单在添加和移除事件发生前后的归一化流量。`

We estimate the effect as the coefficient on the first fully treated day relative to the level of the last fully untreated day. (This may be conservative, as streams seem to be rising relative to trend for a few days after the add event). We use data from countries that differ substantially in size and therefore streaming volumes. To make the data comparable across countries, we normalize streams by the countries' annual total streams in our data. We then multiply these figures by a million to put them in convenient units. We refer to this measure as "normalized streams."

> 我们通过相对于最后一个完全未处理日的水平，在第一个完全处理日的系数来估计效应。（这可能较为保守，因为流量似乎在添加事件后的几天内相对于趋势有所上升）。我们使用了在规模和流量体积上差异显著的不同国家的数据。为了使各国数据具有可比性，我们通过各国在我们数据中的年度总流量对流量进行了归一化处理。随后，我们将这些数值乘以一百万，以便使用更便捷的单位进行表示。我们将这一度量称为“归一化流量”。

Table 3 reports effects of additions and removals from the four curated global playlists. We estimate that appearing on Today's Top Hits daily raises streams by 3.346 normalized streams (standard error=0.28). We estimate that removal from Today's Top Hits reduces normalized streams by 2.757 (0.09). What is the size of the benefit of being included among Today's Top Hits? Songs remain on Today's Top Hits for an average of 74.4 days (see Table 2). If we assume that the effect evolves linearly, then the average daily effect is 3.052, the average of the add and removal effects ( ${ = \ \frac { 3 . 3 4 6 + 2 . 7 5 7 } { 2 }}$ ). Today's Top Hits is a global list, so to calculate its effect on streams we multiply the average daily effect estimate by the average spell length of its songs, by the average spell per song entering the playlist, and by the global number of streams in millions. This is (3.052 streams per million) × (74.4 days) × (1.004 spells) × (85,047 million streams).[^27] This yields 19.4 million additional streams, which - given Spotify's ostensible payments of $6 to $8.4 per thousand streams - translates to between $116,397 and $162,956 in payments from Spotify alone. See Table 4, which also presents estimates for the other global lists. The low end of these estimates vary between $60,265 for RapCaviar and $303,047 for Viva Latino. The high end of the estimates varies between $84,372 at RapCaviar and $424,265 at Viva Latino. We defer further discussion of magnitudes until we discuss the effect of appearing on the Global Top 50 playlist.

> 表 3 报告了四个精选全球播放列表的添加和移除效果。我们估计，每日出现在 Today's Top Hits 上会使标准化流媒体增加 3.346（标准误差=0.28）。我们估计，从 Today's Top Hits 移除会减少标准化流媒体 2.757（0.09）。被纳入 Today's Top Hits 的收益规模是多少？歌曲在 Today's Top Hits 上平均停留 74.4 天（参见表 2）。如果我们假设效果线性演变，那么平均每日效果为 3.052，即添加和移除效果的平均值（ ${ = \ \frac { 3 . 3 4 6 + 2 . 7 5 7 } { 2 }}$ ）。Today's Top Hits 是一个全球列表，因此为了计算其对流媒体的影响，我们将平均每日效果估计值乘以歌曲的平均持续时间、每首进入播放列表的歌曲的平均次数，以及全球流媒体数量（以百万计）。即（每百万 3.052 流媒体）×（74.4 天）×（1.004 次）×（85,047 百万流媒体）。[^27] 这产生了 1940 万额外流媒体，鉴于 Spotify 每千次流媒体支付 6 至 8.4 美元，仅 Spotify 的支付额就在 116,397 美元至 162,956 美元之间。参见表 4，该表还提供了其他全球列表的估计。这些估计的低端范围从 RapCaviar 的 60,265 美元到 Viva Latino 的 303,047 美元。估计的高端范围从 RapCaviar 的 84,372 美元到 Viva Latino 的 424,265 美元。我们推迟对规模的进一步讨论，直到讨论出现在 Global Top 50 播放列表上的效果。

![[Pasted image 20260315013342.png]]

![[Pasted image 20260315013354.png]]

## 4.2 Effect of the Global Top 50 Playlist
**全球前50榜单的影响**

If we knew the algorithm underlying algorithmic lists, then we could use a discontinuity approach to measure the impact of list inclusion on streams, comparing songs that just made the list to those that just missed inclusion. We do not know the list algorithms generally, with the important exception of the most-played lists, such as the Global Top 50, which shows the top 50 songs according to a previous day's streams. Because we observe the streams for the top 200 songs each day, we know which song would have been listed as the Global Top $5 1 ^ { s t }$ through $2 0 0 ^ { t h }$ if the Global Top 50 list were longer, or if it were a Global Top $N$ .[^28] This allows us to ask whether the dropoff in streams is larger for the previous day's $5 1 ^ { s t }$ song than for songs at nearby ranks. The effect of list inclusion will then show up as a discontinuity in the relationship between streaming and the previous day's ranks between the ranks of 50 and 51.

> 如果我们知道算法列表背后的算法，那么我们可以使用不连续性方法来衡量列表包含对流量的影响，比较刚刚上榜的歌曲和刚刚落榜的歌曲。我们通常不知道列表算法，但有一个重要的例外，即播放量最高的列表，例如 Global Top 50，它根据前一天的流量显示前 50 首歌曲。因为我们每天观察前 200 首歌曲的流量，我们知道如果 Global Top 50 列表更长，或者如果它是一个 Global Top N，那么哪首歌曲会被列为 Global Top 第 51 名到第 200 名。[^28] 这使我们能够询问前一天的 第 51 名 歌曲的流量下降是否比附近排名的歌曲更大。列表包含的影响将表现为流量与前一天排名之间关系在第 50 名和第 51 名之间的不连续性。

To implement this flexibly, we estimate the relationship between the change in log streams across sequential ranks and the rank, with the following model, estimated on the global data:

$$ \log \left(\frac {s _ {r t}}{s _ {r - 1 , t}}\right) = \theta_ {r} + \varepsilon_ {r t}, \tag {2} $$

where $s _ { r t }$ is global streams at rank $r$ on day $t$ , $\theta _ { r }$ is an estimated parameter, and $\varepsilon _ { r t }$ is an error term. This delivers a sequence of coefficients $\theta _ { r }$ showing the percent reduction in streams as we move from the $( r - 1 ) ^ { t h }$ ranked song to the $r ^ { t h }$ ranked song. If we plot these $\theta _ { r }$ coefficients in the neighborhood of $\theta _ { 5 1 }$ , is there a jump?

> 为了灵活实现这一点，我们估计了连续排名之间对数流量的变化与排名之间的关系，使用以下模型，基于全球数据进行估计：
> $$ \log \left(\frac {s _ {r t}}{s _ {r - 1 , t}}\right) = \theta_ {r} + \varepsilon_ {r t}, \tag {2} $$
> 其中 $s _ { r t }$ 是第 $t$ 天排名 $r$ 的全球流量，$\theta _ { r }$ 是一个估计参数，$\varepsilon _ { r t }$ 是误差项。这产生了一系列系数 $\theta _ { r }$，显示了从第 $( r - 1 ) ^ { t h }$ 名歌曲移动到第 $r ^ { t h }$ 名歌曲时流量的百分比减少。如果我们在 $\theta _ { 5 1 }$ 附近绘制这些 $\theta _ { r }$ 系数，是否存在跳跃？

Figure 3 reports the result of estimating equation (2) using the daily global top 200 Spotify streaming data. The decline in streams is roughly steady at just under 2 percent for ranks 40-50. The decline from 50 to 51 jumps to 6 percent, then returns to the roughly 2 percent for ranks 52-60, and the difference is large relative to the confidence interval. Thus, being on the list adds about 4 percent to streams, and a regression of $\begin{array} { r } { \log \left( \frac { s _ { r t } } { s _ { r - 1 , t } } \right) } \end{array}$ on rank and an indicator variable equal to one for the $5 1 ^ { s t }$ rank gives a coefficient of -.047 (standard error of .008).

> 图 3 报告了使用每日全球前 200 名 Spotify 流媒体数据估计方程(2)的结果。流媒体量的下降在排名 40-50 之间大致稳定在略低于 2% 的水平。从排名 50 到 51 的下降跃升至 6%，随后在排名 52-60 之间回归至大约 2%，且该差异相对于置信区间较大。因此，上榜使流媒体量增加约 4%，并且对排名和一个指示变量（在排名$5 1 ^ { s t }$时等于 1）进行$\begin{array} { r } { \log \left( \frac { s _ { r t } } { s _ { r - 1 , t } } \right) } \end{array}$的回归，得到的系数为 -.047（标准误差为 .008）。

![[Pasted image 20260315012932.png]]
`Figure 3`
`表3`

How big is the overall effect of being on the Global Top 50? The average global streams for a song at the $5 0 ^ { t h }$ position on the Global Top 50 (and therefore ranked $5 0 ^ { t h }$ the previous day) is 1,242,513. Multiplying this by 0.047 gives 59,000 streams per day. The average duration on the Global Top 50 chart (correcting for censoring and the number of spells per song) is 51.24 days. If the effect of being on the list were the same across ranks - and therefore the same for each day spent on the list - then we can calculate the overall effect of appearing on the Global Top 50 as $( 0 . 0 4 7 ) \times ( 1 , 2 4 2 , 5 1 3 ) \times ( 5 1 . 2 4 ) = 3 , 0 2 1 , 8 6 7$ streams. Songs on the Global Top 50 playlist have an average of 92.8 million global streams, suggesting that 3.3 percent of their streams arise from being on the Global Top 50 chart.

> 登上 Global Top 50 的整体影响有多大？一首在 Global Top 50 上位于第 $5 0 ^ { t h }$ 位的歌曲（因此前一天排名第 $5 0 ^ { t h }$）的平均全球流媒体量为 1,242,513。将其乘以 0.047 得到每天 59,000 次流媒体。在 Global Top 50 榜单上的平均持续时间（校正了审查和每首歌曲的播放次数）为 51.24 天。如果上榜的影响在各个排名中相同——因此在上榜的每一天都相同——那么我们可以计算出出现在 Global Top 50 上的整体影响为 $( 0 . 0 4 7 ) \times ( 1 , 2 4 2 , 5 1 3 ) \times ( 5 1 . 2 4 ) = 3 , 0 2 1 , 8 6 7$ 次流媒体。Global Top 50 播放列表中的歌曲平均有 92.8 百万次全球流媒体，这表明其中 3.3% 的流媒体来自登上 Global Top 50 榜单。

## 4.3 Magnitudes and Mechanical Effects
**量级与机械效应**

To gauge the size of the effect estimates, it is useful to compare them to the effects that would arise mechanically if streaming users spent all of their time using a playlist to which they had subscribed. Take Today's Top Hits, a playlist with 50 songs with 18.5 million followers during the sample period. If followers did all of their listening through the playlist and listened to all 50 songs per day, then entering the list would add 18.5 million daily streams to each song on the list. With a bit of detective work we can estimate that Spotify users listen to an average of roughly 7 songs per day. In 2016 Spotify reported paying $1.813 billion to rights holders.[^29] Spotify also reported paying between $6 and $8.4 per thousand streams. This suggests between 216 and 302 billion worldwide Spotify streams during 2016, or a midpoint of 259 billion streams. Spotify reported 100 million active users during 2016.[^30] Given 365 days in the year, this suggests that users listened to an average of 7.1 songs per day.

> 为了评估效应估计的规模，将其与如果流媒体用户将所有时间花在他们订阅的播放列表上所产生的机械效应进行比较是有用的。以 Today's Top Hits 为例，这是一个在样本期间拥有 1850 万追随者、包含 50 首歌曲的播放列表。如果追随者通过该播放列表进行所有收听，并且每天收听所有 50 首歌曲，那么进入该列表将为列表上的每首歌曲增加 1850 万的日流媒体量。通过一些调查工作，我们可以估计 Spotify 用户平均每天收听大约 7 首歌曲。2016 年，Spotify 报告向权利持有者支付了 18.13 亿美元。[^29] Spotify 还报告每千次流媒体支付 6 到 8.4 美元。这表明 2016 年全球 Spotify 流媒体量在 2160 亿到 3020 亿之间，中点为 2590 亿次流媒体。Spotify 报告 2016 年有 1 亿活跃用户。[^30] 考虑到一年有 365 天，这表明用户平均每天收听了 7.1 首歌曲。

Applying this average listening propensity, if Today's Top Hits users spent their listening time only with the list, then daily streams for listed songs would rise by about 2.6 million (${ = \ \frac { 1 8 . 5 } { ( \frac { 5 0 } { 7 } ) } }$) streams per day. Our econometric estimate of the daily streams effect of being added to Today's Top Hits is 259,531, which is 10 percent of the maximum mechanical effect (see Table 4). For the other global curated lists, the share varies between 15 and 22 percent.

> 应用这种平均收听倾向，如果 Today's Top Hits 用户只收听该列表，那么列表歌曲的每日流媒体播放量将增加约 260 万（${ = \ \frac { 1 8 . 5 } { ( \frac { 5 0 } { 7 } ) } }$）每天。我们对被添加到 Today's Top Hits 的每日流媒体播放量效应的计量经济学估计是 259,531，这是最大机械效应的 10%（见表 4）。对于其他全球策划列表，这一比例在 15% 到 22% 之间变化。

## 4.4 Effects Outside of Spotify
**Spotify 之外的影响**

We would like to know whether Spotify playlist inclusion has an impact outside of Spotify streaming. One measure of sales we can obtain is the daily U.S. iTunes top 100 ranking based on the volume of permanent downloads. We obtain these rankings for April 1-Dec 31, 2017, then match tracks with those added to Today's Top Hits.[^31]

> 我们想要了解 Spotify 播放列表的收录是否在 Spotify 流媒体之外产生影响。我们可以获得的一个销售衡量标准是基于永久下载量的美国 iTunes 每日 top 100 排名。我们获取了 2017 年 4 月 1 日至 12 月 31 日的这些排名，然后将曲目与添加到 Today's Top Hits 的曲目进行匹配。[^31]

We are able to match 82 tracks we observe added to Today's Top Hits. Using the matching tracks, we regress iTunes sales ranks on a track fixed effect and an indicator for the period after the track is added to the playlist. We perform the estimation using windows from 2 to 10 days around the add date. If being added to the playlists stimulated sales of the track at iTunes, we would expect a negative coefficient, reflecting an improving rank. Instead, the coefficients are all positive. They are also significant, beginning with the specifications including 3 days on either side of the add event. This indicates that sales are dropping, relative to other songs, on iTunes even as songs are added to Today's Top Hits. Hence, we do not find any evidence of an impact of Spotify playlist decisions on popularity - and therefore revenue generation - outside of Spotify.

> 我们能够匹配我们观察到添加到 Today's Top Hits 的 82 首曲目。使用匹配的曲目，我们将 iTunes 销售排名回归到曲目固定效应和曲目添加到播放列表后时期的指示变量上。我们使用添加日期周围 2 到 10 天的窗口进行估计。如果被添加到播放列表刺激了曲目在 iTunes 的销售，我们预计会有一个负系数，反映排名的提升。相反，系数全部为正。它们也是显著的，从包括添加事件两侧 3 天的规格开始。这表明，即使曲目被添加到 Today's Top Hits，在 iTunes 上相对于其他歌曲，销售也在下降。因此，我们没有发现任何证据表明 Spotify 播放列表决策在 Spotify 之外对流行度——以及因此产生的收入——有影响。

## Notes

[^27]: While some songs appear more than once on Today's Top Hits, the songs included in the sample used in Table 3 only enter the list once. In the above calculations, we therefore assume that the effect of entering and exiting the playlist is the same for songs that would enter the playlist more than once.

[^28]: In our data, we observe that the Global Top 50 is based on either the streams from the previous day or from two days ago. The Global Top 50 playlist matched the previous day's streaming ranking for 133 days and the streaming ranking of two days earlier for 218 days during 2017. We therefore observe the songs that would have been ranked 51_s__t_ through 200_t__h_ for 351 days in 2017 (out of the 365).

[^29]: See [https://www.statista.com/statistics/487332/spotify-royalty-payment-costs/](https://www.statista.com/statistics/487332/spotify-royalty-payment-costs/).

[^30]: See [https://www.statista.com/statistics/367739/spotify-global-mau/](https://www.statista.com/statistics/367739/spotify-global-mau/).


# 5 New Music Friday Playlists and Product and Artist Discovery
**新的 Music Friday Playlists，产品发现和艺人发现**

Above we documented large and significant impacts of Spotify's playlist decisions on the success of songs added to major global curated playlists. As reflected in the fact that those songs had streaming histories prior to their addition to playlists, the songs added to the major global playlists are widely known prior to their addition to those playlists. "Product discovery" is an elastic term. Even a song well known to some people must be "discovered" before being adopted by others. Hence, even the major global playlists promote discovery of songs and artists. That said, the promotion of new music stands as a potentially different sort of product discovery, at least in degree if not also in kind. Moreover, the promotion of music that is not only new but is also by artists who are themselves new to the market offers a greater degree of product discovery that the promotion of widely known or even new songs by known artists. With these distinctions in mind, we turn now to analyses of Spotify playlists that explicitly promote new music, the New Music Friday lists.

> 上文我们记录了 Spotify 播放列表决策对添加到主要全球精选播放列表的歌曲成功的巨大和显著影响。正如这些歌曲在添加到播放列表之前已有流媒体历史所反映的那样，添加到主要全球播放列表的歌曲在添加到这些播放列表之前已广为人知。“产品发现”是一个弹性术语。即使一首对某些人来说很熟悉的歌曲，在被其他人采纳之前也必须被“发现”。因此，即使是主要全球播放列表也促进歌曲和艺术家的发现。也就是说，新音乐的推广代表了一种潜在不同类型的产品发现，至少在程度上（如果不是在种类上）。此外，推广不仅新而且由市场新艺术家创作的音乐，比推广广为人知或甚至由知名艺术家创作的新歌曲，提供了更大程度的产品发现。考虑到这些区别，我们现在转向分析明确推广新音乐的 Spotify 播放列表，即 New Music Friday 列表。

Each week, Spotify constructs a rank-ordered list of 50 new songs for each country in which it operates. These New Music Friday lists differ across country, albeit with overlap, so that across our 26 countries, Spotify recommended an average of 397 distinct songs per week during 2017. Of these songs, about 17 percent become successful in the sense of appearing in at least one country's top 200. This dwarfs the unconditional success rate. Of the 934,265 songs entering Spotify in 2017, only 19,055, or 2 percent, entered the daily streaming top 200 in at least one of our sample countries. This, in turn, suggests a benefit of the New Music Friday lists in reducing the costs consumers face in discovering which music to sample.

> 每周，Spotify 为其运营的每个国家构建一个包含 50 首新歌的排名列表。这些 New Music Friday 列表在不同国家间有所不同，尽管存在重叠，因此在我们的 26 个国家中，Spotify 在 2017 年每周平均推荐 397 首不同的歌曲。在这些歌曲中，大约 17% 被认为是成功的，因为它们至少在其中一个国家的 top 200 中出现。这使无条件成功率相形见绌。在 2017 年进入 Spotify 的 934,265 首歌曲中，只有 19,055 首，即 2%，在我们样本国家中至少一个国家的每日流媒体 top 200 中出现。这反过来表明，New Music Friday 列表在降低消费者发现哪些音乐值得试听的成本方面具有益处。

Some of the New Music Friday recommendations are for songs by already-known and successful artists, with whom listeners are already acquainted. Other recommendations are for songs by new and previously unknown artists, raising the possibility that these lists help with artist discovery. Songs almost always arrive on the New Music Friday list the day they are released, so we cannot use the before and after approach employed for the global lists above. Instead, we can ask how eventual streaming varies with songs' New Music Friday ranks. As a way to introduce our approach, we begin by showing the share of songs at each New Music Friday rank that ultimately appear in the recommended countries' top 200 daily streaming charts. Figure 4 summarizes these relationships for the top 20 recommended songs using all of the country-weeks in the sample.

> 一些 New Music Friday 的推荐是针对已有名气和成功的艺术家的歌曲，听众已经熟悉这些艺术家。其他推荐则针对新人及此前不为人知的艺术家，这表明这些列表可能有助于艺术家的发掘。歌曲几乎总是在发布当天就登上 New Music Friday 列表，因此我们无法使用上述全球列表中采用的之前和之后方法。相反，我们可以询问最终流媒体播放量如何随歌曲的 New Music Friday 排名而变化。作为介绍我们方法的一种方式，我们首先展示在每个 New Music Friday 排名中，最终出现在推荐国家每日 top 200 流媒体榜单中的歌曲比例。图 4 使用样本中的所有国家-周数据，总结了前 20 首推荐歌曲的这些关系。

![[Pasted image 20260315012924.png]]
`Figure 4: New Music Friday Ranking and Spotify Chart Appearance.`
`表4：周五新曲排行榜与Spotify榜单上榜情况`

Songs with better ranks on the New Music Friday playlists are more likely to appear on the daily Spotify top 200 streaming charts. Close to 85 percent of the songs ranked #1 on a country's New Music Friday lists appear on the country's streaming chart, as do over 80 percent of those ranked #2. The share charting declines monotonically in rank, reaching about 10 percent for songs ranked 20 (or, not shown, lower). We observe a similar relationship between recommendation rank and the share of songs appearing in the top 100, as well as in the top 50, 25, or 10 (not shown). In short, songs with top 10 recommendations have some chance of appearing in the top 200 or even the top 100, while songs recommended outside the top 20 are rather unlikely to achieve even the top 200.

> 在 New Music Friday 播放列表上排名更靠前的歌曲，更有可能出现在每日 Spotify 前 200 流媒体榜单中。在一个国家的 New Music Friday 列表上，接近 85% 排名第一的歌曲会出现在该国的流媒体榜单上，排名第二的歌曲也有超过 80% 如此。上榜份额随排名单调下降，对于排名 20 的歌曲，这一比例降至约 10%（或，未显示，更低排名）。我们观察到推荐排名与出现在前 100、前 50、前 25 或前 10（未显示）榜单的歌曲份额之间存在类似关系。简而言之，获得前 10 推荐的歌曲有一定机会出现在前 200 甚至前 100 榜单中，而推荐排名在前 20 之外的歌曲则不太可能甚至进入前 200 榜单。

Figure 4 shows that songs with higher-ranked recommendations tend to achieve higher streaming ranks. This is suggestive that high recommendation ranks matter for performance.

> 图 4 显示，推荐排名较高的歌曲往往获得更高的流媒体排名。、

But whether higher-ranked recommendations actually cause better streaming performance is another matter requiring different evidence. That is, the relationships in Figure 4 reflect some combination of a causal impact of New Music Friday list rank choices and the ability of list curators to predict which songs are headed for success regardless of the New Music Friday playlist ranks.

> 这表明高推荐排名对表现很重要。但更高排名的推荐是否实际上导致更好的流媒体表现是另一个需要不同证据的问题。也就是说，图 4 中的关系反映了 New Music Friday 榜单排名选择的因果影响以及榜单策划者预测哪些歌曲将取得成功的能力的组合，而不论 New Music Friday 播放列表的排名如何。

## 5.1 Song Fixed Effect Approach
**歌曲固定影响的方法**

The New Music Friday lists differ across countries, and this creates a possible empirical strategy for measuring the impact of New Music Friday ranks on success. Figure 5 provides an illustration of the cross-country variation in New Music Friday rankings, comparing the U.S. and Canadian New Music Friday lists released on December 10, 2017. The rankings are positively correlated, but they are substantially different. If we take the view that countries have similar tastes but are treated with different rankings, then we can measure the effects of New Music Friday rankings by comparing the streaming performance of the same songs in different countries where they have received different New Music Friday rankings.

> New Music Friday 列表在不同国家之间存在差异，这为衡量 New Music Friday 排名对成功的影响提供了一种可能的实证策略。图 5 展示了 New Music Friday 排名的跨国差异，比较了 2017 年 12 月 10 日发布的美国 和 加拿大 New Music Friday 列表。排名呈正相关，但存在显著差异。如果我们认为各国口味相似但被赋予不同排名，那么我们可以通过比较同一歌曲在不同国家中收到不同 New Music Friday 排名时的流媒体表现，来衡量 New Music Friday 排名的影响。

![[Pasted image 20260315013029.png]]
`Figure 5: New Music Friday Ranks in US and Canada.`
`表5：New Music Friday 在美国和加拿大的排名`

Figure 6 shows the U.S.-Canada rank differential distribution for the entire year. Of the songs appearing on both lists, the mean and median differential is roughly zero, but there is variation. The question asked by this measurement approach is whether the songs ranked higher in, say, the U.S. than Canada perform systematically better in the U.S. than Canada. Using a binary measure of whether a song (eventually) appears in the country's daily top 200 streaming chart as the outcome, the song-specific differential can take one of three values: 1, 0, and -1. Figure 7 shows the relationship between the rank differential on the horizontal axis and the smoothed outcome measure. Songs with a better rank in the U.S. are more likely to make the Spotify streaming charts in the U.S. than Canada. This is preliminary evidence that differential New Music Friday rankings give rise to differential stream success.

> 图 6 显示了全年的 U.S.-Canada 排名差异分布。在同时出现在两个榜单的歌曲中，均值与中位数差异大致为零，但仍存在波动。这一测量方法所探讨的问题是，例如在 U.S. 排名高于 Canada 的歌曲，是否在 U.S. 的表现系统性地优于其在 Canada 的表现。以歌曲是否（最终）进入该国每日前 200 流媒体排行榜作为二元结果指标时，歌曲特定差异可取值于三者之一：1、0 与 -1。图 7 展示了横轴上的排名差异与平滑后的结果测量之间的关系。在 U.S. 排名较高的歌曲，相较于 Canada，更有可能进入 U.S. 的 Spotify 流媒体排行榜。这为差异化的 New Music Friday 排名会引发差异化的流媒体成功提供了初步证据。

![[Pasted image 20260315013017.png]]
`Figure 6: New Music Friday Rank Differentials for US and Canada.`
`表6：美国和加拿大的 New Music Friday 排名差值`

![[Pasted image 20260315013108.png]]
`Figure 7: US-Canada New Music Friday Rank Differentials and Probability of Appearing in Top 200.`
`图7：美国-加拿大 New Music Friday 排名差异及进入前200名的概率`

To implement this approach for all countries via a regression, define $D _ { i c } ^ { 2 0 0 }$ to be a binary measure of whether song $i$ appears among the daily top 200 streaming songs in country $c$ at some point after entering the New Music Friday playlist. Next, define $\delta _ { i c } ^ { r }$ as a dummy that is 1 when song $i$ in country $c$ is ranked $r ^ { t h }$ on the country's New Music Friday list.

> 为了通过回归为所有国家实施这种方法，定义 $D _ { i c } ^ { 2 0 0 }$ 为一个二元指标，衡量歌曲 $i$ 在进入 New Music Friday 播放列表后，是否在某个时间点出现在国家 $c$ 的每日 top 200 流媒体歌曲中。接下来，定义 $\delta _ { i c } ^ { r }$ 为一个虚拟变量，当歌曲 $i$ 在国家 $c$ 的 New Music Friday 列表中排名第 $r ^ { t h }$ 时，该变量为 1。

As noted above in the discussion of Figure 4, a regression of $D _ { i c } ^ { 2 0 0 }$ on the $\delta _ { i c } ^ { r }$ terms does not indicate the effect of rank on streaming. The unobserved quality of the song - to the econometrician - affects both rank and streams. Presumably, songs that are good will have both high placements on the list and high streaming. If we had a measure of each song’s quality, then we could control for this directly, and then measure the impact of the New Music Friday ranks on streaming. While we do not observe song quality, we do observe whether the song appears in the Spotify top 200 streaming charts as well as the song’s New Music Friday rank in different countries. Hence, we can include a song fixed effect to control for its quality, then ask whether the song is more likely to appear in the streaming charts in countries where it has a more favorable recommendation. That is, we can estimate

$$ D _ {i c} ^ {2 0 0} = \alpha^ {r} \delta_ {i c} ^ {r} + \mu_ {c} + \eta_ {i} + \varepsilon_ {i c}. \tag {3} $$

In this setup $\eta _ { i }$ is the unobserved quality of song $i$ . Under the assumption that songs have similar appeal in different countries, or that $\eta _ { i }$ is the same across countries, the coefficients $\alpha ^ { r }$ show how ultimate streaming success varies with position on the New Music Friday list. That is, $\alpha ^ { r }$ provides evidence on the causal impact of higher recommendation ranks.

> 如上文对图 4 的讨论所述，将 $D _ { i c } ^ { 2 0 0 }$ 对 $\delta _ { i c } ^ { r }$ 项进行回归并不能表明排名对流量的影响。歌曲的未观测质量——对计量经济学家而言——同时影响排名和流量。推测而言，优质的歌曲在榜单上排名较高且流量也较高。如果我们能度量每首歌曲的质量，便可直接控制这一因素，进而衡量 New Music Friday 排名对流量的影响。尽管我们无法观测歌曲质量，但可以观测歌曲是否出现在 Spotify 前 200 流量榜单中，以及歌曲在不同国家的 New Music Friday 排名。因此，我们可以加入歌曲固定效应以控制其质量，进而探究歌曲在推荐更有利的国家是否更可能出现在流量榜单中。即，我们可以估计
> $$ D _ {i c} ^ {2 0 0} = \alpha^ {r} \delta_ {i c} ^ {r} + \mu_ {c} + \eta_ {i} + \varepsilon_ {i c}. \tag {3} $$
> 在此设定中，$\eta _ { i }$ 表示歌曲 $i$ 的未观测质量。在歌曲在不同国家具有相似吸引力或 $\eta _ { i }$ 跨国一致的假设下，系数 $\alpha ^ { r }$ 显示了最终流量成功如何随 New Music Friday 榜单上的位置而变化。也就是说，$\alpha ^ { r }$ 为更高推荐排名的因果影响提供了证据。

Figure 8 reports the estimated parameters $\alpha ^ { \prime }$ (with $\alpha ^ { 5 0 }$ normalized to 0) from two specifications, with and without song fixed effects. The line labelled "OLS," from the specification without song fixed effects, echoes the "top 200" bars in Figure 4. The "Song Fixed Effects" line comes from a specification including song fixed effects, and the size of the effect of a top ranking is smaller with the song FE included. Songs with a number 1 rank are over 80 percentage points more likely to appear on the streaming charts than songs ranked $5 0 ^ { t h }$ . After including song fixed effects, this differential shrinks to just below 50 percentage points. This finding is consistent with the idea that some part of the raw relationship between ranks and streams arises because curators give favorable ranks to songs they expect consumers will like, rather than a causal impact of the New Music Friday playlist ranking on streams. The effect falls sharply with rank, to about 18 percentage points at rank 10 and to about 4 percentage points at rank 20. (We provide evidence on statistical significance in Table 5 below).

> 图 8 报告了来自两种设定（包含和不包含歌曲固定效应）的估计参数 $\alpha ^ { \prime }$（其中 $\alpha ^ { 5 0 }$ 归一化为 0）。标记为“OLS”的线来自不包含歌曲固定效应的设定，它呼应了图 4 中的“top 200”条形图。“Song Fixed Effects”线来自包含歌曲固定效应的设定，并且加入歌曲固定效应后，顶级排名的影响规模变小。排名第 1 的歌曲比排名 $5 0 ^ { t h }$ 的歌曲在流媒体榜单上出现的可能性高出超过 80 个百分点。在包含歌曲固定效应后，这一差异缩小至略低于 50 个百分点。这一发现与以下观点一致：排名与流媒体播放量之间的原始关系部分源于策展人给予他们预计消费者会喜欢的歌曲有利排名，而非“New Music Friday”播放列表排名对流媒体播放量的因果影响。该效应随排名急剧下降，在排名 10 时降至约 18 个百分点，在排名 20 时降至约 4 个百分点。（我们在下表 5 中提供了统计显著性的证据）。

![[Pasted image 20260315013121.png]]
`Figure 8: Effect of Appearing in New Music Friday on Top 200 Streaming Chart Appearance.`
`表8：出现在 New Music Friday 对 Top 200 Streaming Chart 出现的影响`

![[Pasted image 20260315013406.png]]

Even controlling for song quality with song fixed effects, two main threats to identification remain. The first is that countries have different tastes, in which case perceived song quality would differ across countries, and a single song fixed effect that is common across countries would not control for song quality. A second challenge is that country-specific New Music Friday lists will differ across countries for endogenous reasons. We explore these in turn.

> 即使通过歌曲固定效应控制歌曲质量，识别仍面临两个主要威胁。首先是各国口味不同，在这种情况下，感知的歌曲质量会因国家而异，而一个跨国家通用的单一歌曲固定效应将无法控制歌曲质量。第二个挑战是，特定国家的 New Music Friday 列表会因内生原因而因国家而异。我们将依次探讨这些。

The song fixed effects approach assumes that unobserved song quality is the same across places where the song receives different ranks. This puts some burden on places having similar preferences. We deal with this by grouping countries with a common language, with an English-speaking group consisting of the US, Canada, and Great Britain and a Spanishspeaking group consisting of Spain, Mexico, and Colombia. We can verify the similarity of these countries' musical tastes, based on Spotify listening. Using the 2017 streaming data to create a vector for each country with the share of streams for each artist, we see that the correlations between linguistically similar countries' vectors are among the highest. The correlation for the US and Canada is 0.95, and the correlation for Mexico and Spain is 0.93. We then re-estimate (3) using only similar countries.

> 歌曲固定效应方法假设未观测到的歌曲质量在歌曲获得不同排名的地区是相同的。这给具有相似偏好的地区带来了一些负担。我们通过将国家按共同语言分组来处理这个问题，其中英语国家组包括 US 、 Canada 和 Great Britain ，西班牙语国家组包括 Spain 、 Mexico 和 Colombia 。我们可以基于 Spotify 收听数据来验证这些国家音乐品味的相似性。使用 2017 年的流媒体数据为每个国家创建一个向量，其中包含每位艺术家的流媒体份额，我们看到语言相似国家向量之间的相关性是最高的之一。US 和 Canada 的相关性为 0.95 ， Mexico 和 Spain 的相关性为 0.93 。然后，我们仅使用相似国家重新估计 (3) 。

Rather than report a proliferation of figures, we summarize our results by estimating (3) with three rank dummy variables (ranks 1-5, ranks 6-10, and ranks 11-30) rather than 49. Table 5 reports these results, starting with OLS and the baseline song fixed effects approaches in columns (1) and (2). Columns (3) and (4) report specifications using English (US, Canada, and Great Britain) and Spanish-language (Spain, Mexico, and Colombia) country groups, respectively, and results are quite similar to the baseline.[^32] Effects for ranks 1-5 are large, effects for ranks 6-10 are smaller but significant, and effects for ranks 11-30 are small and insignificant.

> 与其报告大量图表，我们通过使用三个等级虚拟变量（等级 1-5、等级 6-10 和等级 11-30）而非 49 个来估计（3），从而总结我们的结果。Table 5 报告了这些结果，从列（1）和（2）中的 OLS 和基线歌曲固定效应方法开始。列（3）和（4）分别报告了使用英语（US、Canada 和 Great Britain）和西班牙语（Spain、Mexico 和 Colombia）国家组的规格，结果与基线非常相似。[^32] 等级 1-5 的效应很大，等级 6-10 的效应较小但显著，而等级 11-30 的效应很小且不显著。

This still leaves a concern that ranks are endogenously different across countries. Perhaps the most salient concern arises from domestic music, which one might expect to be both better-ranked on its home-county New Music Friday list, as well as better-performing on its domestic streaming chart but not because the better ranking causes the better performance. The New Music Friday lists have elevated ranks for domestic music: on average domestic music makes up 15 percent more of the New Music Friday listings at home than abroad. To avoid this problem, we re-estimate the model excluding domestic music. Results, in column (5) of Table 5, are very similar to the baseline results.

> 这仍然留下一个担忧，即排名在不同国家之间是内生性不同的。或许最显著的担忧来自国内音乐，人们可能预期国内音乐在其本国的 New Music Friday 列表上排名更好，同时在其国内流媒体图表上表现更佳，但并非因为更好的排名导致了更好的表现。New Music Friday 列表对国内音乐给予了更高的排名：平均而言，国内音乐在国内的 New Music Friday 列表中所占比例比在国外高出 15 percent。为了避免这个问题，我们重新估计了排除国内音乐的模型。结果，在 Table 5 的 column (5) 中，与基线结果非常相似。

## 5.2 New Songs and Artists
**新的歌曲与艺术家**

While all of the songs entering the New Music Friday lists are new, many are by established artists. While the popularization of a new song, even if by an established artist, requires product discovery on the part of curators and consumers, ascertaining whether the New Music Friday list can promote discovery of works by new artists is of separate interest. In order to study artist discovery we would like to estimate the New Music Friday effect separately for artists who are not already widely known to consumers. To this end we reestimate the model including only songs by less-well-known artists. Column (6) of Table 5 includes only independent-label artists without streams in the 2016 data, and results are similar. Column (7) includes only the demonstrably new artists, those who not only have no streams in 2016 but whose first recording appears in 2017. This reduces the sample size sharply, to 2,221. Still, results remain quite similar, although standard errors rise. Column (8) uses only the new artists and excludes domestic music. Results are again quite similar. Finally, column (9) uses new independent artists, again with similar results. We conclude that the New Music Friday playlists aid in the discovery of new artists.

> 虽然所有进入 New Music Friday 列表的歌曲都是新的，但许多是由知名艺术家创作的。尽管一首新歌的推广，即使是由知名艺术家创作，也需要策展人和消费者进行产品发现，但确定 New Music Friday 列表是否能促进新艺术家作品的发现则具有独立意义。为了研究艺术家的发现，我们希望对那些尚未被消费者广泛知晓的艺术家单独估计 New Music Friday 效应。为此，我们重新估计了模型，仅包括不太知名艺术家的歌曲。表 5 的第 (6) 列仅包括在 2016 年数据中没有流量的独立厂牌艺术家，结果相似。第 (7) 列仅包括明显的新艺术家，即那些不仅在 2016 年没有流量，而且其首次录音出现在 2017 年的艺术家。这使样本量急剧减少，至 2,221。尽管如此，结果仍然相当相似，尽管标准误差上升。第 (8) 列仅使用新艺术家并排除国内音乐。结果再次相当相似。最后，第 (9) 列使用新的独立艺术家，结果再次相似。我们得出结论，New Music Friday 播放列表有助于新艺术家的发现。

## 5.3 Instrumental Variables Approach
**工具变量法**

Even with domestic music excluded, one can be concerned that the differential rankings of, say, French songs in the US and Germany may endogenously reflect differential curatorial expectations about tastes in the two countries. To get around this we would require a source of variation in the rank of particular songs across countries that is unrelated to the appeal of the song.

> 即便排除国内音乐的影响，人们仍可能担忧——例如法国歌曲在美国和德国的排名差异，可能内在地反映了两国策展方对听众品味的预期差异。为规避这一问题，我们需要找到特定歌曲在各国间排名差异的来源，且该差异需与歌曲本身的吸引力无关。

Home bias, along with different-sized home markets, gives us a possible strategy. Suppose there is home bias in the New Music Friday lists, so that a disproportionate share of the songs on the New Music Friday lists are domestic in each country. Suppose further that because of differences in market size, there are different amounts of domestic music in each market. Then non-domestic music would receive worse ranks in larger markets, simply because it was more likely to be pushed down the ranking by domestic music. For our purpose, this would give us a reason why particular songs would achieve different New Music Friday ranks in different countries that is unrelated to the appeal of the song in the two countries.

> 本土偏好，连同不同规模的本土市场，为我们提供了一种可能的策略。假设在 New Music Friday 列表中存在本土偏好，因此每个国家的 New Music Friday 列表中的歌曲中，本土歌曲所占比例过高。进一步假设，由于市场规模的不同，每个市场中本土音乐的数量也不同。那么，非本土音乐在较大的市场中会获得更差的排名，仅仅是因为它更有可能被本土音乐推低排名。对于我们的目的而言，这将为我们提供一个理由，解释为什么特定歌曲在不同国家会获得不同的 New Music Friday 排名，而这与歌曲在两个国家的吸引力无关。

To explore this strategy, we use the total Spotify streams (among the top 200) as a measure of market size for each country. Using only the non-domestic songs, we then run a first-stage regression of the songs' New Music Friday ranks on song fixed effects and the music market size variable (total streams in the country). The coefficient on the market size variable indicates whether a given song has a worse (higher) rank in a country with a larger market, and the coefficient is large and significant (see Table 6).

> 为了探索这一策略，我们使用总 Spotify 流媒体量（前 200 名中）作为每个国家市场规模的衡量指标。仅使用非本土歌曲，我们随后对歌曲的 New Music Friday 排名进行第一阶段回归，以歌曲固定效应和音乐市场规模变量（该国的总流媒体量）为自变量。市场规模变量的系数表明，给定歌曲在市场规模较大的国家是否具有更差（更高）的排名，且该系数大且显著（见表 6）。

![[Pasted image 20260315013416.png]]

We then implement this directly in a regression of our streaming measure (whether a song appears in the top 200 on song fixed effects as well as its New Music Friday rank, instrumenting the rank with the market size measure. We have only one instrument, so we can only use one measure of New Music Friday rank. We explore both the level and the log of the New Music Friday rank.

> 然后，我们直接在回归中实现这一点，回归我们的流媒体测量（无论一首歌是否出现在前 200 名中），基于歌曲固定效应以及其 New Music Friday 排名，使用市场规模测量作为排名的工具变量。我们只有一个工具变量，因此我们只能使用 New Music Friday 排名的一个测量。我们探索了 New Music Friday 排名的水平和对数。

Columns (1) and (5) of Table 6 report OLS regressions of the streaming measure on the level and the log of the New Music Friday rank, respectively, without fixed effects. The resulting coefficients reflect both the determinants of ranks and their effects. Columns (2) and (6) then include song fixed effects, and - as in our earlier exercises - the coefficient on rank falls by roughly half. Columns (3) and (7) report the first stage regressions of the level and the log of the New Music Friday rank on song fixed effects as well as market size, estimated with robust standard errors. The market size measure is positively and significantly related to rank, indicating that non-domestic songs have worse (higher) ranks in countries with larger music markets. Columns (4) and (8) continue to include song fixed effects and also instrument the rank measures using market size. Robust standard errors are reported. Coefficients are similar to the song FE estimates, although standard errors are much larger, and the coefficients are slightly smaller in absolute value. We take the similarity of the IV estimates to the FE estimates to indicate that our basic estimates do not arise from endogenous New Music Friday ranks.

> 表 6 的第 (1) 列和第 (5) 列分别报告了流媒体指标对 New Music Friday 排名的水平和对数的 OLS 回归，未包含固定效应。所得系数既反映了排名的决定因素，也反映了其影响。随后，第 (2) 列和第 (6) 列包含了歌曲固定效应，并且——正如我们之前的练习一样——排名系数大致下降了一半。第 (3) 列和第 (7) 列报告了 New Music Friday 排名的水平和对数对歌曲固定效应以及市场规模的 first stage 回归，估计时使用了稳健标准误。市场规模指标与排名呈显著正相关，表明非本土歌曲在音乐市场较大的国家中排名更差（更高）。第 (4) 列和第 (8) 列继续包含歌曲固定效应，并使用市场规模作为工具变量对排名指标进行工具变量估计。报告了稳健标准误。系数与歌曲 FE 估计值相似，尽管标准误大得多，且系数的绝对值略小。我们将 IV 估计值与 FE 估计值的相似性视为表明我们的基本估计并非源于内生性 New Music Friday 排名。

## 5.4 Effects over Time
**长期效应**

Songs remain on the New Music Friday lists for only seven days. To the extent that listeners use the New Music Friday playlists as a utility for playing recommended songs, we would expect a clear effect during the week that songs remain on the list. Effects could continue past the time on the list, for example via the information communicated by list inclusion.

> 歌曲仅在 New Music Friday 列表上保留七天。就听众将 New Music Friday 播放列表用作播放推荐歌曲的工具而言，我们预期在歌曲留在列表上的那一周内会有明显效果。效果可能会在列表时间之后持续，例如通过入选列表所传达的信息。

Here we explore whether New Music Friday effects are persistent. We adapt the estimation framework of equation (3) slightly to estimate effects over time. Define $D _ { i c \tau } ^ { 2 0 0 }$ as a binary measure that is 1 if song $i$ appears in the streaming top 200 in country c $\tau$ days after appearance on country $c$'s New Music Friday list:

$$ D _ {i c \tau} ^ {2 0 0} = \alpha_ {\tau} ^ {r} \delta_ {i c} ^ {r} + \mu_ {c} + \eta_ {i} + \varepsilon_ {i c \tau}. \tag {4} $$

Then the parameter $\alpha _ { \tau } ^ { r }$ indicates the additional propensity to be among the top 200 streaming songs $\tau$ days after being added to the list.

> 这里我们探讨 New Music Friday 效应是否具有持续性。我们略微调整方程（3）的估计框架，以估计随时间变化的影响。定义 $D _ { i c \tau } ^ { 2 0 0 }$ 为一个二元指标，如果歌曲 $i$ 在国家 c 的 New Music Friday 列表上出现后 $\tau$ 天，出现在该国流媒体前 200 名中，则该指标为 1：
> $$ D _ {i c \tau} ^ {2 0 0} = \alpha_ {\tau} ^ {r} \delta_ {i c} ^ {r} + \mu_ {c} + \eta_ {i} + \varepsilon_ {i c \tau}. \tag {4} $$
> 那么，参数 $\alpha _ { \tau } ^ { r }$ 表示在加入列表后 $\tau$ 天，成为流媒体前 200 名歌曲的额外倾向。

Figures 9 and 10 reports three sets of estimates for different groups of ranks. Figure 9 covers only the first 14 days after the appearance of the New Music Friday list. The leftmost figure shows how the effect of appearing in the top 5 varies across days since appearance. The center figure repeats the analysis for songs ranked 6-10, and the rightmost left figure reports it for songs ranked 11-30.

> 图 9 和 图 10 报告了三组针对不同排名组的估计。图 9 仅涵盖了 New Music Friday 列表出现后的前 14 天。最左侧的图显示了出现在前 5 名的影响如何随着出现后的天数而变化。中间的图对排名 6-10 的歌曲重复了这一分析，而最右侧的图报告了排名 11-30 的歌曲的情况。

![[Pasted image 20260315013153.png]]
`Figure 9: Effect Over Time of Appearing in New Music Friday - First 14 Days.`
`表9：出现在 New Music Friday 中的随时间效应 - 前14天`

![[Pasted image 20260315013211.png]]
`Figure 10: Effect Over Time of Appearing in New Music Friday.`
`表10：在 New Music Friday 中出现的随时间效应`

As Figure 9 shows, there are large and immediate effects of songs appearing on the New Music Friday lists. These effects rise for the first four days, then decline. There is no sharp decline after day 7, when the songs leave the lists. And indeed, as Figure 10 shows, the effects persist for 100 days after appearance on the list, indicating that the effects of the New Music Friday lists are not merely mechanical. In short, there are large, persistent, and significant effects for songs in the top 5 and large but smaller effects for songs ranked 6-10. Effects for songs ranked 11-30 are small.

> 如图 9 所示，歌曲出现在 New Music Friday 列表上会产生巨大且即时的影响。这些影响在前四天上升，然后下降。在第 7 天歌曲离开列表后，没有急剧下降。事实上，如图 10 所示，这些影响在出现在列表后持续 100 天，表明 New Music Friday 列表的影响不仅仅是机械性的。简而言之，对于排名前 5 的歌曲，有巨大、持久且显著的影响，而对于排名 6-10 的歌曲，影响巨大但较小。对于排名 11-30 的歌曲，影响较小。

## 5.5 Aggregate Effects on Streams
**对流量的累计影响**

We are interested in impacts of list inclusion on the total number of streams. We can construct measures of country-level streams for each song, subject to the caveat that we only observe streams when a song is among the daily top 200. Hence, our measure understates streaming, particularly for lower-ranked songs that are more commonly outside the top 200.

> 我们关注列表收录对总流媒体数量的影响。我们可以为每首歌构建国家层面的流媒体量度，但需要注意的是，我们只在一首歌进入每日前 200 名时才能观察到其流媒体数据。因此，我们的量度低估了流媒体量，特别是对于那些排名较低、更常处于前 200 名之外的歌曲。

Figure 11 aggregates the effect over time, reporting the aggregate result by rank. A number 1 ranking adds about 550 normalized streams (corresponding to about 14,000,000 additional streams for a song ranked #1 on the U.S. chart). A song ranked #5 gets over 80 additional normalized streams, or about 2.1 million additional U.S. streams for a #5 ranking on the U.S. New Music Friday playlist. The effects peak within a few days after appearance on the New Music Friday list.

> 图 11 汇总了随时间变化的效果，按排名报告了汇总结果。排名第一增加约 550 个标准化流（对应一首在 U.S. 榜单上排名第一的歌曲约 14,000,000 个额外流）。排名第五的歌曲获得超过 80 个额外标准化流，或对于在 U.S. New Music Friday 播放列表上排名第五的歌曲，约 210 万额外 U.S. 流。效果在出现在 New Music Friday 列表后的几天内达到峰值。

![[Pasted image 20260315013225.png]]
`Figure 11: Effect of Appearing in New Music Friday on Normalized Streams.`
`表11：出现在 New Music Friday 对标准化流量的影响`

With Spotify's ostensible payments of $6 and $8.4 per thousand streams, the benefit of being ranked #1 on the U.S. New Music Friday playlist is worth between $83,600 and $117,100, including only the direct benefits arising from Spotify payments.

> 随着 Spotify 每千次流媒体播放的明显支付为 6 美元和 8.4 美元，在 U.S. New Music Friday playlist 上排名第一的收益价值在 83,600 美元到 117,100 美元之间，仅包括来自 Spotify 支付的直接收益。

## Notes

[^31]: The iTunes rankings are from itunescharts.net/us/charts/songs/2017/.

[^32]: We also obtain very similar results using only the US and Canada, and Spain and Mexico, respectively.


# 6 Which Types of Songs Do Spotify Playlists Promote?
**Spotify播放列表推广哪些类型的歌曲？**

Rights holders in the independent record label community have long lamented their limited access to radio airplay (Thomson, 2009). Even in the streaming era, with its relaxed distribution bottlenecks, concerns remain. It is not uncommon to read assertions that playlists are "controlled by three major labels: Universal Music Group, Sony Music Entertainment, and Warner Music Group, a group that collectively owns a very substantial ownership share of not just Spotify, but other platforms like VEVO." In this section we descriptively explore a few questions relevant to these ostensible concerns, asking which sorts of songs, by label type and national origin, are available and commonly streamed at Spotify. Further, which sorts of songs appear on the global curated and the country-specific New Music Friday playlists?

> 独立唱片公司社群的权利持有者长期以来一直哀叹他们获得电台播放的机会有限（ Thomson, 2009 ）。即使在流媒体时代，随着分销瓶颈的缓解，担忧依然存在。经常可以读到这样的断言：播放列表“由三大主要唱片公司控制： Universal Music Group 、 Sony Music Entertainment 和 Warner Music Group ，这个集团不仅拥有 Spotify 的相当大所有权份额，还拥有其他平台如 VEVO 的所有权份额。”在本节中，我们描述性地探讨了与这些表面担忧相关的几个问题，询问哪些类型的歌曲，按唱片公司类型和国籍，在 Spotify 上可用且常被流播放。此外，哪些类型的歌曲出现在全球策划的和国家特定的 New Music Friday 播放列表上？

As Table 7 shows, among the 19,055 songs that we observe streaming in the 2017 countryspecific sample, just under half (measured by either listings or distinct songs) are from independent record labels. The independent share of streams, however, is much smaller, at just over a quarter. U.S. origin songs make up a quarter of listings and songs in the country-level sample but account for 59 percent of streams. Domestic songs make up just over a quarter of listings, distinct songs, and streams in the country-level data on average.

> 如表 7 所示，在我们观察到的 2017 年国家特定样本中流媒体的 19,055 首歌曲中，略低于一半（以列表或独特歌曲衡量）来自独立唱片公司。然而，独立唱片公司在流媒体中的份额要小得多，仅略高于四分之一。U.S. 原产歌曲在国家级样本中占列表和歌曲的四分之一，但占流媒体的 59％。在国内歌曲中，平均在国家级数据中占列表、独特歌曲和流媒体的略高于四分之一。

![[Pasted image 20260315013426.png]]

The song sample made up of the global daily top 200 includes only 1,764 songs. Of these, independent songs account for a quarter of the tracks and just under a fifth of streams. U.S. origin songs account for 68 percent of these tracks and 71 percent of streams.

> 由全球每日前 200 名组成的歌曲样本仅包含 1,764 首歌曲。其中，独立歌曲占曲目的四分之一，流媒体播放量略低于五分之一。U.S. 原产歌曲占这些曲目的 68% 和流媒体播放量的 71%。

How about the playlists? Independent-label songs account for well under half of the listings and distinct songs at the global curated lists, while US-origin tracks account for roughly three quarters or more of the listings and songs, as well as streams, appearing on the global curated lists.

> 那么播放列表呢？独立厂牌的歌曲在全球精选列表中占不到一半的列表和独特歌曲，而 US 原产曲目则占大约四分之三或更多的列表、歌曲以及流媒体播放量，这些出现在全球精选列表中。

The New Music Friday lists have different coverage. First, they include greater independent music representation, just over half of the tracks overall. Second, they include less USorigin representation, accounting for roughly a third of listings and songs. Finally, domestic music makes up just under a fifth of the New Music Friday listings and songs. Given the large number of origin countries in the world, this average reflects a substantial amount of home bias. On average, origin repertoires make up 15 percentage points more of the New Music Friday lists in their home countries, relative to their origin shares outside of the home country.

> New Music Friday 列表的覆盖范围有所不同。首先，它们包含了更多的独立音乐代表，总体略超过一半的曲目。其次，它们包含较少的美国原产代表，约占列表和歌曲的三分之一。最后，国内音乐占 New Music Friday 列表和歌曲的略低于五分之一。鉴于世界上原产国数量众多，这一平均值反映了相当大的本土偏好。平均而言，原产曲目在本国 New Music Friday 列表中的占比，相对于其在本国以外的原产份额，高出 15 个百分点。

# 7 Conclusion
**结论**

Streaming has emerged as an important channel for music consumption, and Spotify is the most prominent platform, with a higher market share than was held by retailers or radio stations in the digital era. This paper has measured the power of Spotify to influence song success with its general playlists, and we find clear evidence that Spotify has power to influence consumption decisions. We document large and statistically significant effects. The major global playlists raise streams for prominent songs substantially. Getting on Today's Top Hits is worth almost 20 million additional streams, which translates to $116,000 and $163,000 in additional revenue from Spotify alone. Playlists also affect the success of new songs and new artists. Getting on the top of the New Music Friday playlist in the U.S. is worth roughly 14 million streams ($84,000-$117,000). Making the Global Top 50 chart raises streams by about 59,000 per day, or by about 3 million overall. Playlists have important impacts on which songs are heavily streamed. The major global lists tend to promote major-label and US-origin music, while the New Music Friday lists provide heavier coverage of independent and domestic music.

> 流媒体已成为音乐消费的重要渠道，Spotify 是最突出的平台，其市场份额超过了数字时代的零售商或广播电台。本文测量了 Spotify 通过其通用播放列表影响歌曲成功的能力，我们发现明确的证据表明 Spotify 有能力影响消费决策。我们记录了巨大且统计上显著的影响。主要的全球播放列表显著提升了知名歌曲的流媒体播放量。登上 Today's Top Hits 播放列表几乎相当于额外获得 2000 万次流媒体播放，这仅从 Spotify 平台就转化为 116,000 美元到 163,000 美元的额外收入。播放列表也影响新歌曲和新艺术家的成功。登上美国 New Music Friday 播放列表的顶部大约相当于 1400 万次流媒体播放（84,000 美元到 117,000 美元）。登上 Global Top 50 榜单每天提升约 59,000 次流媒体播放，或总体提升约 300 万次。播放列表对哪些歌曲被大量播放有重要影响。主要的全球列表倾向于推广大厂牌和美国起源的音乐，而 New Music Friday 列表更侧重于独立和国内音乐。

The fact that playlists have substantial impacts on song success should be of interest for both music industry participants and observers of platforms more generally. Growing concentration in the streaming market, as well as other markets dominated by one or a few players, may create a need for scrutiny of how platforms exercise their power.

> 播放列表对歌曲成功具有重大影响这一事实，应引起音乐行业参与者以及更广泛平台观察者的兴趣。流媒体市场以及其他由一两个主导者控制的市场日益集中，可能需要对平台如何行使权力进行审查。

# References
**参考文献**

- Adomavicius, G. and A. Tuzhilin (2005): "Toward the next generation of recommender systems: A survey of the state-of-the-art and possible extensions," IEEE transactions on knowledge and data engineering, 17, 734–749.
- Aguiar, L. (2017): "Let the music play? Free streaming and its effects on digital music consumption," Information Economics and Policy, 41, 1–14.
- Arrington, M. (2009): "This Is Quite Possibly The Spotify Cap Table." Techcrunch, [https://techcrunch.com/2009/08/07/this-is-quite-possibly-the-sp](https://techcrunch.com/2009/08/07/this-is-quite-possibly-the-sp) otify-cap-table/, August 7.
- Bertoni, S. (2013): "How Spotify Made Lorde A Pop Superstar," Forbes, [https://www.f](https://www.f/) orbes.com/sites/stevenbertoni/2013/11/26/how-spotify-made-lorde-a-pop-sup erstar/, November 26.
- Cookson, R. (2015): "Spotify bans 'payola' on playlists," Financial Times, https://www .ft.com/content/af1728ca-4740-11e5-af2f-4d6e0e5eda22, August 20.
- Corniere, A. and G. Taylor (2014): "Integration and search engine bias," The RAND Journal of Economics, 45, 576–597.
- Datta, H., G. Knox, and B. J. Bronnenberg (2017): "Changing their tune: How consumers' adoption of online streaming affects music consumption and discovery," Marketing Science.
- DellaVigna, S. and J. Hermle (2017): "Does Conflict of Interest Lead to Biased Coverage? Evidence from Movie Reviews," Review of Economic Studies, 84, 1510–1550.
- Dertouzos, J. N. (2008): "Radio Airplay and the Record Industry: An Economic Analysis," National Association of Broadcasters, USA.
- Edelman, B. (2011): "Bias in search results: Diagnosis and response," Indian JL & Tech., 7, 16.
- Hagiu, A. and B. Jullien (2011): "Why do intermediaries divert search?" The RAND Journal of Economics, 42, 337–362.
- Ip, G. (2018): "The Antitrust Case Against Facebook, Google and Amazon," Wall Street Journal, [https://www.wsj.com/articles/the-antitrust-case-against-facebook-g](https://www.wsj.com/articles/the-antitrust-case-against-facebook-g) oogle-amazon-and-apple-1516121561, January 16.
- Lee, D. S. and T. Lemieux (2010): "Regression discontinuity designs in economics," Journal of economic literature, 48, 281–355.
- Lewis, R., J. M. Rao, and D. H. Reiley (2015): "Measuring the effects of advertising: The digital frontier," in Economic Analysis of the Digital Economy, University of Chicago Press, 191–218.
- Liebowitz, S. J. (2004): "The elusive symbiosis: The impact of radio on the record industry," Review of Economic Research on Copyright Issues, 93–118.
- Lindvall, H. (2009): "Behind the music: The real reason why the major labels love Spotify," The Guardian, [https://www.theguardian.com/music/musicblog/2009/aug/17/](https://www.theguardian.com/music/musicblog/2009/aug/17/) major-labels-spotify, August 17.
- McBride, S. (2014): "WRITTEN DIRECT TESTIMONY OF STEPHAN MCBRIDE (On behalf of Pandora Media, Inc)," [http://www.loc.gov/crb/rate/14-CRB-0001-WR](http://www.loc.gov/crb/rate/14-CRB-0001-WR) /statements/Pandora/13_Written_Direct_Testimony_of_Stephan_McBride_with_F igures_and_Tables_and_Appendices_PUBLIC_pdf.pdf, Filed with Copyright Royalty Board, Washington, DC.
- Nayman, L. (2012): "Rock 'n' Roll Payola: Dick Clark and Alan Freed." In These Times, [http://inthesetimes.com/article/13100/rock_n_roll_payola_dick_clark](http://inthesetimes.com/article/13100/rock_n_roll_payola_dick_clark) _and_alan_freed, April 24
- Peoples, G. (2016): "How a Licensing Deal Between Merlin and Pandora Cast a Tall Shadow Over New Webcasting Rates." Billboard, [https://www.billboard.com/articl](https://www.billboard.com/articl) es/business/6889363/merlin-pandora-webcasting-iv-copyright-royalty-boardwarner-iheartradio, February 25.
- Porzecanski, K. (2018): "Soros Says Google, Facebook Are Near-Monopolies That Spur Addiction." Bloomberg Business Week, [https://www.bloomberg.com/news/articles/](https://www.bloomberg.com/news/articles/) 2018-01-25/soros-says-google-facebook-are-near-monopolies-spur-addiction, January 25.
- Reinstein, D. A. and C. M. Snyder (2005): "The influence of expert reviews on consumer demand for experience goods: A case study of movie critics," The journal of industrial economics, 53, 27–51.
- Reuter, J. and E. Zitzewitz (2006): "Do ads influence editors? Advertising and bias in the financial media," The Quarterly Journal of Economics, 121, 197–227.
- Richardson, M. and S. Wilkie (2015): "Faddists, enthusiasts and Canadian divas: broadcasting quotas and the supply response," Review of International Economics, 23, 404–424.
- Rysman, M. (2009): "The economics of two-sided markets," Journal of Economic Perspectives, 23, 125–43.
- Salganik, M. J., P. S. Dodds, and D. J. Watts (2006): "Experimental study of inequality and unpredictability in an artificial cultural market," science, 311, 854–856.
- Sorensen, A. T. (2007): "Bestseller lists and product variety," The journal of industrial economics, 55, 715–738.
- Thomson, K. (2009): "Same Old Song," Future of Music Coalition, https://futureofmu sic.org/article/research/same-old-song, April 29.
- United States Securities and Exchange Commission (2018): "Form F-1 Registration Statement, Spotify Technology, S.A." [https://www.sec.gov/Archives/edgar/dat](https://www.sec.gov/Archives/edgar/dat) a/1639920/000119312518063434/d494294df1.htm#rom494294_14.
- Waldfogel, J. (2017): "How Digitization Has Created a Golden Age of Music, Movies, Books, and Television," Journal of Economic Perspectives, 31, 195–214.
- Zentner, A., M. Smith, and C. Kaya (2013): "How video rental patterns change as consumers move online," Management Science, 59, 2622–2634.
- Zhu, F. and Q. Liu (2016): "Competing with complementors: An empirical look at amazon.com," .