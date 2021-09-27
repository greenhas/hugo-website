+++
draft = false
date = 2021-09-10T12:01:57-04:00
title = "positivism, transparency, and ethics in data science"
slug = "positivism-transparency-and-ethics-in-data-science" 
tags = ["data science", "philosophy of science", "research paradigms", "positivism", "open science"]
categories = ["macro"]
+++

This semester, I'm teaching my unit's graduate *Introduction to Data Science* course for the first time, which I'm very excited about. One of the first changes I made to the syllabus was to move the "transparency, ethics, and privacy" module from the end of the semester to the near-beginning, and writing the "lecture" for that module has proven to be a real treat.

Over the past few years, I've had really good conversations with colleagues about the tension that exists between the (laudable) values of open science and the (equally laudable) values of data ethics and privacy. I got into data science(-adjacent work) through educational technology and got introduced to educational technology through Open Educational Resources, so embracing the ideas of open science came easily to me. Pretty quickly, though, I found that data ethics and data privacy started to take priority for me—and all this at the same time that I was being introduced to different research paradigms. These days, as much as I am theoretically supportive of the open science movement, I don't feel that it is applicable—or even appropriate—for a lot of the work that I do.

I funnelled a lot of this thinking into this lecture, taking a few paragraphs to talk about research paradigms and to explicitly situate data science as a positivist enterprise before getting into transparency, ethics, and privacy. I wanted to make the argument that you can't understand why transparency is valued in data science without understanding its positivist underpinnings, to follow it up by explaining that those positivist underpinnings are often the **very source** of ethical issues in data science, and to conclude by discussing privacy in data science as existing in tension between those positivist underpinnings and other ethical considerations. 

I'm proud of this first draft, but I'm hoping to revisit it in future semesters—I'd love to get feedback!

# Introduction

This week’s lecture is on transparency, privacy, and ethics, but before we tackle any of those, we need to take a quick detour into the nerdy-but-important world of the philosophy of science. You see, it turns out that not only are transparency, privacy, and ethics all related in the context of data science, but all of those are related to the basic assumptions that data science makes about how the world works. Let's call these assumptions paradigms (as many people do). You could take entire classes on what paradigms are and why they’re important, but I’m going to try to keep this to a few paragraphs, so keep in mind that I’m making some generalizations and skipping some details.

A great way to compare research paradigms is to compare, say, molecular biology (my partner’s major in college) and French (my major in college). A professor of molecular biology (or of any of the other “hard sciences”) assumes that there is a predictable reality behind what they’re studying. That is, organic molecules work in particular, quasi-universal ways, and if you can figure that out, you can introduce established causes to bring about desired effects. This is often called a “positivist” paradigm, with "positivist" having connotations of "rational" and "empirical."

In contrast, a professor of French (or any of the other disciplines in the humanities) assumes that what they’re studying is important, but largely arbitrary. French is decidedly not universal—it’s something that humans made up instead of discovered. Plus, it doesn't apply to most humans and isn't consistent across the humans that it does apply to (for example, French-speaking people in Switzerland count differently than French-speaking people in Canada—they can't even agree on numbers). Thus, while you could try to talk about French in terms of cause and effect, most French professors are more interested in understanding and describing French than in predicting it. This is often called an "interpretivist" paradigm, underlining its focus on trying to understand humans' semi-arbitrary meaning-making.

In between the hard sciences and the humanities, there's a large, important mega-discipline we can call the social sciences, which includes library and information sciences, technology studies, education research, and data science. There's a fair bit of dispute within the social sciences about whether they ought to be modeled after the hard sciences (with a positivist paradigm) or the humanities (with an interpretivist paradigm). That is, when we're studying people and people-related phenomena, can we assume that there are quasi-universal laws that govern and therefore predict human behavior in the same way we can of atoms, chemicals, and molecules? Or, is it safer to assume that people's behavior is context-dependent rather than universal and something to be understood rather than predicted? For the record, I am more of an interpretivist than a positivist—my research is much more interested in describing and understanding phenomena because I'm skeptical about the possibility or value of predicting human behavior. That said, I have a healthy respect for positivism, and I'll be the first to admit that trying to determine cause and effect is more directly "useful" than trying to document contextual variations in human behavior. I prefer the interpretivist paradigm, but the fact is that we need positivist views, too.

At this point in the conversation, it probably won't surprise you to learn that data science is overwhelmingly a positivist enterprise. Determining causes and effects, making predictions, and drawing statistically-sound conclusions that can be acted upon with confidence are at the heart of data science. These are all worthy pursuits—period. I'm making this point, though, because understanding data science's positivist foundations are important for understanding why transparency is important to data science. However, understanding the goals of positivism also helps us draw attention to some of the ethical problems also raised by data science. Then, understanding the tension between 1) transparency and positivism and 2) other ethical values can help us understand how privacy fits into the picture.

# Transparency

Transparency is one of the core values of any positivist approach to science. Even the most committed positivist will acknowledge that even if there are universal laws governing the behavior of atoms, bacteria, humans, or organizations, it can be tremendously difficult to determine what those laws are, especially since a lot of the easy stuff was figured out centuries or decades ago by folks like Newton, Mendel, and Curie.

To identify a cause and effect relationship with a great degree of confidence requires a few things, including access to appropriate data. Appropriate data can cost a lot of money to gather, be difficult to gather, take a lot of time to gather, or all of the above. Modern information and communication technologies make it a lot easier to share data than ever before, but there are still obstacles to actually sharing that data, including the very human belief that "if I put all the effort into gathering this data, I'm not going to give it to others to analyze for free." Nonetheless, governments and research funding agencies are increasingly requiring scientists funded by their grants to share their data as a condition of that funding. In parallel, work is being done to think more comprehensively about how to collect, manage, and share data in appropriate, responsible ways. These open science efforts are based on the beliefs that 1) more science is better science, 2) sharing data allows for more science, and 3) sharing data therefore makes for better science. In general terms, I think this is incontestable logic and that locking down scientific data is morally questionable—however, we'll see later that I think there are major caveats to this.

If sharing data is one part of being transparent, it's not the whole thing. My colleague Josh Rosenberg (whose summarized definition of data science we saw last week) once participated in a study in which

 > independent analysts used the same dataset to test two hypotheses regarding the effects of scientists’ gender and professional status on verbosity during group meetings (Schweinsberg et al., 2021, p. 230)

In other words, in the spirit of transparent, open science, Josh and dozens of other researchers (the list of authors on this article is literally a page long) were all given the same data and encouraged to test the same hypotheses. However, apart from the data and the hypotheses, the organizers of the study were intentionally skimpy on details. For example, it was up to individual researchers to determine how to best measure "professional status" using the available data, what statistical tests to use, etc. As a result,

> Researchers reported radically different analyses and dispersed empirical outcomes, in a number of cases obtaining significant effects in opposite directions for the same research question. (Schweinsberg et al., 2021, p. 230)

In short, even though they were all given the same prompts and the same data, researchers made very different analytical decisions and came to very different results, sometimes producing conflicting (but individually compelling) findings. The article reports that

> Subjective researcher decisions play a critical role in driving the reported empirical results, underscoring the need for open data, systematic robustness checks, and transparency regarding both analytic paths taken and not taken. (Schweinsberg et al., 2021, p. 230)

That is, scientists make lots of decisions when analyzing data, and while open data helps, it's also important for researchers to clearly communicate which decisions they made and why they made them. In theory, any research article is supposed to contain a detailed section of how any analysis was completed, but in practice, word limits and researchers' attention spans are too short for articles to cover every decision that could potentially make a difference.

Thus, open science isn't just about sharing data; it's also about sharing analysis. One of the advantages to using software like R to carry out your analysis is that you have to program the software to carry out the analysis that you want. So, if you are willing to share your data and your code, someone can perfectly recreate every decision you made and every step you took.

Generally speaking, this is still all good stuff. Two major concerns of positivist research communities right now are replication and retractions. Remember that the goal of positivist research is to determine quasi-universal laws that govern and predict phenomena; thus, if one group of scientists gets a certain result when carrying out a study, another group of scientists ought to get the same (or at least a similar) result when replicating that study. In the social sciences—and even parts of the hard sciences—there's often talk of a replication crisis, where a worryingly low number of studies can be replicated the way that people would expect. This challenges the very core of positivist goals for research, but sharing code and data can help someone understand what they're replicating and why they might be having trouble replicating it.

On a similar note, retractions are instances in which a research study is pulled from publication because of concerns about replication, honest mistakes that led to errors in the analysis, or research misconduct that intentionally falsified data or results. Sharing code and data helps with this, too. A friend of mine in grad school worked for a political science journal that required all articles to also submit their data and their code—in addition to the traditional peer review of a research article, he was tasked with reviewing their analysis to make sure that there wasn't any funny business or legitimate mistakes buried in a line of code. I honestly don't know how widespread this practice is, but positivist journals in positivist disciplines ought to be doing more of this work to ensure better science and prevent future retractions.
Ethics

To discuss ethics in data science, I believe it's important to understand its positivist roots. Remember that positivism is about identifying relationships between causes and effects, and using those identified relationships to make predictions and draw statistically-sound conclusions. While the value of transparency has ethical dimensions to it (for example, shouldn't data from publicly-funded research be publicly-available?), I hope it is clear from the last section that in positivist disciplines, transparency's chief value is in supporting the more confident identification and wider application of causal relationships—that is at the core of positivist research. Thus, data science, like any positivist science, is chiefly about identifying cause and effect and using it to predict behavior.

Last week, we discussed some of the context surrounding the development of data science, including the increased computational power and the more abundant data that are made possible by modern information communication technologies. It turns out that the more computational power you have and the more data you have access to, the more you can do to identify and test causal relationships. In many ways, big data and data science are a positivist's dream come true! With so much data available for collecting and so much computational power at our fingertips, humans can (and have) try to predict all sorts of things. However, there's a danger inherent in all of this opportunity. To quote Ian Malcolm, Jeff Goldblum's unforgettable character in the movie Jurassic Park:

![](https://media.giphy.com/media/mCClSS6xbi8us/giphy.gif?cid=ecf05e47c885u7rmgqrscbvyaulsytjbzzepx8s7hgzby9a4&rid=giphy.gif)

> Your scientists were so preoccupied with whether or not they could, they never stopped to think if they should.

Data science is not the exact equivalent of bringing dinosaurs back to life, but the ease of accessing data and computational power and the widespread, often uncritical focus on the positivist value of predicting cause and effect can certainly have unintended consequences. Just because we can predict something with data science, does that mean we should? Furthermore, while the creation of dinosaurs in Jurassic Park is a given (and, of course, a disaster), whether we even can predict as much with data science as we think we can is still up for debate. Let's consider an example; head's up, it's an ugly picture of the way that supposedly-objective data science can be disgustingly racist.

Just this past week, Ryan Mac at the New York Times reported that

> Facebook users who recently watched a video from a British tabloid featuring Black men saw an automated prompt from the social network that asked if they would like to “keep seeing videos about Primates,” causing the company to investigate and disable the artificial intelligence-powered feature that pushed the message.

Later in the article, Mac (2021) continues:

> Google, Amazon and other technology companies have been under scrutiny for years for biases within their artificial intelligence systems, particularly around issues of race. Studies (Links to an external site.) have shown (Links to an external site.) that facial recognition technology is biased against people of color and has more trouble identifying them, leading to incidents where Black people have been discriminated against or arrested because of computer error (Links to an external site.).

> In one example in 2015, Google Photos (Links to an external site.) mistakenly labeled pictures of Black people as “gorillas,” for which Google said it was “genuinely sorry” and would work to fix the issue immediately. More than two years later, Wired (Links to an external site.) found that Google’s solution was to censor the word “gorilla” from searches, while also blocking “chimp,” “chimpanzee” and “monkey.”

Artificial intelligence certainly meets our definition of data science in this class (it's programmed, it uses statistics, and it's applied to a specific discipline), and its appeal is undeniable. If we could use data science to make predictions about what pictures contain which search terms, what themes exist in which videos, or what identity is associated with which face, we could make a lot of predictions, at scale, with very little human effort (though, of course, replacing human employees with cheaper software has its own ethical issues). However, Mac's examples are reminders that artificial intelligence can't make perfect predictions; furthermore, the awfulness of these examples invites the question whether we should even try!

The attractiveness of positivism is understandable and not necessarily bad. Cause and effect relationships are important and worth studying. However, valuing the ability to predict above everything else and trusting big data and data science to make accurate predictions can lead to disaster. Even when predictions are accurate, that doesn't mean the data science behind them is morally sound. For example, Hao (2021) has argued that Facebook has actually become quite good at predicting what kind of content will get a lot of engagement from users. The problem is that conspiracy theories, misinformation, and hate speech are quite good at getting a lot of engagement, and Facebook's commitment to engagement means that its data science wizardry is always going to churn up a lot of that kind of content. Similarly, Tufecki (2018) has wondered whether the same YouTube recommendation engine that helps me find more and more train videos to watch is also feeding more and more radical political content to viewers who start with videos advocating relatively mainstream positions. Those aren't necessarily "wrong" predictions, but they can have dangerous consequences.

Ethics is another field that we could spend a whole semester on, so I can't walk you through all of the ethical considerations that you should make to make sure that you're using data science for good and not (even accidentally) for evil. I do, however, think that this advice from D'Ignazio and Klein (2020) is worth starting with:

> we can begin to examine how power unfolds in and around data. This often means asking uncomfortable questions: who is doing the work of data science (and who is not)? Whose goals are prioritized in data science (and whose are not)? And who benefits from data science (and who is either overlooked or actively harmed)? These questions are uncomfortable because they mask the inconvenient truth that there are groups of people who are disproportionately benefitting from data science, and there are groups of people who are disproportionately harmed. Asking these who questions allows us, as data scientists ourselves, to start to see how privilege is baked into our data practices and our data products. (p. 26).

# Privacy

I'm tackling privacy last because this discussion builds on all of the previous sections of this lecture. To understand privacy as it relates to data science, we need to understand: 1) the core goals of positivist research, 2) how the value of transparency is a natural extension of those goals, and 3) how focusing on the core goals of positivist research at the expense of ethical considerations can lead to disaster. Putting these pieces together, let's consider two ways that data science poses threats to privacy.

First, transparency—a good value with good motivations—poses risks to privacy. Let's imagine that a group of scientists has acquired a large collection of cell phone data. Like other kinds of big data, this collection, combined with some data science magic, has tremendous potential. Salganik (2018) begins his book on data science-adjacent digital social research with a description of a study that used phone data to produce estimates similar to "gold standard... surveys" but "ten times faster and fifty times cheaper" (p. 2). That all sounds like good news.

In this same vein, Hardesty (2013) acknowledges this potential, but starts to get into the issue of privacy pretty quickly:

> The proliferation of sensor-studded cellphones could lead to a wealth of data with socially useful applications — in urban planning (Links to an external site.), epidemiology, operations research and emergency preparedness, among other things. Of course, before being released to researchers, the data would have to be stripped of identifying information. But how hard could it be to protect the identity of one unnamed cellphone user in a data set of hundreds of thousands or even millions?

As Hardesty suggests here, data scientists—and other scientists—are generally attentive to privacy. Anyone here at UK who does "human subjects research" has to demonstrate that they are going to protect the privacy and anonymity of the people who participated in their research, and only the laziest of scientists are going to make no effort to do this whatsoever. The problem, though, is this isn't always as easy as it sounds. For example, I do a lot of Twitter research, and most social media researchers know to at least remove real names and screennames from data before publishing it in papers. The problem, though, is that Twitter has a decent search engine; whenever I read Twitter research with this kind of anonymized tweets, I'll usually crack open a Web browser, search for the quoted text, and see if I can't find out who the "anonymized" participant is. It's usually not that hard. Cell phone data isn't as easy to de-anonymize, but Hardesty (2013) reports that it isn't impossible either:

> According to a paper appearing this week in Scientific Reports (Links to an external site.), harder than you might think. Researchers at MIT and the Université Catholique de Louvain, in Belgium, analyzed data on 1.5 million cellphone users in a small European country over a span of 15 months and found that just four points of reference, with fairly low spatial and temporal resolution, was enough to uniquely identify 95 percent of them.

> In other words, to extract the complete location information for a single person from an “anonymized” data set of more than a million people, all you would need to do is place him or her within a couple of hundred yards of a cellphone transmitter, sometime over the course of an hour, four times in one year. A few Twitter posts would probably provide all the information you needed, if they contained specific information about the person’s whereabouts.

So, transparency is good, but even an anonymized dataset can create privacy risks for people, and it's important to keep that in mind. As much as I love the motivations behind open science, I very rarely share my research data, because I don't want to create any trouble for the Twitter users I'm studying... especially because they rarely realize I'm studying them and might be very uncomfortable if they found out (see Fiesler & Proferes, 2018). This point brings us to a second perspective on privacy and data science.

This perspective focuses on how positivism—an important research perspective with good intentions—can also pose risks to privacy. Recall my comment from earlier that the more data you have available, the more predictions you can make. This creates an obvious incentive to collect as much data as possible to make predictions that are important to you. We've already discussed how those predictions can be ethically questionable, but let's expand that to how the data collection itself can violate expectations of privacy.

In November 2019, two reporters at the Tampa Bay Times (Bedi & McGrory, 2020) reported that:

> The Pasco Sheriff’s Office keeps a secret list of kids it thinks could “fall into a life of crime” based on factors like whether they’ve been abused or gotten a D or an F in school, according to the agency's internal intelligence manual.

> The Sheriff’s Office assembles the list by combining the rosters for most middle and high schools in the county with records so sensitive, they’re protected by state and federal law.

> School district data shows which children are struggling academically, miss too many classes or are sent to the office for discipline. Records from the state Department of Children and Families flag kids who have witnessed household violence or experienced it themselves.

> According to the manual, any one of those factors makes a child more likely to become a criminal.

> Four hundred and twenty kids are on the list, the Sheriff’s Office said.

> The process largely plays out in secret. The Sheriff’s Office doesn’t tell the kids or their parents about the designation. In an interview, schools superintendent Kurt Browning said he was unaware the Sheriff’s Office was using school data to identify kids who might become criminals. So were the principals of two high schools.

There are a lot of concerns associated with this kind of project, which, again, qualifies as data science. Should we predict whether students could "fall into a life of crime"? (There are serious civil liberties concerns.) Are there dangers that certain populations are going to be singled out as future criminals? (Absolutely!) Do the data that the Sheriff's Office is using represent what they think they do? (No, "grades" do not equal "intelligence.")

As difficult as it is to set those questions aside, though, let's ask the question of whether a law enforcement agency ought to have across-the-board access to students' grades and disciplinary records. If we're guided entirely by positivist goals, more data leads to better science, so sure, it's worth it. However, we can't afford to make this kind of decision based entirely on whether it improves our predictive power (though, again, that's not necessarily the case). We also need to consider what rights students' have to privacy and what line we need to draw, even if it means the Sheriff's Office doesn't have as much data to work with.
Conclusion

This lecture has been both a lot and also not nearly enough. It's important that we keep transparency, ethics, and privacy in mind throughout the rest of the semester, and I hope that I've really hammered that point home. At the same time, though, there are so many more things we need to consider to really appreciate what it means to be transparent, determine which ethical frameworks to follow, and make sure we're respecting people's privacy. This is an ongoing journey—the most important part is that everyone come along for the ride.

# References

Bedi, N., & McGrory, K. (2020, November 19). Pasco's sheriff uses grades and abuse histories to label schoolchildren potential criminals. The kids and their parents don't know. *Tampa Bay Times*. https://projects.tampabay.com/projects/2020/investigations/police-pasco-sheriff-targeted/school-data/ (Links to an external site.)

D'Ignazio, C., & Klein, L. F. (2020). *Data feminism*. The MIT Press.

Fiesler, C., & Proferes, N. (2018). "Participant" perceptions of Twitter research ethics. *Social Media + Society*, *4*(1). [https://doi.org/10.1177/2056305118763366](https://doi.org/10.1177/2056305118763366)

Gershgorn, D. (2021, July 15). Black teen barred from skating rink by inaccurate facial recognition. *The Verge*. [https://www.theverge.com/2021/7/15/22578801/black-teen-skating-rink-inaccurate-facial-recognition](https://www.theverge.com/2021/7/15/22578801/black-teen-skating-rink-inaccurate-facial-recognition)

Hao, K. (2021, March 11). How Facebook got addicted to spreading misinformation. *MIT Technology Review*. [https://www.technologyreview.com/2021/03/11/1020600/facebook-responsible-ai-misinformation/](https://www.technologyreview.com/2021/03/11/1020600/facebook-responsible-ai-misinformation/)

Mac, R. (2021, September 3). Facebook apologizes after A.I. puts 'primates' label on video of black men. *The New York Times*. [https://www.nytimes.com/2021/09/03/technology/facebook-ai-race-primates.html](https://www.nytimes.com/2021/09/03/technology/facebook-ai-race-primates.html)

Salganik, M. J. (2018). *Bit by bit: Social research in the digital age*. Princeton University Press.

Schweinsberg, M., Feldman, M., Staub, N., van den Akker, O. R., van Aert, R. C. M., van Assen, M. A. L. M., Liu, Y., Althoff, T., Heer, J., Kale, A., Mohamed, Z., Amireh, H., Prasad, V. V., Bernstein, A., Robinson, E., Snellman, K., Sommer, S. A., Otner, S. M. G., ... Ulhmann, E. L. (2021). Same data, different conclusions: Radical dispersion in empirical results when independent analysts operationalize and test the same hypothesis. *Organizational Behavior and Human Decision Processes*, *165*, 228-249. [https://doi.org/10.1016/j.obhdp.2021.02.003](https://doi.org/10.1016/j.obhdp.2021.02.003)

Tufekci, Z. (2018, March 10). YouTube, the Great Radicalizer [opinion column]. *The New York Times*. [https://www.nytimes.com/2018/03/10/opinion/sunday/youtube-politics-radical.html](https://www.nytimes.com/2018/03/10/opinion/sunday/youtube-politics-radical.html)