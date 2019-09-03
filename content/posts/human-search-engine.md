+++
draft = false
date = 2019-09-03T13:50:00-04:00
title = "Human Search Engine teaching activity"
slug = "human-search-engine" 
tags = ["teaching", "search engines", "ICT 200"]
categories = ["macro"]
+++

In the spirit of [last week's](https://spencergreenhalgh.com/posts/sandwiches-and-arguments/) sharing of teaching activities from one of my online courses, I'd like to share another discussion post activity that I'm both 1) proud of, and 2) desperately in need of feedback on. 

One of my favorite things about teaching ICT courses is that I get to learn some technical details that don't come up in an educational technology curriculum and that haven't come up in my personal efforts to learn more about technology. For example, I didn't really have an understanding of how a search engine worked until I had to teach it to others! I've done a fair amount of web scraping in my research, so it was a treat to find out that the basics of web crawling aren't that far from what I'm able to accomplish as a programmer. That said, I knew that my students probably don't have any experience with web scraping, so I've been looking for another way to get the fundamentals of search engines across to them. This is the second iteration of this activity, but could still use a lot more polish. I'd love feedback, but feel free to also adapt it for your own teaching!

# The Prompt

Two of the readings you've just completed are closely tied to the way that search engines work. As you read, the Deep Web is simply anything that isn't indexed by (and therefore accessible through) search engines. Then, the How Search Engines Work reading obviously had a lot to say about what Google (or DuckDuckGo) looks like "under the hood." While you've probably learned a lot from these readings, they were still kind of abstract and technical, so you might still not feel like you have a solid grasp of how a search engine works. That's where this activity comes in!

For this activity, we are going to replace with human effort the steps that computer programs take in order to build a search engine database and rank results in response to a question. There are two parts to this activity, and you will earn half a point for completing each of them.

## Part 1: Crawling and Indexing (0.5 points)

1. Log in with your UK Google Account (you can find information at the bottom of [this page](https://www.uky.edu/see/linkblue)) and create a new Google Sheet (you can click on [this link](https://sheets.new) to do that directly, so long as you're already logged in). Give your Google Sheet a name and click the "Share" button in the top right corner. This should set it up so that "Anyone at University of Kentucky with the link can view."
2. In cell A1, write "page URL", in cell B1, write "page title", and in cell C1, write "excerpt."
3. Go to en.wikipedia.org. Click on one of the links on the front page and use the page it takes you to as a starting point for your "crawling and indexing."
4. Copy the URL for that page from your browser and paste it in cell A2. Copy the page title and paste it in cell B2. Copy the first paragraph of text and paste it in cell C2.
5. Click on one of the links on this page. Repeat step 4 for this new page (but filling in A3 instead of A2, etc.)

From here on out, you're going to spend **at least 30 minutes** repeating this process of clicking on links to new pages ("crawling") and copying information to your Google Sheet database ("indexing"). This is more or less the same work that a web crawler does, except that an actual "robot" grabs more information&mdash;and does it faster! The point of us doing this by hand is to appreciate all the work that has to go into a search engine behind the scenes for it to be useful for us... and to set up the next part of the activity!

6. After your 30 minutes have elapsed, post a link to your Google Sheet "database" to the discussion forum post below. **Make sure that you've made your Google Sheet accessible by others!!!** Include in your post a few comments on whether and how you think about search engines differently now that you've pretended to be a human one!

## Part 2a: Searching (0.25 points)

For this part of the activity, pick a classmate's discussion post. Before accessing their "database," think of a question or a term that you might enter into a search engine. Post that question or term in a reply to your classmate's post.

## Part 2b: Ranking (0.25 points)

After posting your question or term, you're committed to trying to find a "most relevant" Web page! Make sure that you're logged in with your UK Google account and open up the Google Sheet "database." With your question or term in mind, review all of the pages that are included in the database and pick the top three (in order) most relevant pages for your question or term. (Spoiler alert: They might not be all-that-relevant! You're just going to have to do your best!).

In a second reply to your classmate's post, list the top three "most relevant" pages for your search query. Then, explain how you determined that those were the most relevant. What information did you use to judge relevance? Is there any information you would have liked to have to judge relevance but that wasn't in the database? Conclude with a couple of thoughts on how you see search engines differently now that you've tried doing this "by hand!"