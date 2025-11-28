# Decision Intelligence? Yes, please.

*Published: January 30, 2023*

*Originally published on [Medium](https://medium.com/@ake.edlund/decision-intelligence-yes-please-19ea9e66fa26)*

I've been a regular Medium reader for quite some time now, and for me one of the main reasons for joining was the generous sharing of hard earned experiences from people.

I remember for example reading about "What I wish I knew before choosing X" where 'X' was a technology choice we just had made in my company. The article had an image of something burning with high flames.

Good insights, always to be taken with some grains of salt, and always telling yourself that 'OK, they were unlucky/too early/not so smart. We're different'. You wish…

Now it's high time for me to start giving back, maybe giving some readers some insight or at least the feeling that they are not alone, or maybe even the warm feeling of being waaay better than this guy and his team mates.

Now to the click bait title, anything with 'Decision Intelligence' should, rightfully, cause some interest from anyone trying to make a living in the analytics domain.

Disclaimer, late I know, this text is just another confirmation of the importance of what especially [Cassie Kozyrkov](https://medium.com/@kozyrkov) is articulating so well. If that is what you really want to know more about stop reading this, and [go here](https://medium.com/towards-data-science/introduction-to-decision-intelligence-5d147ddab767).

Here we go.

## The party is all set.

We got plenty of data and people who are really good at making the data 'sing', we got the owners of the data, who want nothing more than putting it to a spin — to see what we all can make from it. We got math wizards and hackers, we got business guys and one or two 'we know more about this area than anyone'. We got the [Drew Conway Venn diagram](http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram) all covered, many times over.

But where do you start? Our original 'way of working' was, back at the old (sic!) data lake time, to first get the data then go out hunting for business. That was not easy for various reasons, and a topic of its own (clue: try convincing business owners to jump onto the cool ML train, business owners who still are not superhappy of earlier BI journeys).

Over time, after many cold calls and misunderstandings, we did get better at storytelling and making a case for an MVP or at least a POC ('POC graveyards' is/should already be covered here at Medium, if not please add it — the main reason for MLOps of today).

## Talk to the right person.

Obvious, right? Not so easy. In larger corporations there are many people between an analytics team and its intended customer. All these people are needed, I'm sure, but as someone who wants to make a difference using analytics we do need to talk to the person who makes the actual decision and the person(s) who knows all relevant details about the target area/system/process/…

In one project we, me and my data science colleague, spent some (close to 6 months in the end) months developing models to predict failures in a specific telco service. At one point (in the end) we were giving a demo at an internal analytics summit, demoing what we were working on, and some cool deep learning techniques fresh out of arXiv, that we'd love to try on some projects (if anyone would, please, understand how cool it would be).

A senior engineer came by. He had seen some plots from our ongoing predictive maintenance project. He was interested since he'd been working hands-on with this exact telco service for years. Many. Years. He politely had some questions. It was clear that he didn't want to embarrass us, but the questions were very basic, and very clearly making us look anything but cool.

'What weather data did you use? You know snow has a clear impact on these things. Not to mention hot Summers, boy!' Again, he was just curious, as any good engineer. Ending with the comment that finally put a big question mark to our project: 'You know we always run these things with backup components, just in case something would break'.

So what had happened here? We started the project with a good motivation: the value of predicting failures in these systems was clear, everyone knew that. In addition there were some plans of maybe buying a solution from outside, instead of building it in-house.

Value — check.

Making sure we beat the external solution proving our value to the company — yes, we'll do that!

Talking to the right person? No, obviously not.

## Get the metric right. Get a sign-off: target to reach, commitment to act if target reached.

A first warning sign (in the same project as above) was when we discussed the metrics for success, we really tried to get a commitment from business to use our predictions for actual decisioning, and to get there we needed to have an agreed metric and a value attached to that metric.

The warning sign was in one of the first meetings when the external vendor was impressing our business with 'very high accuracy'. Now. In these environments the failures are rare (making it extra hard to do predictive modeling). Very rare. So rare that anyone could bring the default dummy model and have great accuracy. 'I predict no failures. Oh, I got 99% accuracy, cool!'. No, not cool.

So, in one way we earned our place in the project by asking some questions around the right metric to use, getting our own business to understand why this was a cheap trick from the vendor.

Now. Did we get a metric and a target to reach? And were these grounded in the actual value it would bring to the company, if used, if making decisions based on our analysis, on our data?

Yes and no. It was clearly not fully understood and founded, and eventually the performance of our models (did beat the vendor's) were not high enough to be used. We did save the company a lot of money, not buying an external solution (that wouldn't have been used anyway). But we could have stopped months earlier.

## More examples, same mistakes

In the second example, if I didn't lose you already, we got all wild into trying a bunch of deep learning architectures, the whole (at that time) shebang, all to help out creating a good text classifier (think customer support area).

Again the value was clear, and others (external data science team) had had a go at it. We could do much better in a very much shorter time. We got this new bunch of new tools in our bag, and we were going to use it.

Again. Yes, we did waay better than the competition, and I took a fraction of the time it had taken them. So, was it used?

No. This time it was due to more practical limitations: yes we could classify the texts into 40+ reasonable groupings, all making perfect sense to the service people. But, in reality the mail threads moved over classes, plus the service people handled many classes in parallel (of course), and — as so often — the problem we were solving was far away from the problems they had to solve first. We were basically suggesting 240 sandpaper before the 40.

And, also in this case we didn't get to talk to all the right people until the end. And again we didn't agree beforehand of commitment to use (if good enough) what we developed.

## Do your homework

Maybe one more lesson from above would be:

> Just because others have tried earlier, doesn't grant that the problem is correctly formulated.

In both examples we had better results than earlier teams and, also in head-on competition. Still, doesn't mean it was the right game to play, at all. I guess that the lesson could be summarised as 'Do your homework!'.

Above were examples from five years ago. Do expect more, both from the last five years, but for sure from future mistakes.

---

*This article reflects on lessons learned from analytics projects and the importance of decision intelligence in data science work.*
