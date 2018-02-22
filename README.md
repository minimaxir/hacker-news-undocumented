# A List of Hacker News's Undocumented Features and Behaviors

[Hacker News](https://news.ycombinator.com), a simple link aggregator owned and operated by Silicon Valley startup incubator [Y Combinator](http://www.ycombinator.com), has had many [positive effects](https://news.ycombinator.com/item?id=16409768) on SV startups and engineers as a whole. On Hacker News, users receive Karma whenever another user upvotes a submission or comment they made, which incentives positive contributions to the community.

However, in maintaining its simplicity, many new features and behaviors added over the years on Hacker News are not fully documented other than the [occasional](https://news.ycombinator.com/item?id=12073675) comments from staff. This list details some of the hidden norms about Hacker News not otherwise covered in the [Guidelines](https://news.ycombinator.com/newsguidelines.html) and the [FAQ](https://news.ycombinator.com/newsfaq.html), along with a few bonus features outside of typical HN usage. If there is anything missing/incorrect from this list, feel free to file a GitHub issue/PR.

*This list has no affiliation with Hacker News, Y Combinator, or any YC-backed company.*

## Undocumented Features

### Moderators

Hacker News currently has two full time moderators: Dan Gackle ([dang](https://news.ycombinator.com/user?id=dang)) and Scott Bell ([sctb](https://news.ycombinator.com/user?id=sctb)). Their [comment](https://news.ycombinator.com/threads?id=dang) [replies](https://news.ycombinator.com/threads?id=sctb) provide a pseudo-log of Hacker News moderation.

Both are very responsive when contacted at [hn@ycombinator.com](mailto:hn@ycombinator.com), and is the best option for resolving any issues on Hacker News.

### Downvoting Comments

All comments start with a score of 1 point (but in order to prevent bandwagoning, the comment score is not visible to users other than the author). After users reach **500 Karma**, they gain the ability to downvote another comment. Downvoted comments (i.e. with a score < 1) reduce their placement on the comment thread and will appear desaturated to other users deemphasize them. There is no upper limit on the score of a comment, but the minimum score is -4 points.

![](/images/hn_downvotes.png)

Complaining about being downvoted is discouraged and usually results in even more downvotes.

If the comment desaturation makes Hacker News difficult to read, you can install the CSS extension [discussed here](https://news.ycombinator.com/item?id=16426569).
  
### Flagging/Vouching

If a user has **30 Karma**, they can flag submissions. Although submissions cannot be downvoted, flags act as a "super" downvote and enough flags will strongly reduce the rank of the submission, or kill it entirely (flagging is *supposed* to be used for submissions which are spam/off-topic, but that isn't always the case in practice). A submission that's flagged to death will have a `[flagged]` tag. Comments behave similarly. 

In contrast, a `[dead]` submission is either killed by a moderator or by the software.

If a user has **30 Karma**, they can also [vouch](https://blog.ycombinator.com/two-hn-announcements/) for a `[flagged]` or `[dead]` submission/comment. A vouched submission/comment has its rank restored, but it can be `[flagged]` again at which point it can't be re-vouched.

### Setting top color
If a user has **250 Karma**, they can set the color of the top bar in their profile settings. The default is #ff6600. Here's the [complete set](https://news.ycombinator.com/topcolors) of colors users have set.

### Duplicate Submissions

Hacker News encourages a single discussion on a given story. All others are marked as a `[dupe]` and will be killed without the ability to vouch. This includes articles which are insubstantial variations of an earlier widely-discussed submission.

### Anti-Voting Manipulation

The FAQ states "users should vote for a story because they personally find it intellectually interesting, not because someone has content to promote." Indeed, Hacker News [utilizes](https://news.ycombinator.com/item?id=7972941) a voting ring detector which will prevent caught submissions from hitting the front page. Due to sites like [Product Hunt](https://www.producthunt.com) normalizing the asking for upvotes or other engagement via social media, the implicit asking of upvotes is also done for Hacker News, usually due to [ignorance](https://twitter.com/minimaxir/status/958397508996055040) of the Hacker News rule against it. There are very few good reasons to draw attention to a Hacker News submission immediately after it has been submitted.

One popular "trick" for obfuscating voting manipulation on Hacker News is to link to the Hacker News's `/newest` page of new submissions (instead of a direct link which would otherwise make voting manipulation obvious), and asking friends to upvote the submission from that page. This trick doesn't actually work.

### Flame-War Detector

The FAQ notes that submission rank is impacted by "[software which downweights overheated discussions](https://news.ycombinator.com/item?id=16020089)." A good rule of thumb for this effect is when the number of comments on a submission exceeds its score. Moderators can overrule the downranking for appropriate, not-actually-a-flame-war discussions.

### Second-Chance Pool

Moderators will sometimes [rescue a post](https://news.ycombinator.com/item?id=11662380) which didn't receive a lot of upvotes and reset the submission time on the post.

Relatedly, moderators can also [invite users](https://news.ycombinator.com/item?id=10308900) via email to resubmit a post which didn't get much traction.

### Edit/Delete Time Limits

After a post or comment is made, it can be edited by the author **within 2 hours**. A post/comment can be deleted by the author within those two hours, **but only if it has no replies**, in order to prevent discussion from being lost. In that case, the post/comment **cannot be deleted** (This can result in a fake `[deleted]` edit if a person wants to remove their comment in the limit but can't).

If you need something deleted but you can't, you'll have to message [hn@ycombinator.com](mailto:hn@ycombinator.com).

### Comment Collapsing

Comments can be collapsed by clicking the `[+]` icon to improve readability.`[flagged]` comments are collapsed by default, and moderators can set a comment to automatically be collapsed if necessary (e.g. meta-discussion).

### Shadowbanning

Both users and domains can be shadowbanned, where all posts/comments by that user / submissions to that domain will be instantly `[dead]` and cannot receive votes/comments (but can still be vouched). A good way to tell if a user/domain is banned is to either have another user with `showdead` enabled check for a series of `[dead]` content from that source, or view those submissions in Private Browsing/Incognito mode to see if they appear.

![](/images/shadowban.png)

Users/domains are usually shadowbanned for breaking HN rules/spam. If you feel you are unfairly shadowbanned, contact [hn@ycombinator.com](mailto:hn@ycombinator.com).

### Green Usernames

Accounts which are less than **2 weeks** old will appear with a green username.

## Behaviors

### Implicit Downranking of Politics

The Guidelines state that political discussion is off-topic. However, as of recently, the line between technology and politics has become *extremely* blurred. Most tech related submissions with a hint of political partisanship will quickly be flagged to death by users (or die a slow death due to the inevitable flame war).

### Implicit Downranking of Race/Gender

Likewise, diversity and inclusion has become a recent, important issue in technology. However, despite discussions about race/gender not being off-topic, they tend to be flagged to death by users regardless. Unfortunately. (Moderators occasionally unkill such threads if they see it in time, although it rarely sticks).

### Paywalls

Many news websites have started implementing a paywall for their content, which has caused conflict with Hacker News's "original source" rule. The `web` button next to submissions (that does a Google search for the given title) was partially intended to serve as a paywall workaround; however, recent changes to the paywall implementations have closed that loophole.

As a result, submissions which link to paywalled sites tend to get many comments complaining about paywalls.

### Perceived Favoritism Toward YC Companies

YC Companies get two notable benefits on Hacker News; they can post jobs ads to the front page (which start of at Rank #6, cannot be voted/commented on, and have a fixed decay rate), and the ability to do a [Launch HN](https://hn.algolia.com/?query=Launch%20HN&sort=byPopularity&prefix=false&page=0&dateRange=all&type=story) when their startup launches out of a YC batch.

Currently, there is no evidence that non-job submissions about a YC startup receive preferential treatment on the front page, or kill submissions critical of a YC startup. In fact, the moderators have stated that they explicitly [avoid killing controversial YC posts](https://news.ycombinator.com/item?id=8258752) when possible.

Additionally, founders of YC companies see each other's usernames [show up in orange,](https://techcrunch.com/2013/05/18/the-evolution-of-hacker-news/) which--although not an explicit benefit--does allow fellow YC founders to immediately identify one another in discussions. 

## Bonus Features

### Hacker News Classic

Hacker News allows people to use the [old front page ranking algorithm](https://news.ycombinator.com/classic). This results in different (and occasionally better) content.

### Hacker News Wayback

Hacker News allows users to see what the front page looks like [at any point in time](https://news.ycombinator.com/front?day=2012-03-24). You can also do a wayback view for any user at their registration date by clicking their registration date in their profile.

### Hacker News on BigQuery

If you want to gather large amount of Hacker News data for data analysis/machine learning, you should use the [Hacker News dataset on BigQuery](https://cloud.google.com/bigquery/public-data/hacker-news), which is updated daily and is much more pragmatic to use than manually scraping data from the Hacker News API.

## To-Do

* Add more images/citations

## Maintainer

Max Woolf ([@minimaxir](http://minimaxir.com), [minimaxir](https://news.ycombinator.com/user?id=minimaxir) on Hacker News since 2012)

*Max has no affiliation with Hacker News, Y Combinator, or any YC-backed company.*
