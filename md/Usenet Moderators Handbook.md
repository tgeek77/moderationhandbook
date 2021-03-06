# Usenet Moderator's Handbook
## Table of Contents

1. Introduction
2. What does 'moderated' mean
3. Why do Usenet moderated newsgroups exist
4. Role of a moderator
5. How the moderation process works technically
 1. Mailpath usage
 2. Standard News Header Usage
    1. Approved: Line
    2. Date: Line
    3. Distribution: Line
    4. Expires: Line
    5. Followup-To: Line
    6. From: Line
    7. Keywords: Line
    8. Newsgroups: Line
    9. Path: Line
    10. References: Line
    11. Reply-To: Line
    12. Subject: Line
    13. Other Informational headers
  3. Other headers that should be removed before posting
  4. Signatures
  5. Creating newsgroup specific headers
  6. Receiving submissions
    1. Articles posted to a moderated group
    2. Emailed submissions
  7. Adding moderator comments
  8. Submitting articles
  9. Canceling articles
  10. Where to find other documentation on moderation
6. What are the different types of moderated groups
  1. Announce groups
  2. Binary groups
  3. Digests
  4. Discussion groups
  5. Source groups
7. Setting up a new moderated group
  1. Submission aliases
  2. Email submission servers
8. Choosing a moderation policy
  1. Article rejections
  2. Copyrights
  3. Dealing with forged Approved: headers
  4. Commercial postings
  5. Dealing with cross-posted articles
9. Backup moderators
10. Multiple or Team Moderation
  1. Team moderator mailing lists
  2. Facilitators
  3. Rejection Notices
  4. Multiple moderator conflict resolution
11. Handling temporary moderator absences
12. Gatewaying newsgroups to mailing lists
  1. Newsgate
  2. Listserv
13. Creating Periodic Informational Postings
  1. Copyright
  2. Frequency of distribution and news.answers
14. Archiving postings to the group
  1. FTP Archives
  2. Email Archives
  3. Archives of selected articles
15. Tools for moderators
16. News transport gotcha's
  1. Line lengths
  2. Old C News blanks-in-ng bug
  3. B News non-local unapproved articles bug
  4. Article size concerns
  5. Amount of messages posted daily
  6. Cross-posting to other moderated groups
  7. Extra headers on directly posted articles
  8. Multiple copies of the same submission received
  9. B News static Newsgroup: header limit
17. How to deal with your readership
  1. Personality of your group
  2. Deciding a course of action
  3. Commonly perceived problems with moderation
  4. Vocal minority
  5. Anonymous postings
18. Answers to general questions
  1. How big is my group's readership?
  2. What mechanisms guard the group from unauthorized "Approved:" headers?
  3. Have any moderators gotten paid for what they do?
  4. Why are readers complaining of lost articles?
  5. Readers complain of articles being deleted after a day
19. Passing the torch
20. Acknowledgments
21. Security Considerations
22. References
23. Author's Address

Appendices
1. Usenet Specific Newsgroup Moderation Information
2. Discussion lists for Usenet moderators
  1. moderators-advice
  2. moderators
  3. Changing moderators
  4. Usenet moderator replacement concerns
  5. Group Charters
  6. Submitting articles through public Usenet Mail/News gateways
  7. Usenet Moderated Newsgroup Archive List
3. Canned Messages
  1. C News Duplicate headers message template
  2. Thanks for FAQ comments
  3. Inappropriate submission
  4. Get a Clue
  5. Test elsewhere
4. Tributes

## 1. Introduction

The purpose of this document is to assist new and existing moderators in understanding what is involved in moderating a newsgroup. This document contains information about how the moderation process works, how to get started, where to get existing moderation posting software, what NetNews related problems moderators may encounter, and where to get additional
help if needed.

In the past, most moderators learned on-the-job, and there was not much documentation available about what was expected of a moderator. This document attempts to aid new moderators in understanding what it is that
they have gotten themselves into. This document will also be useful to those wishing to volunteer to be a moderator.

Within this document, Usenet refers to the traditional core hierarchies of comp, misc, news, rec, sci, soc and talk. The term 'Network News' (or 'NetNews') refers to all hierarchies that use the same transport and reader mechanisms that the traditional core hierarchies do.

Moderation of newsgroups is transcending the traditional core Usenet news hierarchies as many organizations are using NetNews software for internal use. Also, many non-core hierarchies, such as alt, biz, bionet, etc., contain moderated newsgroups.

It is the intent of the author that this document also be of use to those who are not Usenet moderators but are moderating NetNews newsgroups nevertheless.

It is expected that readers of this document are already familiar with NetNews, at least from a user's perspective, and have been exposed to network tools such as FTP. A complete explanation of NetNews jargon and culture is beyond the scope of this document.

## 2. What does 'moderated' mean ?

'Moderated' means that all postings to the newsgroup go to a mail address (e.g., news.group@example.com) instead of appearing in the newsgroup directly. The postings are then forwarded via email to a moderator, or group of moderators, or even an automated program, who decides whether to actually inject the article into the newsgroup or to reject it as not meeting guidelines spelled out in the group's charter.

The main purpose of newsgroup moderation is to prevent inappropriate posts to the newsgroup. For example, moderation can prevent discussion or requests for software from appearing in groups dedicated to posting source code. It can also be used to facilitate discussions, to create a forum for announcements, to prevent repeated posts of the same information, or to cut off endless uninformative arguments. Some groups, e.g., rec.humor.funny and some source groups, also use it to control the traffic volume.

Moderation should not be used to censor unpopular viewpoints, or those that the moderator simply disagrees with. It is best to have a very clear charter and moderation policy for the newsgroup, so that newsgroup readers and posters can tell which topics are, or are not, appropriate for discussion on the newsgroup.

## 3. Why do Usenet moderated newsgroups exist ?

Groups on the net are moderated for a variety of reasons. All moderation serves the same basic purpose, to filter out inappropriate postings and to deliver timely, on-topic articles. Most moderated groups fall into one of five general categories:

1. Groups with postings of an informative nature not suited to discussion and always originating from the same (very small) group of posters. Groups within this category include news.lists, news.announce.newusers and comp.mail.maps.

2. Groups derived from regular groups with such a high volume that it is hard for the average reader to keep up. The moderated versions of these groups are an attempt to provide a lower volume and higher quality version of the same forum. An example of this category is news.announce.newgroups (a reduced form of news.groups).

3. Groups derived from regular groups that have often been abused. That is, the regular groups often received postings of items that were not germane to the stated topic of the group (or sometimes even within the realm of politeness for the net). This also includes groups suffering from an annoying number of duplicate postings and inappropriate followups. Moderated groups in this category include comp.sources.misc.

4. Groups designed to serve as direct feedback to an off-the-net group. The discussion in comp.std.mumps is an example of this.

5. Groups that are gatewayed into Usenet from an Internet mailing list. These groups are moderated by someone on the Internet side but are shared with the Usenet population. Submissions mailed to the proper addresses, given below, will appear in both the group on Usenet, and the Internet list. This includes some groups in the "inet" distribution such as comp.ai.vision.

##  4. Role of a moderator

Moderating a newsgroup is a volunteer effort but it carries certain responsibilities. The role of a moderator is to review, approve and post articles relevant to a newsgroup according to the group's charter or guidelines.

If an article does not qualify for posting, it is to be sent back to the author with an explanation of why it is not suitable for posting.

Depending on the nature of the group, acceptable turnaround time can range from a few days to a few weeks. If posts accepted for the group have a long delay before being actually posted, as happens with moderated net magazines, it is a good idea to let the submitter know that the post was accepted, and what the approximate posting date will be.

## 5. How the moderation process works technically

This section contains technical information about the news mechanisms of concern to newsgroup moderators, including standard news headers,
dealing with submissions, and generating special purpose headers to
better serve your newsgroup.

A moderated newsgroup is marked as such in the news transport software
(most often with a trailing "m" flag in the active file of news systems). What this means is that articles must be approved before they are accepted in the group. When an article is posted to a moderated group, the news transport software will mail the article to the moderator See Mailpath Usage for approval and actual injection into the news system.

Once the moderator has received a submitted article in the incoming
mailbox, (and if necessary has edited the article's content) the
moderator needs to process the article's headers a bit before actually
posting it to the group. The descriptions below explain usage of the
various headers.

Technically, all that the moderator has to do is add an "Approved"
header, and repost the article. The only thing that differentiates an
"approved" from a "non-approved" posting is the existence of the
"Approved:" header. The news transport will then accept it and
transfer it to other machines.

New moderators, especially those not familiar with news mechanisms, may
need to refer back to the list of standard news headers ([Section
5.2](#5.2)) often as they familiarize themselves with the moderation
process.



### 5.1. Mailpath usage

When a net.citizen posts a message to a moderated newsgroup, the news
software looks up the moderator's submission address. The software then
mails the unapproved article to the moderator for approval and injection
into the news system.

To make this work the mailpaths file is used on B News or C News
systems. INN uses the moderators file and the inn.conf file to provide
the same functionality.

The list of moderator addresses can change almost daily and trying to
keep up with it can be a job in itself at times. For that reason the
mailpaths file can be configured to send all unapproved submissions to
moderated newsgroups to a site which has volunteered and been approved
as a mail forwarder for Usenet moderators. In almost all cases it is
best to configure news software to forward unapproved articles to one of
the established mailpath forwarders.

David Lawrence
[<tale@isc.org.net>](https://web.archive.org/web/20071021065323/mailto:tale@isc.org.net);
maintains the periodic posting

**["How to Construct the Mailpaths
File"](/web/20071021065323/http://www.landfield.com/faqs/mailpaths/part1/)**

It describes the syntax of the contents of the file and how to construct
it for your B News or C News system. It also lists the sites that are
maintaining a current listing of moderator addresses and are acting as
mail forwarders for the Usenet moderator infrastructure.

The article is periodically posted to the newsgroups
[news.lists](https://web.archive.org/web/20071021065323/news:news.lists),
[news.admin.misc](https://web.archive.org/web/20071021065323/news:news.admin.misc)
and
[news.answers](https://web.archive.org/web/20071021065323/news:news.answers).



### 5.2. Standard News Header Usage

Articles posted to moderated newsgroups, like all other news articles,
must conform to the article specifications of the Usenet news system, as
described in RFC 1036[1]. The list below explains the standard news
headers as they pertain to moderating Usenet newsgroups, though if there
is any doubt about the specifications of a particular header RFC 1036
should be consulted. [[See Section 5.10](#5.10) for more information on
obtaining [RFC
1036](/web/20071021065323/http://www.landfield.com/rfcs/rfc1036.html)
and other NetNews related RFCs and documents.]

There is no preferred order of headers. Compliant software should accept
the articles with the following headers in any order.



#### 5.2.1. Approved: Line

Any article posted to a moderated newsgroup must contain an Approved:
line. Always sign the approved line with your electronic address. The
software won't care what is here, but in case something goes wrong, the
community will know who approved the article.

Some moderators sign the Approved: line with the moderator's submission
address, so that any comments-to-the-moderator tend to get routed into
the moderation mailbox.

A sample Approved: line:

**Approved: kent@landfield.com (comp.sources.misc)**

If an article has been approved by the moderators of different moderated
groups, the moderator with final approval should try to put the other
moderators on the Approved: line as a way of documenting that it was
approved to appear in multiple groups.

A sample Approved: line marking approval in more than one group:

**Approved: kent@landfield.com, tale@isc.org**

While showing multiple approvals is not required, it is informative to
the readership and common courtesy to the other moderator(s) to do so.

**NOTE: Beware of approving cross-posted articles. Refer to "Section
5.2.8 Newsgroups: Line", "Section 8.5 Dealing with cross-posted
articles" and "Section 15.6. Cross-posting to other moderated groups"
for a discussion of the problems.**



#### [5.2.2. Date: Line](#5.2.2top){#5.2.2}

Strip the Date: header from submitted articles, or change it into
something like X-Original-Date:. Do not include an X-Original-Date:
header without a good reason. For example, an article might refer to
"today's New York Times", or might mention software "uploaded to an
FTP site today. Proving your timeliness isn't a good reason unless, for
some reason, it has been in question.

The problem with keeping the original Date: header is that it might
badly confuse the news posting software, or some latency could cause the
article to be unnecessarily rejected at sites, especially when the date
was completely wrong.



#### [5.2.3. Distribution: Line](#5.2.3top){#5.2.3}

The Distribution: header should be stripped from any submitted article.
You should try not to post things of a definite local nature to
world-wide groups with the current state of network news propagation.

Unfortunately, using the Distribution: header rarely produces the
intended or desired results. An article posted with a restrictive
Distribution: header is almost certain to be propagated far beyond the
intended area, and will be equally likely to miss some sites that would
be interested in that region's news, and might even be physically
located in the intended target zone.

In addition, many articles are posted with "na" (North America) or
"usa" (U.S.A.) distributions because of poorly-thought-out software
defaults, rather than any conscious decision by the poster. Many
non-North-American readers are annoyed by this needless limitation on
what news reaches them.

In theory distributions work as intended, but in practice, due to lack
of verification by posting agents, misconfigured news transport agents,
wide-area sites which pick up all news regardless of distribution, and
inadequate controls on the names of the distributions, they are
relatively useless.



#### [5.2.4. Expires: Line](#5.2.4top){#5.2.4}

Moderators should consider adding an Expires: header if the information
being posted has a limited period of usefulness. For example, a Call For
Papers (CFP) posted to the group
[news.announce.conferences](https://web.archive.org/web/20071021065323/news:news.announce.conferences)
might be valid only until a certain date. The Expires: header can then
be set to expire the article the day after the deadline specified in the
CFP.

Many sites with limited news retention times keep articles with explicit
Expires: headers online longer than the default time period, so an
Expires: header can help keep periodically posted information readily
available to readers at all times.

Your use of the Expires: line should be documented in your group's
periodic policy posting.



#### [5.2.5. Followup-To: Line](#5.2.5top){#5.2.5}

If you have a policy of directing all followups to the article
submitter, or if the submitter requests it, use the header line

**Followup-To: poster**

The news reader software will then email followups to the address listed
in the Reply-To:, and if non-existent, to the From: address.

In some cases it might be appropriate to place the name of an
unmoderated discussion group in this header.

For example:
[Comp.sys.amiga.announce](https://web.archive.org/web/20071021065323/file://comp.sys.amiga.announce/)
does not carry any discussions. Articles there contain the line

**Followup-To: comp.sys.amiga.misc**

With this header, when a reader with compliant news software tries to
followup to an article appearing in the group, their article is actually
redirected to the unmoderated discussion group
[comp.sys.amiga.misc](https://web.archive.org/web/20071021065323/news:comp.sys.amiga.misc).

The appropriate use and content of this header are very dependent on the
community of readers that the newsgroup is serving.

**NOTE: It is never correct to put an actual email address in the
Followup-To: line.**



#### [5.2.6. From: Line](#5.2.6top){#5.2.6}

Postings to newsgroups should have a From: line that refers to the
submitter, unless the posting is a digest, in which case the From: line
should be that of the compiler of the digest.

Since most news readers display From: line information, it is
appropriate to accurately depict who the article's content is "From",
when possible.



#### [5.2.7. Keywords: Line](#5.2.7top){#5.2.7}

Keywords: lines should be included as received in the posted article.
Some moderators may want to add a Keywords: line if it doesn't already
exist. Some moderators have added "SPOILERS" to the Keywords: line in
articles posted to movie or book discussion groups if the article gives
away the ending.

Some moderators have a list of all of the keywords used in the group and
adjust the Keywords: line as needed. Limiting the set of keywords makes
keyword searching a lot easier and avoids problems with synonyms and
variant spellings.

Keywords: should augment rather than replace keyword usage on the
Subject: line because, unfortunately, some news reader programs cannot
use Keywords: to auto-select articles.



#### [5.2.8. Newsgroups: Line](#5.2.8top){#5.2.8}

If the moderator receives a request to cross-post an article to multiple
groups, and the moderator has a policy of honoring cross- posting
requests, the moderator should try to comply with the poster's
specification if the other groups make sense and are not moderated.

If the submitter requests cross-posting to newsgroups that the moderator
cannot post to, the submitter should be so notified, unless there is a
clear policy statement covering this inability. For example, users at
many sites cannot post or cross-post articles to any alt groups.

If one or more of the other requested groups are moderated, the
moderator can either inform the submitter that the article is being
cross-posted to only unmoderated newsgroups or coordinate with the
moderator(s) of the other group(s). Leave the final decision of what is
relevant on other newsgroups with moderators for those newsgroups.

Due to the nature of existing news software, an article cross-posted by
a moderator to multiple moderated newsgroups appears in all the
specified moderated groups without requiring the further approval of the
other moderator(s). A posting of this type will probably surprise and
may even anger the other moderator(s) if the article posted violates the
charter of the other moderated newsgroup(s).



#### [5.2.9. Path: Line](#5.2.9top){#5.2.9}

The original Path: line should be removed and the news system should be
allowed to generate a new one. The purpose of the Path: line is to show
the path that the article took since being injected into the news
system. Since the moderator is the one that actually injects an article
into the news system, any previous Path: line should be discarded before
the moderator posts the article.

Also insure your news transport software generates a non-replyable Path:
line. For example:

**Path: host!not-for-mail**

This allows it to be propagated back to the site it came from. It also
assures that mail from seriously broken news sites is not returned to
you.

New moderators shouldn't need to worry about this. If there is not a
Path: line in an article, most news transport software generate one
similar to that shown above.



#### [5.2.10. References: Line](#5.2.10top){#5.2.10}

The References: header is used by some threaded newsreaders to chain a
set of articles together. It allows a discussion thread or multi- part
posting to be dealt with as a unit. The second and and subsequent
articles in a set should include a References: header.

News reader software needs to be able to reconstruct the article tree
even if (a) the root article is missing, such as the article has
expired, (b) the immediate predecessor is missing as in a canceled
article. The software must do this based solely on information from the
References: headers of existing articles.

The References: headers are used in different ways today depending on
the article flow in the moderated group. If articles are posted so that
all linked articles are posted in sequence and within a short period,
such as is done in sources groups, then References: headers can be
constructed with a minimalist method. Otherwise, groups where referenced
articles are not in sequence or are posted days apart should use the
standard References: header usage.

The standard and recommended usage of the References: headers is to
include the Message-ID of both the first and one to three immediately
prior article(s), in chronological order. The reason for this strategy
is to keep news reader programs with thread-specific kill files happy
after some articles have expired.

With the minimalist method used by source or binary moderated
newsgroups, the References: header contains the Message-ID of the first
part of the series (or package). The References: header only lists the
Message-ID of the first part posted and not all the intermediate parts.

By using this header, threaded news readers present each set of postings
as a single item to the user making it much easier for them to read.

**NOTE: Another way of linking articles is to list the Message-ID of
every part. This is not recommended as it just increases the size of the
articles without adding much additional information or utility.**



#### [5.2.11. Reply-To: Line](#5.2.11top){#5.2.11}

The Reply-To: line should be preserved if it existed in the submission.
This allows the news reader software to email replies back to the
article's submitter at their preferred address.



#### [5.2.12. Subject: Line](#5.2.12top){#5.2.12}

Standardizing your use of the Subject: line somewhat can really help
readers choose which articles to read and construct accurate kill files.
A leading or trailing keyword system can help immensely, for example.
Moderators of source and binary newsgroups use the Subject: line in a
de-facto way to make it easier for the readership to see what an article
is. For example:

The leading volume-issue and the trailing Part number information are
helpful in giving the readership quick clues to an article.

Assure that your use of the Subject: line is documented in the
newgroup's policy posting so that the readership knows it is occurring
and can take advantage of it.



#### [5.2.13. Other Informational headers](#5.2.13top){#5.2.13}

There are additional headers that a submitter may supply from time to
time. Informational headers such as Summary: and Organization: lines
should be included as received in the posted article.



### [5.3. Other headers that should be removed before posting](#5.3top){#5.3}

Submitted articles may arrive in your mailbox with one or more headers
that should be removed before posting. Automated scripts can do this for
you, or, for a low-volume group, you might prefer to remove them by
hand, or write your own pre-processing tools.



### [5.4. Signatures](#5.4top){#5.4}

Some moderators allow all postings to go out with the original signature
block as received. Others trim excessive signature blocks off, or remove
all but a few lines. In other cases, the moderator will append a
standard newsgroup signature to the bottom of the posting, typically
containing a line or two describing how to submit articles to the
newsgroup, how to retrieve the FAQ, or other highly condensed
information.

Moderators need to be aware that news software may be appending the
moderator's own personal signature file to the end of postings. This
may not be desired and can cause confusion with the original
submitter's signature. The moderator should decide what is the most
appropriate way to deal with their personal signature.



### [5.5. Creating newsgroup specific headers](#5.5top){#5.5}

A moderator may find that their newsgroup is better served with the
addition of non-standard informational header lines to the individual
postings. This can be done with user-definable "X-" headers placed in
the [RFC
1036](/web/20071021065323/http://www.landfield.com/rfcs/rfc1036.html)
header portion of the article or by creating auxiliary headers as the
[comp.sources](https://web.archive.org/web/20071021065323/news:comp.sources).*
groups have done.

Source newsgroup moderators have established additional headers whose
sole purpose is to support the posting of source code, automatic
archiving and index creation.

Auxiliary headers do not appear in the [RFC
1036](/web/20071021065323/http://www.landfield.com/rfcs/rfc1036.html)
"News" header section of an article. Instead they are the first lines
of the article text separated from the news headers by a single line
containing a newline. The actual article text is then separated from the
auxiliary headers by another single line containing a newline.

In either case, the moderator should inform the newsgroup of the purpose
and use of the new headers. This should be done in the periodic policy
posting.



### [5.6. Receiving submissions](#5.6top){#5.6}

Submissions are received by the moderator as mail. Although it is
possible to use a personal mailbox, it is not advisable. The moderator
mailbox should be either a separate account or an alias that points to
the moderator's personal account. There are various reasons for doing
this, among them:

-   Filtering on the To: line to separate submissions from other mail.
-   Ease of maintenance when the moderator moves or is replaced.
-   Most important, if it's the same mailbox is very hard to tell
    what's a submission from what's personal mail.
-   [Others, I am sure]

Submissions to a moderated group should be automatically acknowledged
when received. This can be accomplished using the deliver or procmail
mail processing packages. The UCB Vacation program can also be used to
generate acknowledgements.

Deliver is available from
[comp.sources.reviewed](https://web.archive.org/web/20071021065323/news:comp.sources.reviewed)
archives in volume1. Procmail is available from
[comp.sources.misc](https://web.archive.org/web/20071021065323/news:comp.sources.misc)
archives in volume43. Other mail filtering programs may be used as such
as 'mh' and the 'filter' program that comes as part of Elm.

There are procmail auto-reply tools in the [moderators'
archive](/web/20071021065323/http://www.landfield.com/moderators/).
[See [Section
15](/web/20071021065323/http://www.landfield.com/usenet/moderators/handbook/mod15.html)
for the location of the archive.]



#### [5.6.1. Articles posted to a moderated group](#5.6.1top){#5.6.1}

There are a couple ways that a reader can submit an article to be posted
to a moderated newsgroup. The reader can post the article to the
moderated newsgroup as if the group was not moderated. If the news
software is properly configured then it will forward the article to the
appropriate moderator for approval. Unfortunately, it is not unusual for
a posting to be lost in a misconfigured news system. Readers then send
mail to the moderator wondering where their article went to. The
moderator has not seen it and has no idea what the submitter is talking
about.

Other problems with encouraging direct posting to newsgroups is that the
article might be cross-posted or might have been sent without knowing
the group's moderation status. Another problem that makes directly
posted articles harder to deal with is the duplicate headers problem
described in [Section
16.7](/web/20071021065323/http://www.landfield.com/usenet/moderators/handbook/mod16.html#16.7).



#### [5.6.2. Emailed submissions](#5.6.2top){#5.6.2}

Moderators should consider encouraging submitters to mail articles to
the submission address directly instead of direct postings to the group.
The benefits are, users are usually alerted to mail problems faster than
news problems, duplicate headers are not a problem and articles received
via email are guaranteed not to be cross-posted. All in all, emailed
submissions tend to cause moderators less grief then do directly posted
submissions.



### [5.7. Adding moderator comments](#5.7top){#5.7}

Comments from the moderator, if necessary, should be added in a way that
clearly differentiates the comments from the submitted article. This is
usually done by including comments enclosed in brackets **[ such as
this ]**. Whether the comments are included at the beginning or
appended to the end of the article does not really matter. It has been
suggested that placing the comments at the end of a posting is better
since it does not interrupt the flow of the author's train of thought.

It is also sometimes appropriate to interject comments into the middle
of a posted article; for example, if a post gives a vague reference to
an FTP site, the moderator may wish to add a line with a specific
reference immediately below that paragraph to avoid confusion.

Also moderators should sign the comments, either with their name or some
way to identify the moderator (e.g., *-mod, -editor* or the moderator's
initials).

No matter what method is chosen, the moderator should be consistent so
that the group's readership can easily locate and recognize the
moderator's comments.



### [5.8. Submitting articles](#5.8top){#5.8}

The software and process a moderator uses to post to a newsgroup can be
as simple as piping an article through a script from within the
moderator's mailer which posts it. It can be as full blown as a program
that creates Auxiliary headers for a source submission and checks for
all sorts of potential name conflict problems and common posting errors.

The moderator should determine what is needed to make these tasks
easier. Taking the time to try to figure out actual posting procedures
can potentially save time every day.

Posting software is available on the [moderator tools
archive](/web/20071021065323/http://www.landfield.com/moderators/). From
the simplest "submit" script to the complication of "postit", the
archive has a wide range of posting tools that are there for others to
grab and modify for their purposes. [See [Section
15](/web/20071021065323/http://www.landfield.com/usenet/moderators/handbook/mod15.html)
for the location of the archive.]



### [5.9. Canceling articles](#5.9top){#5.9}

From time to time you may need to cancel an article. It may be that you
need to cancel an article with forged approval or an article that was
posted in error. Whatever the reason, know how to cancel an article so
that when the need arises you are prepared to cancel it quickly and
correctly. To cancel an article, create a cancel message and post it the
very same way the article was originally posted. The From: and Sender:
headers need to be the same as they were in the original article. Take
the Message-ID: of the article being canceled and make it the cancel
header by "Control: cancel <message-id>".

You should use the same Newsgroups: line as the original, and you must
have an Approved: line, otherwise it'll get submitted to the moderator
for approval.

You might choose to make the Subject: contents the same, but it is not
necessary. Finally, if you provide your own Message-IDs for your
articles make sure that you give the cancel message a new Message-ID.
For example, to cancel this message:

Post this cancel message:

Also put a note in the body of the cancellation message explaining why
you cancelled the article. This is normally just a one-line comment.

There are scripts in the [moderator tools
archive](/web/20071021065323/http://www.landfield.com/moderators/) to
assist in canceling articles.



### [5.10. Where to find other documentation on moderation](#5.10top){#5.10}

News programs communicate with each other according to standard
protocols, some of which are described by RFCs. RFC stands for Request
For Comment, but for many of the RFC's it might be better described as
Requirements For Compliance. Many of the RFCs describe de-facto
standards in the Internet Community. They are a form of a published
software standard. Copies of RFCs are often posted to the net in the
group
[comp.doc](https://web.archive.org/web/20071021065323/news:comp.doc) and
obtainable from archive sites such as ds.internic.net.

Current news-related RFCs include the following:

-   [RFC
    1036](/web/20071021065323/http://www.landfield.com/rfcs/rfc1036.html)
    [[[1]](/web/20071021065323/http://www.landfield.com/usenet/moderators/handbook/mod22.html)]{.small}
    specifies the format of Usenet articles.
-   [RFC
    2822](/web/20071021065323/http://www.landfield.com/rfcs/rfc2822.html)
    [[[2]](/web/20071021065323/http://www.landfield.com/usenet/moderators/handbook/mod22.html)]{.small}
    specifies the format of mail messages; RFC 1036 uses this. This RFC
    obsoletes RFC 822.
-   [RFC
    977](/web/20071021065323/http://www.landfield.com/rfcs/rfc977.html)
    [[[3]](/web/20071021065323/http://www.landfield.com/usenet/moderators/handbook/mod22.html)]{.small}
    specifies NNTP, the Network News Transfer Protocol.
-   [RFC
    1123](/web/20071021065323/http://www.landfield.com/rfcs/rfc1123.html)
    [[[4]](/web/20071021065323/http://www.landfield.com/usenet/moderators/handbook/mod22.html)]{.small}
    amends RFC 822.
-   [RFC
    1153](/web/20071021065323/http://www.landfield.com/rfcs/rfc1153.html)
    [[[5]](/web/20071021065323/http://www.landfield.com/usenet/moderators/handbook/mod22.html)]{.small}
    specifies the digest format some groups use.
-   [RFC
    2980](/web/20071021065323/http://www.landfield.com/rfcs/rfc2980.html)
    [[[6]](/web/20071021065323/http://www.landfield.com/usenet/moderators/handbook/mod22.html)]{.small}
    Common NNTP Extensions, Specified extensions to RFC 977.

Henry Spencer has a draft of a successor to RFC 1036 that attempts to
document and explain all subsequent enhancements and existing practice
as implemented in the newer news systems. This draft (often called
son-of-1036) can be obtained by anonymous ftp from ftp.zoo.toronto.edu.
Son-of-1036 is intended to be stand-alone reading and does not require
that one also read RFCs 2822 or 1123.

The IETF's Usenet Article Standard Update Working Group (usefor) is
actively working to create an official update to RFC 1036. More
information on the working group, as well as the group's archives are
located at
[http://www.landfield.com/usefor/](https://web.archive.org/web/20071021065323/http://www.landfield.com/usefor/).

Kent Landfield is currently developing an FYI describing Sources group
moderation.

Chris Lewis maintains an FAQ that suggests a format for an FAQ.

[FAQs: A Suggested Minimal Digest
Format"](/web/20071021065323/http://www.landfield.com/faqs/faqs/minimal-digest-format/preamble.html)

It is periodically posted to
[news.admin.misc](https://web.archive.org/web/20071021065323/news:news.admin.misc)
and to the groups
[news.software.readers](https://web.archive.org/web/20071021065323/news:news.software.readers)
and *.answers.

It is also probably a wise thing to re-read the documents that are
posted from time to time in
[news.announce.newusers](https://web.archive.org/web/20071021065323/news:news.announce.newusers)
so that you are aware of what the rest of the community is seeing. It
may have been a long time since you last read those articles and they
have changed over the years.

For additional background information on Usenet and moderation checkout

[http://www.faqs.org/usenet/](https://web.archive.org/web/20071021065323/http://www.faqs.org/usenet/)

and

[http://www.faqs.org/](https://web.archive.org/web/20071021065323/http://www.faqs.org/)

## [6. What are the different types of moderated groups ?](#6TOC){#6}

Moderated groups come in many forms. A brief description of the major
types follows.



### [6.1. Announce groups](#6TOC){#6.1}

Announce groups are generally specified as low-volume newsgroups that
all readers interested in a specific topic may subscribe to. Some
announce groups serve as a collecting point for
[FAQs](/web/20071021065229/http://www.landfield.com/faqs/) and
announcements for a set of related newsgroups, such as
[rec.music.info](https://web.archive.org/web/20071021065229/news:rec.music.info).
Most announce groups are chartered for fast turnaround time, which in
turn implies only light editing of content;
[comp.newprod](https://web.archive.org/web/20071021065229/news:comp.newprod)
is a rare exception. Moderators of announce groups should make the
charter as specific as possible, and should keep the focus on the value
to the readers rather than the posters.



### [6.2. Binary groups](#6TOC){#6.2}

Binary groups exist to distribute software. [See also Source groups,
[Section 6.5](#6.5)] Binary groups distribute executable binaries or
other non-human-readable material, usually for one particular system
type. Normally binaries are distributed only for systems where many
users do not have development or compilation facilities, such as
personal computers of various types.

Moderators of binary groups should take particular care to prevent the
distribution of software containing viruses. Because UNIX executables
tend to rely on the site-specific configuration, they should never be
posted to the net.



### [6.3. Digests](#6TOC){#6.3}

In preparing a digest, the moderator packs all accepted articles into
one file, and posts it to the newsgroup. Articles are edited to remove
unuseful mail headers, excessive signatures, and other noise. A summary,
table of contents, or other index information is added to the top of the
digest to assist readers in finding pertinent information. Depending on
the nature or volume of the group, digests may be sent out once a day,
or whenever a certain volume of messages has accumulated. Special-topic
digests may also be put out when one topic generates a large number of
messages.

The return address on a digest is the posting address for the group;
unless specified otherwise, all replies to the digest are considered
submissions. Digest format makes it difficult for readers to mail
replies to the authors of individual submissions, and defeats threaded
news readers; it is discouraged for these reasons. It is easy to send
news as separate items to the newsgroup while sending digests to mail
subscribers, as the Telecom digest does.

[RFC
1153](/web/20071021065229/http://www.landfield.com/rfcs/rfc1153.html)
specifies the digest format used by some moderated groups. [See the
group
[comp.risks](https://web.archive.org/web/20071021065229/news:comp.risks)
for an example.] The "MH" mail package also supports building message
digests.



### [6.4. Discussion groups](#6TOC){#6.4}

Discussion groups are usually moderated to quell overheated arguments or
to eliminate certain types of repetitive discussions. Moderation also
removes thoroughly inappropriate posts, such as chain letters, blanket
cross-posts, and topics specifically excluded from the group's charter.

Discussion groups are frequently used for questions, and moderators may
want to prepare a Frequently Asked Questions (FAQ) posting for the
group, or to delegate another knowledgeable poster to do so. Moderators
of discussion groups should also be prepared to answer common questions
offline, perhaps by forwarding the relevant section(s) of the FAQ."



### [6.5. Source groups](#6TOC){#6.5}

Source newsgroups are moderated newsgroups whose sole purpose is for the
distribution and archiving of source code. These groups are different
from the binary groups in that the distributed code is not compiled and
is in text format. The people receiving code from these groups are
expected to have the facilities to compile the programs into executable
form.

## [7. Setting up a new moderated group](#7TOC){#7}

This is very dependent on the news system employed (e.g., INN, C News,
ANU). Refer to the documentation supplied as part of the news transport
software for the specific steps required to set up a moderated group.

There are, however, a few general steps in common.

1.  Assure that the moderator has an active account on the system from
    which moderation will be performed. Create it if needed.

2.  Choose and install the submission aliases for the moderator. Two
    aliases are usually needed, one for receiving actual submissions,
    and another for receiving administrative requests.

    **news.group.name -> news-group-name & news-group-name-request**

3.  Ensure that whatever server, filter or auto-reply software will be
    used by the moderator is available on the system. Install and test
    it if necessary.

4.  Install the forwarding entry for the moderated group into the
    mailpaths or moderators file, or equivalent.

5.  Finally, the group must be created and marked moderated, using the
    'm' flag in the 'active' file. This is done using the tool
    appropriate for your news transport. (Eg: newsbin/maint/addgroup for
    C News or 'ctlinnd newgroup' for INN)

The same steps are used to moderate a pre-existing group which is being
changed from un-moderated to moderated status.

If you have further questions, post them in
[news.software.b](https://web.archive.org/web/20071021025547/news:news.software.b)
or
[news.admin.technical](https://web.archive.org/web/20071021025547/news:news.admin.technical).



### [7.1. Submission aliases](#7TOC){#7.1}

When you set up your group you will need to establish two mail aliases,
so that directly posted articles and emailed submissions can reach you.

-   The address for submissions to the list. It is better if this is not
    the name of the newsgroup itself, but something similarly
    descriptive. For example,
    [comp.source.reviewed](https://web.archive.org/web/20071021025547/news:comp.source.reviewed)'s
    address for submissions might be

    **csr@host.domain**

-   An address where requests and administrative information should be
    sent. Normally this address is "FOO-request" for submission
    address "FOO". Using the example of
    [comp.sources.reviewed](https://web.archive.org/web/20071021025547/news:comp.sources.reviewed)
    above, the associated request list address would be

    **csr-request@host.domain**

Depending on the expected newsgroup and administrative volume, it may be
appropriate to have both aliases point to the same place, while
retaining the ability to reconfigure the destinations locally. You will
need to notify the appropriate people to assure the [mailpaths
file](/web/20071021025547/http://www.landfield.com/usenet/moderators/handbook/mod05.html#5.1)
is updated. Usenet moderators refer to [Appendix
A](/web/20071021025547/http://www.landfield.com/usenet/moderators/handbook/appendixA.html).



### [7.2. Email submission servers](#7TOC){#7.2}

If your group is to have multiple moderators then you might want to
consider setting up a truly co-moderated group. This would be useful for
high-volume newsgroups.

Greg Woods <woods@ncar.ucar.edu> has written a program to support
multiple moderators. When mail is sent to the moderated group alias, it
is routed by sendmail to the program, which randomly selects one of the
list of moderators to handle the submission. The submission is then
forwarded to that moderator. (The program is available in the
[moderators' tools
archive](/web/20071021025547/http://www.landfield.com/moderators/).)

STUMP (Secure Team-based USENET Moderation Program) is a robomoderator
allowing teams of moderators or individual moderators to moderate a
newsgroup, via email or Web interface. STUMP allows for preapproved and
banned lists, has built-in forgery protection, and a mechanism to
automatically reject certain invalid messages. It requires no tools on
the individual human moderators' machines. STUMP itself runs in a Unix
account. It is currently used in many USENET newsgroups and is available
from

[http://www.algebra.com/~ichudov/stump](https://web.archive.org/web/20071021025547/http://www.algebra.com/~ichudov/stump/)

See [Section
10](/web/20071021025547/http://www.landfield.com/usenet/moderators/handbook/mod10.html)
for additional discussion of team moderation.

## [8. Choosing a moderation policy](#8TOC){#8}

Before you can write up the policies that are going to guide you in
moderating your group, there are a few things to consider.



## [8.1. Article rejections](#8TOC){#8.1}

When an inappropriate posting is submitted to the newsgroup, the
moderator should send the submitter email informing the sender that
their submission was inappropriate for posting to the group. If
possible, suggest a newsgroup where the posting might be appropriate.
Forwarding a canned message can save the moderator time and assure that
the submitter knows which newsgroups might be an acceptable alternative.



**

"I am sorry but I am unable to post your request to the newsgroup
comp.sources.misc. This newsgroup is a moderated newsgroup whose sole
purpose is for the distribution and archiving of source code.

Requests for software can be made to comp.sources.wanted or a more
specific newsgroup if one exists. Requests for help with the sources
gathered from the net should be made to the newsgroups comp.sources.d or
comp.sources.bugs depending on the type of the problem."



If the article is cross-posted to other groups, the moderator should
inform the submitter that the article did not appear in the other groups
specified in the Newsgroups: line. Do not repost it yourself - this may
get you into problems. Send the entire article back to the poster, so
that he or she can repost it to a non-moderated group, if so desired.

Some common reasons why articles are rejected are:

-   Submitted article does not fall within the charter of the group,
-   Copyright or reprint permission problems,
-   Previously posted question has already been answered,
-   Excessive quoting,
-   Asking something specified in the group's FAQ or policy posting,
-   Message targeted towards one person and should have been sent via
    email to that person,
-   Articles that are just flames with little to no real substance.

[See [Section
2](/web/20071021065355/http://www.landfield.com/usenet/moderators/handbook/mod02.html)
and [Section
17.1](/web/20071021065355/http://www.landfield.com/usenet/moderators/handbook/mod17.html#17.1)
for discussions of the difference between moderation and censorship.]



## [8.2. Copyrights](#8TOC){#8.2}

Copyrighted submissions should not be posted without the explicit
permission of the copyright holder or the appropriate release authority.
Any such release notice should be prominently visible in the article.
This rule applies equally to general articles, images, and software. If
there are any questions about the legality or approval status of a
submission, the moderator should not post it until appropriate
permission has been received.

In the opinion of the moderators who helped write this document, there
should be no "compilation copyright" placed on the newsgroup by the
moderator. The newsgroups are a collective effort, the result of the
sites that pass the newsgroup around, the kind souls that maintain
software and article archives, and -most importantly- the people who
write the articles. Please note, in no way can a moderator-supplied
copyright notice supersede the copyright of the individual submitters.



## [8.3. Dealing with forged Approved: headers](#8TOC){#8.3}

As moderator of your group, you are within your rights to cancel
articles with forged Approved: headers at any time you wish.

It is not possible to stop someone from posting to a moderated newsgroup
if they know how. All you can do is complain at them, or complain to
root@ or postmaster@ or usenet@ or newsmaster@ or news@ the offending
host.

In the end, if they choose to continue to ignore convention, the Usenet
community can try to get their site's NetNews feeds cut off by
convincing their neighbors to stop feeding the offenders.

If there are repeated forgeries, or if a forged article causes
widespread confusion among readers, it is wise to inform the net in the
appropriate newsgroups (i.e.
[news.admin.policy](https://web.archive.org/web/20071021065355/news:news.admin.policy))
that these are forged postings and of the trouble you are having. Often
a public denouncement will be enough to make the offender stop. Note
that few people bother to denounce forgeries posted on April 1.

Another approach is to have an auto-canceler script that verifies all
articles received by the moderator's site in the moderator's newsgroup
have been posted by the moderator or a backup moderator. If an article
is encountered that was not posted by the moderator then the script
automagically cancels the article and a mail message is sent to the
sender parties involved. Naturally, this is tricky when there are
changing or multiple moderators. There are also potential problems
generated due to propagation delay. There are auto-canceler scripts
available in the [moderators
archive](/web/20071021065355/http://www.landfield.com/moderators/)
described in [Section
15](/web/20071021065355/http://www.landfield.com/usenet/moderators/handbook/mod15.html).

If forgeries are not a common problem on a newsgroup, canceling by hand
when they do come up is probably the best option.



## [8.4. Commercial postings](#8TOC){#8.4}

The group charter should state clearly what the policy on posting
articles of a commercial nature should be. If the group charter does not
address this issue, or is unclear, then the moderator must define a
clear and consistent policy on the subject. The policy should be
documented before the issue arises, so that the newsgroup's readership
knows what to expect to have done.

Don't believe the myth that commercial postings are not allowed on
Usenet. In reality, commercial posting have been traversing the world
via Usenet newsgroups almost since the beginning of NetNews.

With that said, blatant commercials and hyperbole are roundly frowned
upon. It is best to spell this out in the policy. The important thing is
that you post only what the readers want (learned via a survey maybe). A
good way to describe a generally acceptable policy:

**"Information, not promotion."**



## [8.5. Dealing with cross-posted articles](#8TOC){#8.5}

The moderator needs to determine how cross-posted articles are going to
be handled for the group. In some cases the moderator may honor the
Newsgroups: lines which list other newsgroups outside the moderator's
control. In other cases the moderator's policy may state that
cross-posting will never be done, or will be done only at the
moderator's discretion.

If an article submitted to a moderated group is rejected, then it does
not get posted to the unmoderated groups listed in the Newsgroups: line.
This is a little unfair to the submitter if the moderator does not
inform the submitter of the situation. Not all readers/submitters are
aware of how NetNews moderation works.

Some moderators refuse to honor any cross-postings listed on the
Newsgroups: line and only post to their own group. There is nothing
wrong with this policy but the moderator should assure that the group's
readership is aware of the policy.

Articles are sometimes cross-posted to multiple moderated groups. In
those cases, it is important to make sure that moderators of all groups
have approved the article before it is actually posted. [See [Section
16.6](/web/20071021065355/http://www.landfield.com/usenet/moderators/handbook/mod16.html#16.6)
]

9. Backup moderators



Each new moderator should recruit one or more people willing to serve as
a backup, on a permanent or temporary basis as needed. These backups
should be located as soon as possible after the moderator is selected.

The need for a backup moderator depends a lot on the nature and volume
of the group. A newsgroup that contains mostly pre-approved
[FAQs](/web/20071021065659/http://www.landfield.com/faqs/) from other
groups, such as some of the *.info groups gaining popularity, needs
backup moderators a lot less than a high-volume discussion group or a
time-sensitive *.announce group.

Having others who can fill in temporarily, if the need arises, serves as
an insurance policy for the primary moderator. You may need to take some
time off from moderator responsibilities due to work schedules,
vacations, or net connectivity problems, to name a few common reasons.
In those cases, having a pre-selected backup assures the newsgroup's
continuity during periods when you are unavailable.

## [10. Multiple or Team Moderation](#10TOC){#10}

In some cases it might be possible to share a moderation job, rotating
from one person to another. No one moderator should become hard to
replace. In many cases, a diversity in moderation styles and filtering
choices will enrich a group.

If the topic of your group makes it possible for you to split the task
(by sub-topic or otherwise) consider it desirable to "farm out" the
work as it reduces moderator burn-out. As 'titles' are an easy reward
to give, consider 'Guest Moderators', 'Associate Moderators' and
'Co-Moderators'.

For extremely high volume newsgroups it may be necessary to have the
group moderated by a team of moderators. Some such groups have as many
as 10 moderators. There are benefits for having a team of moderators,
including,

-   no need for backup moderators,
-   much easier to go on vacation or take a short break,
-   consulting/second opinion on topics of concern,
-   possible to have a moderator dedicated to answering queries.
-   more bodies working towards making the newsgroup a better resource,

There are different ways for a team of moderators to manage a
newsgroup's volume. STUMP (Secure Team-based USENET Moderation Program)
is a robomoderator allowing teams of moderators or individual moderators
to moderate a newsgroup, via email or Web interface. For more
information on STUMP, see

[http://www.algebra.com/~ichudov/stump/](https://web.archive.org/web/20071021065531/http://www.algebra.com/~ichudov/stump/)

Reguardless of the software used, there are things that any moderation
team should be aware of and need to do. Setting up the process and rules
of team moderation is critical to a successful group. Don't forget team
moderation is a real "team" effort.



### [10.1. Team moderator mailing lists](#10TOC){#10.1}

Like any other moderated newsgroup, an alias for submissions to the
newsgroup should be setup. The incoming articles need to be distributed
among the moderators. There are software packages available in the
moderators archive which do this. Three strategies for submission
distribution among moderators are:

-   systematic distribution,
-   random distribution,
-   moderator selected message locking.

Systematic distribution usually targets the next moderator to receive a
submission in a round-robin fashion. [See [Section 7.2. Email
submission
servers](/web/20071021065531/http://www.landfield.com/usenet/moderators/handbook/mod07.html#7.2)
for a description of random distribution.] The *.answers moderators
have set up a scheme whereby all incoming messages are entered into a
queue, and individual moderators lock messages to take them out of the
queue for servicing. This has the advantage that should an individual
moderator take a vacation, absolutely no reconfiguration needs to be
done.

Besides the normal submission and administrative list address it is
necessary to have a list address for the moderation team members. In a
team moderation scenario, it is recommended that moderators communicate
closely with each other to enforce a standard moderation policy and to
discuss matters relating to the newsgroup.

Any message sent to the team list goes to all the group moderators. It
is also helpful for any reader who may wish to pose a question or make a
comment to all the moderators.

A pointer to the team moderators list should be included in the group's
FAQ or the group's policy posting.



### [10.2. Facilitators](#10TOC){#10.2}

Someone needs to be responsible for maintaining the list of moderators
receiving the submissions. The moderator team list needs to be
frequently updated as moderators go on leave etc. This may be an
existing group moderator but it should more properly be a non- moderator
acting as a facilitator.

More successful team moderated groups have a group of people working
with the group moderators supplying unbiased services to the team. For
example, facilitators provide additional services to the group and the
moderation team by:

-   maintaining the distribution script,
-   writing and maintaining FAQs,
-   'owners' of moderation submission, administrative and team mailing
    list addresses/facilities,
-   maintaining the official group archives or WWW access,
-   supplying other group specific needs.

What facilitators are NOT expected to do is:

-   receive articles for the newsgroup,
-   review articles for the newsgroup,
-   post submitted articles to the newsgroup.

In times of group crisis, facilitators should have the right to post an
article using an 'Approved:' line. It is expected that facilitators
would only post original articles explaining the situation or its
solution as absolutely necessary to resolve a moderator conflict.

Having a good communication among not only the moderators but also the
facilitators keeps the newsgroup functionality healthy. An example of
such a mailing list is: 'srg-admin@aldhfn.org' for the group
soc.religion.gnosis. Another example is 'ww2-mods@acpub.duke.edu'.

In this case, the mailing list for the moderators and facilitators is
the same one.



### [10.3. Rejection Notices](#10TOC){#10.3}

It is recommended that all rejection notices sent out, in multiple
moderators environment, be carbon copied to all the moderators and
facilitators. This helps in avoiding confusion & conflicts.

In general, all rejections should be honored by co-moderators, unless
majority moderators overturn it.



### [10.4. Multiple moderator conflict resolution](#10TOC){#10.4}

Sometimes conflicts between moderators can get out of hand and spill
over into the group. Then everyone suffers.

In extreme cases, with a polarized readership, it's generally better to
have all moderators resign and stand for re-election, or choose some
other way of letting the readership have its say, rather than relying
on, for example, confidence motions among the moderators.

In some cases, it makes sense to use a corporate board of directors
model for moderatorship, and document it officially.

This is something that needs to be decided early and not something to be
decided when the problem arises. It should be documented in the group's
policy posting at a minimum and really should be addressed in the
group's charter if possible.

Methods of handling inter-moderator conflicts need to be decided before
conflicts arise, especially in groups which handle a controversial or
emotional topic. Once a problem gets out of control, it can be difficult
to get people to agree on a method for resolving it. These methods
should be documented in the group's policy posting or available from
the official FTP site.

## 11. Handling temporary moderator absences

In the event that a moderator is not able to perform the duties of the
moderator for some small length of time, such as a vacation, the
moderator should inform the community by posting to the appropriate
newsgroup, that there will be a delay in posting articles. It is not
usually necessary to give a reason for the delay, though you may choose
to do so. If a moderator finds that they will be unable to perform their
duties for a more extended period of time, they should allow the backup
moderator to assume posting responsibilities until the primary moderator
is able to once again assume the responsibilities of posting to the
newsgroup. In this manner, articles submitted can to be posted to the
newsgroup in a timely fashion and the newsgroup continues to be a
resource the NetNews community can depend on.

## [12. Gatewaying newsgroups to mailing lists](#12TOC){#12}

There are people who will hear about your group who do not have access
to network news distributions or software. You may want to set up a
mailing list that allows your group to be a resource for those who have
email access but no NetNews access. Here are a couple of approaches you
will want to consider.



### [12.1. Newsgate](#12TOC){#12.1}

Rich Salz has written a package named "newsgate" that is in wide
spread use for bidirectionally gatewaying articles posted to a newsgroup
into email. Rich has turned over the maintenance for newsgate to the
[Internet Software
Consortium](https://web.archive.org/web/20071021065450/http://www.isc.org/isc/).
You can retrieve a copy of the sources to newsgate at
[ftp://ftp.isc.org/isc/inn/contrib/newsgate.tar.Z](https://web.archive.org/web/20071021065450/ftp://ftp.isc.org/isc/inn/contrib/newsgate.tar.Z).

His kit provides two programs for "linking" RFC 822 Mail messages and
RFC 1036 Network News articles. Each half of the conversion is handled
by a different program, mail2news or news2mail. A few utility programs
are also included.

With these programs and the right set of mail aliases, news sys and
active file entries, it is possible to build any set of moderated,
unmoderated, one-way, or bi-directional gateways between any set of news
and mail groups and lists that you may need to support your group.

Installation instructions (sample /usr/lib/news/newsfeeds and
/etc/aliases entries are provided in the documentation for newsgate.

**NOTE: Even though the documentation tells you to use inews, you should
use rnews instead and please be careful not to produce loops!**



### [12.2. Listserv](#12TOC){#12.2}

Another method of gatewaying is via LISTSERV gateways. It is relatively
easy to arrange a two-way gateway between a BITNET list and a moderated
group. (For example, the group
[comp.compilers](https://web.archive.org/web/20071021065450/news:comp.compilers)
and the list COMPIL-L@AMERICAN.EDU carry the same content.) It works
automatically; the gateway there picks up messages from the group as
they arrive and sends them to the list. It also forwards submissions to
the moderator. The moderator can do any necessary list maintenance, such
as deleting the addresses of people who forget to unsubscribe before
their accounts expired, via email.

If you are interested in finding out more about establishing a LISTSERV
gateway send a message to
[listserv@auvm.american.edu](https://web.archive.org/web/20071021065450/mailto:listserv@auvm.american.edu)
with a body of

**send netgate policy**

and an informational file will be returned via email. Questions about
Listserv/NetNews gateways can be posted to
[bit.admin](https://web.archive.org/web/20071021065450/news:bit.admin)
or sent to
[news-admin@auvm.american.edu](https://web.archive.org/web/20071021065450/mailto:news-admin@auvm.american.edu)
or
[NEWS-ADM@AUVM.BITNET](https://web.archive.org/web/20071021065450/mailto:NEWS-ADM@AUVM.BITNET).

## [13. Creating Periodic Informational Postings](#13TOC){#13}

One of the best ways to communicate with your readership, as well as a
tool for saving you time, is via a policy posting, and potentially
additional [Frequently Asked Questions postings
(FAQ)](/web/20071021065305/http://www.landfield.com/faqs/).

A policy posting is an article that describes how you will run the
newsgroup. It should include information describing the use of any
additional Auxiliary header lines, how and where articles should be
submitted, and general guidelines for the group (often including the
charter) used by you in performing the responsibilities as the
newsgroup's moderator.

Other things that might be included are:

-   How you will deal with cross-posted submissions,
-   How postings of a commercial nature will be dealt with,
-   Use of backup or multiple moderators,
-   Items concerning the group that have been hashed out via the group
    or moderator lead surveys,
-   Where to obtain a current copy of the informational postings outside
    of the newsgroup. If possible, an email location or mailserver
    should be included, since not all users have FTP capabilities,
-   A list of sites, if any, that archive the group as well as how to
    become an archive site,
-   Moderator conflict resolution methods,
-   Moderator replacement policy.

This posting should be made periodically to the group.

Your group may be best served by having both a periodic policy posting
and an FAQ. Quite often it becomes necessary to have a Frequently Asked
Questions posting. Readers drop in and out of newsgroups frequently, and
may not be familiar with previous discussions. A FAQ posting can help
reduce the number of duplicate questions submitted to the newsgroup.

FAQ posting(s) do not have to be written, or even directly posted, by
the primary moderator. Many moderated groups have a group of relevant
FAQs posted, written by a number of authors. It is perfectly acceptable
to simply give an FAQ author permission to post or cross-post the FAQ
into your newsgroup. All the poster needs to do is add the appropriate
Approved: header to the FAQ posting. (Of course, if the moderator gives
others permission to post to the group, automatic cancellation software,
if used, should not cancel those articles.)

More suggestions about writing and maintaining FAQs, as well as
information about automatic FAQ-posting software, can be gotten from the
**faq-maintainers@faqs.org** mailing list. To subscribe, send a message
to

[faq-maintainers-request@faqs.org](https://web.archive.org/web/20071021065305/mailto:faq-maintainers-request@faqs.org)

There is a good deal of information about writing FAQs and the FAQ
posting process available from

[http://www.faqs.org/authors.html](https://web.archive.org/web/20071021065305/http://www.faqs.org/authors.html)

Having these types of documents as a consistent part of the group will
save you from answering the same questions again and again. The
readership will be able to get the majority of the information about the
group from the group itself. When people submit requests for information
that has already been covered, it is easy to simply forward the
appropriate informational posting to them, or send them a pointer to it.



### [13.1. Copyright](#13TOC){#13.1}

Recently there has been a lot of discussion about implicit and explicit
copyrights on policy and FAQ postings. This has become an issue, in
part, due to the increasing number of CD-ROM vendors and Internet How-To
book authors, who reproduce informational postings in commercial
products, with or without obtaining the permission of the authors or
maintainers.

It is wise to document your copyright and any distribution restrictions
within your periodic postings. In most cases you should try to be as
open as possible. The purpose of the newsgroups is to communicate
information to the community at large. Your information is probably
archived and available in many ways and places that you are not aware
of; it does not make a lot of sense to be overly sensitive to one
particular use of postings that have already been broadcast freely all
over the world. Remember that copyright laws can vary widely among the
many countries where your posting goes.

If asked, it is up to you if you want to see your group's informational
postings included. A suggestion might be to send a message back such as:



***I give you permission to use my FAQ for the group 'your.group' as
you have requested with the following additional conditions:***

1.  You state explicitly that the information in the FAQ may not be
    entirely correct or up to date. That information should not be used
    directly without first checking it out. FAQ information is only a
    guideline.
2.  Do not change the content of the FAQ in any way but may reformat it
    to better integrate with your production media.
3.  Assure that credit is given as appropriate.
4.  You send me a free copy of the {book/cdrom...}



This is just a suggested starting point; feel free to modify it as
needed to suit your policies.



### [13.2. Frequency of distribution and news.answers](#13TOC){#13.2}

You will need to determine how often your informational postings are
actually posted to your group. Sources groups post them at the beginning
of each new volume in the archives. Discussion and announcement group
moderators may decide to post them on a periodic basis, usually once a
month. The policy statement should document how often informational
posting are done. If there are many requests for the FAQ, or repeats of
FAQ information, it may make sense to post the FAQ more often, or to
frequently post an explanation of how to obtain the FAQ or policy
posting.

It is strongly suggested that your policy posting and any FAQ have a
consistent Subject: line every time that it is posted, to assist readers
in recognizing it.

You may also want to consider cross-posting your informational postings
to
[news.answers](https://web.archive.org/web/20071021065305/news:news.answers)
and the other appropriate *.answers newsgroups. This requires the prior
approval of the *.answers moderators. The process is fairly easy, and
is described in the posting

[Introduction to the *.answers
Newsgroups](https://web.archive.org/web/20071021065305/http://www.faqs.org/faqs/news-answers/introduction/preamble.html)

posted regularly to
[news.announce.newusers](https://web.archive.org/web/20071021065305/news:news.announce.newusers),[news.answers](https://web.archive.org/web/20071021065305/news:news.answers)
and the other *.answers groups, and

-   [*.answers submission
    guidelines](https://web.archive.org/web/20071021065305/http://www.faqs.org/faqs/news-answers/guidelines/preamble.html),
    the
-   [*.answers post-approval
    guidelines](https://web.archive.org/web/20071021065305/http://www.faqs.org/faqs/news-answers/postapproval-guidelines/preamble.html)

posted regularly to all of the *.answers groups (
[alt.answers](https://web.archive.org/web/20071021065305/news:alt.answers),
[comp.answers](https://web.archive.org/web/20071021065305/news:comp.answers),
[humanities.answers](https://web.archive.org/web/20071021065305/news:humanities.answers),
[de.answers](https://web.archive.org/web/20071021065305/news:de.answers),
[misc.answers](https://web.archive.org/web/20071021065305/news:misc.answers),
[news.answers](https://web.archive.org/web/20071021065305/news:news.answers),
[rec.answers](https://web.archive.org/web/20071021065305/news:rec.answers),
[sci.answers](https://web.archive.org/web/20071021065305/news:sci.answers),
[soc.answers](https://web.archive.org/web/20071021065305/news:soc.answers),
and
[talk.answers](https://web.archive.org/web/20071021065305/news:talk.answers).)
Additionally, they can be found archived at

[http://www.faqs.org/faqs/news.answers/](https://web.archive.org/web/20071021065305/http://www.faqs.org/faqs/news-answers/)

The basic requirements for cross-posting to *.answers, above basic
compliance with RFC 1036, are meeting the *.answers standards for the
consistent content of a few of the standard header lines, and the
addition of an auxiliary header containing an Archive-name: header.
There are no format restrictions whatsoever on the contents of postings
to *.answers.

The *.answers groups are archived on
[rtfm.mit.edu](https://web.archive.org/web/20071021065305/ftp://rtfm.mit.edu/pub/usenet/)
and elsewhere around the world such as on
[www.faqs.org/faqs/](https://web.archive.org/web/20071021065305/http://www.faqs.org/faqs/).
If you are not sure if your consistent content of a few of the standard
header lines, and the addition of an auxiliary header containing an
Archive-name: header. There are no format restrictions whatsoever on the
contents of postings to *.answers.

Even if you do not want to cross-post your informational posting to
*.answers, you should have it listed in the

["List Of Periodic Informational
Posts"](https://web.archive.org/web/20071021065305/http://www.faqs.org/faqs/periodic-postings/)

which is posted regularly to
[news.lists](https://web.archive.org/web/20071021065305/news:news.lists)
and
[news.answers](https://web.archive.org/web/20071021065305/news:news.answers).
To have your informational posting listed, send it to

[news-answers-request@mit.edu](https://web.archive.org/web/20071021065305/mailto:news-answers-request@mit.edu),

with a note saying what the posting frequency is, and that you wish to
add your posting to the List of Periodic Informational Posts, but are
not seeking approval for cross-posting to *.answers.

## [14. Archiving postings to the group](#14TOC){#14}

It is very common for a moderator to keep an archive of the discussion
in their group. While this is recommended, disk space limitations may
prevent it. Newsgroup archives are more feasible on Internet sites where
they can be made available via anonymous FTP. If you keep an archive
accessible via UUCP you'll probably get requests for back issues that
you may have to fill by hand. LISTSERV gatewayed lists can do this very
conveniently, complete with automatic archival and on-demand retrieval.



### [14.1. FTP Archives](#14TOC){#14.1}

You should list archives that you consider official in your group's
policy posting. There are tools to assist you in keeping your archives
up to date with a minimum of effort. An example is the
["rkive"](https://web.archive.org/web/20071021065543/http://www.landfield.com/rkive/)
package written by [Kent Landfield
<kent@landfield.com>](https://web.archive.org/web/20071021065543/mailto:kent@landfield.com).
It allows you to automatically archive some or all articles as they
arrive in a newsgroup and will create the appropriate Index files.



### [14.2. Email Archives](#14TOC){#14.2}

You may find it useful to set up email-based access to your archives. If
so, see the FAQ titled

["Mail Archive Server Software List,
A Summary of Available Mail Archive Server
Software"](https://web.archive.org/web/20071021065543/http://www.faqs.org/faqs/mail/archive-servers/faq/),

initially written by Jonathan Kamens and currently maintained by Piero
Serini. (piero@strider.st.dsi.unimi.it) and is posted periodically to
[comp.mail.misc](https://web.archive.org/web/20071021065543/news:comp.mail.misc),
[comp.sources.wanted](https://web.archive.org/web/20071021065543/news:comp.sources.wanted),
[comp.answers](https://web.archive.org/web/20071021065543/news:comp.answers)
and
[news.answers](https://web.archive.org/web/20071021065543/news:news.answers).
It is also available from sites that archive
[news.answers](https://web.archive.org/web/20071021065543/news:news.answers).

For reference purposes, email-based archive access programs are often
known as "mailservers."



### [14.3. Archives of selected articles](#14TOC){#14.3}

Some moderators find it useful to set up selective archives of
noteworthy articles from their groups. For example,
[rec.food.recipes](https://web.archive.org/web/20071021065543/news:rec.food.recipes)
has an FTP archive of categorized recipes, and
[alt.sewing](https://web.archive.org/web/20071021065543/news:alt.sewing)
has an archive of collected posts about specific sewing techniques.
Although it takes a great deal of human effort to maintain such
archives, they are generally more useful than wholesale archives,
especially for high-volume discussion groups.

15. Tools for moderators



An archive of tools written and used by moderators of Usenet newsgroups
now exists. In the past, most moderators were forced to write much of
their posting software by themselves, though sometimes other experienced
moderators would share their sources when asked. Until recently there
has not been a single archive where moderators could make what they had
available for all to use.

Moderators both new and existing can see how others with similar types
of newsgroups are doing their job. A much wider set of support software
is becoming available to the moderating community as we all bring our
tools out of the closet. There is no reason new moderators need to
develop their own software/support environment from scratch as has been
the norm in the past. To make the tools most useful, the moderator will
probably need to be familiar with the 'C' language, UNIX shell and
perl scripts, in order to adapt them to their own group's needs.

The contents of the moderators' tools archive have been generously made
available in an "AS IS" condition. The archive is a snapshot of
existing tools, as they are being used, rather than a formal release of
polished software. Many of the sources, scripts, and supporting
documentation are not as pretty as their authors might wish, but they
work. The tools are being made available so that other moderators can
see working examples of how the tasks are handled, and potentially use
them as a starting point for their own custom tools.

If you would like to contribute, either send your tools to

[mod-archive@landfield.com](https://web.archive.org/web/20071021065632/mailto:mod-archive@landfield.com)

or send email explaining where the tools can be picked up.

The moderator's tool archive is available via HTTP or FTP from

[http://www.landfield.com/moderators/](https://web.archive.org/web/20071021065632/http://www.landfield.com/moderators/)
or
[ftp://ftp.landfield.com/moderators/](https://web.archive.org/web/20071021065632/ftp://ftp.landfield.com/moderators/)

[UUNET](https://web.archive.org/web/20071021065632/http://www.uu.net/)
mirrors the tools directory and has made it available via FTP from

[ftp://ftp.uu.net/networking/news/moderating/](https://web.archive.org/web/20071021065632/ftp://ftp.uu.net/networking/news/moderating/)

## [16. News transport gotcha's](#16TOC){#16}

There are a few quirks in the network news transport software that you
might encounter, and should be aware of. What follows is far from a
complete list but does include the ones most commonly encountered.



### [16.1. Line lengths](#16TOC){#16.1}

The [NNTP reference
implementation](https://web.archive.org/web/20071021025645/http://www.academ.com/academ/nntp/)
package in use on the Internet has a limit on the number of characters
that an individual line may contain. Submissions containing lines longer
than 512 bytes will be corrupted because the reference servers will
truncate the lines longer than 512 bytes.

In general you should limit your individual line lengths to 79
characters or less if possible. Systems that have fixed record lengths,
such as some BITNET IBM servers, can drop text longer than that.



### [16.2. Old C News blanks-in-ng bug](#16TOC){#16.2}

If there is a newsgroup line in an article like this

**Newsgroups: comp.unmoderated, comp.moderated**

some older versions of C News fail to skip the space after the comma and
so only see the group "comp.moderated" which of course is not
moderated and passes it along. When the message hits a B News site, the
space is squeezed out, the moderated group is seen for the first time
and the message gets mailed in. This has been fixed in later C News
releases, but sites running older software will still act this way.



### [16.3. B News non-local unapproved articles bug](#16TOC){#16.3}

As mentioned in [Section
5](/web/20071021025645/http://www.landfield.com/usenet/moderators/handbook/mod05.html),
most news servers will automatically forward unapproved postings to the
moderator. This should only occur for local postings, otherwise,
situations can occur where the moderator gets far more than one copy of
the same article. B News forwards non-local articles too. This coupled
with the old C News blanks-in-ng bug has been responsible for moderators
being deluged with hundreds of copies of an article. It's particularly
nasty when the newsgroup has been recently unmoderated and not every
server has respected the control message and the ex-moderator gets
bombed.

To be fair, the B News behavior of mailing unapproved non-local articles
to the moderator was not a "bug". It was a "feature".

It used to be that B News was the only game in town. It used to be that
people ran ancient software versions forever. In such an environment, it
was useful for a site receiving an article that should have gone to the
moderator to assume that the previous hosts were running old software,
and do the moderator-send itself. That is not the case today.

This bug has not been fixed, and never will be because B News is no
longer being supported. Fortunately, B News is dying out.



### [16.4. Article size concerns](#16TOC){#16.4}

In some places, such as small systems and news-to-mail gateways, there
are problems when individual article sizes exceed software limits. We
need to either remove builtin system limitations or work around them.
Since it takes time to remove old software versions and overcome
hardware limitations netwide, the best course of action is to work
around the limitations so that the news will get to all sites.

Individual postings should be less than or equal to 60K. If it is
necessary to split the posting into multiple parts, each part should be
less than or equal to 60K. This is due to the architecture restrictions
of some older systems. This restriction is more in the minds of the
users on the net than the software running it. Postings of 90K
successfully make it through most present day news systems. Many mail
systems have limitations of 100K on messages that pass through them.
This is a concern because there are news to mail gateways that deliver
and post news via electronic mail.

Note that some commercial gateways to the Internet have broken news and
mail software that truncate anything over around 25K. Most are in the
process of correcting their sub-standard software but at this point that
has not been universally accomplished.



### [16.5. Amount of messages posted daily](#16TOC){#16.5}

Moderators of high volume newsgroups should try to limit the amount of
data posted per day so as not to flood news spool directories on smaller
systems. A good rule of thumb is to limit posting to 800K per day if
possible.

If you are overwhelmed with posts on one day, it may be better to hold
some articles back until the next day. Articles can be posted either in
chronological order, or grouped by subject. On the other hand, it is not
a good idea to loosen your acceptance standards simply because fewer
articles were submitted in a given time period - in most cases it is
better to have lower volume than lower quality.



### [16.6. Cross-posting to other moderated groups](#16TOC){#16.6}

None of the NetNews software handles cross-posted moderation very well,
largely because there is no consensus on what the correct action is.
What actually happens is that the posting software picks one of the
moderated groups more or less at random (usually the first moderated
group) and mails the message to its moderator. If the posting software
used by the moderator who received the article does not check for other
moderated newsgroups, the article will appear in the newsgroup of the
other moderated group without being approved by the appropriate
moderator.

Moderators should try to bullet-proof the posting software by making it
check cross-posting to multiple moderated groups. But until NetNews gets
a far more sophisticated posting scheme, e.g., one that lets a moderator
add a new newsgroup to a message already in circulation, glitches like
this will happen.

Remember that it is often VERY desirable to cross-post among moderated
newsgroups:

Many of the postings in
[news.answers](https://web.archive.org/web/20071021025645/news:news.answers)
are cross-posted into the group from other moderated groups.



### [16.7. Extra headers on directly posted articles](#16TOC){#16.7}

Some submissions will arrive with two sets of headers. The "real"
headers will be a set of generic mail headers; the news headers will be
included as text within the body of the mail message. Even worse, in
these cases the mail headers may indicate that the article is "From"
usenet@site or news@site, making it difficult to identify or respond
to the actual author.

This is the article-headers-in-body problem caused by C News feeding the
article into UCB Mail or mailx instead of /bin/mail, which usually
incorporates the news headers into the mail header.

Explanation: in C News, the newsbin/relay/injnews script is used by
inews to do site-specific header bashing. When it discovers the
newsgroup is moderated, it invokes mail to send off the article to the
moderator (via mailpaths). Unlike B News and INN, where time has been
spent to configure how to use the mail transport directly (to merge the
news headers in with the mail headers), C News blindly punts the article
into "mail" which is a user agent, which often refuses to accept
"header-like" stuff at the beginning of a message as part of the [RFC
822](/web/20071021025645/http://www.landfield.com/rfcs/rfc822.html)
header block. In essence, mail will often implicitly put a blank line at
the beginning of the message, so the headers carefully crafted by
injnews end up as part of the body instead of the mail headers.

If this becomes a problem for you, it would be appropriate to send a
message to usenet@ and/or postmaster@ at the offending site with a
suggestion on how to fix their C News injnews script.

[See [Appendix
B](/web/20071021025645/http://www.landfield.com/usenet/moderators/handbook/appendixB.html)
for a description of the solution. A template message is included that
will allow you to inform the offending site of both the problem and the
solution.]



### [16.8. Multiple copies of the same submission received](#16TOC){#16.8}

There are a number of different reasons why you may get many copies of a
submission:

-   A mailer or gateway bug that keeps resending the same message
    (distinguished by having the same sites in "Received by" headers).
-   The posting site doesn't have the group marked as moderated
    (usually you only get a few extra copies of the message, all with
    short "Path" headers, if any).
-   Interaction with the C-news problem when there is a space in the
    list of newsgroups; when it gets to a B-news site, the space is
    squashed out and the moderated group is recognized (there are
    multiple newsgroups in the header, and your moderated group is not
    the first in the list).
-   Submitter was unaware that the group was moderated and repeatedly
    attempted to post the article to the group since their article did
    not immediately appear in their local newsgroup.

Contacting the administrator of the site where the problem posting was
generated is probably a good first step.



### [16.9. B News static Newsgroup: header limit](#16TOC){#16.9}

B News inews has a static limit of 256 bytes for header lines. One might
think that this limits Newsgroups: headers to about 254 bytes, but
unfortunately the practical limit is lower than that. The Xref: header,
which is generated from the Newsgroups: line plus article numbers, is
longer than the Newsgroups: header. If the Xref: header at a particular
site is longer than 256 bytes, the article simply will not appear at
that site.

Since the length of the same article's Xref: header varies from site to
site, and cannot be easily computed in advance, it is necessary to leave
some spare room in the Newsgroups: header. Set a fair limit on the size
of the Newsgroups: header, and make a policy prohibiting cross-posting
to more groups than will fit on the line. Some moderators have decided
on a 200-character limit for the entire Newsgroups: line.

## [17. How to deal with your readership](#17TOC){#17}

Moderators need to take the time to figure out how they wish their
newsgroup to be perceived on the net. Some of this is forced upon the
moderator by the group's charter but much of it is up to the moderator.
Are you planning on being proactive in keeping discussions going and on
track ? Do you see yourself only as a filter for the group hoping to
keep yourself totally in the shadows ? Or do you plan to be somewhere in
the middle of the two ? And how will you deal with the submitters ? Much
of the perceived success in being a moderator is how your deal with your
group's readership.



### [17.1. Personality of your group](#17TOC){#17.1}

**This is up to you as the moderator to determine.**

The whole point of having a moderator is to act as a filter, so you
don't get 20 copies of the origin of "foobar" all posted. In general,
you decide:

-   Which submissions are appropriate for the newsgroup,
-   What format to post them in,
-   What order to post things in,
-   Whether to edit the submissions,
-   How, or in what directions to steer the discussion.

For example: because of the very restrictive charter of
[news.announce.important](https://web.archive.org/web/20071021065408/news:news.announce.important),
submissions accepted and posted to the group should be articles that are
SO important that nearly everyone on Usenet should read them. For this
reason almost all postings are rejected. The moderator often suggests to
the submitter that the submission instead belongs in another group, such
as
[news.misc](https://web.archive.org/web/20071021065408/news:news.misc).

However, for most discussion newsgroups, you'll probably want to let
almost everything through; otherwise you can get a reputation as a
tyrant or censor. Most moderators try to help the author say what they
really meant; if the original submission isn't clear you can suggest
changes, or suggest a different place where it might belong. If you get
duplicates, pick the best one and post it, perhaps along with an
editorial note thanking A, B and C for their similar answer.

If you get a high noise/signal ratio, you can delete some of the noise
(like extra mail headers or signature lines). If the poster asks a
question that you know the answer to, it's common to post the question
and give the answer right there in an editorial note **[such notes are
generally in brackets, like this - MRH.]**

Other common editorial practices are to remove excessive quoted
material, and to reformat paragraphs to be under 80 columns per line.
(Some moderators return articles to the author for such reformatting,
though.)

If you want to have a lively discussion (or discussions) going, you
might group related notes (possibly into a digest) and pass almost
everything through. If your goal is to improve the quality of the
newsgroup (like
[rec.humor.funny](https://web.archive.org/web/20071021065408/news:rec.humor.funny)
does for
[rec.humor](https://web.archive.org/web/20071021065408/news:rec.humor))
you might be very selective.



### [17.2. Deciding a course of action](#17TOC){#17.2}

There are times when you may not know the best way to handle an issue or
policy. You cannot always be sure what the newsgroup's readership
actually wants to see happen. When a significant question or controversy
arises, you should consider running a survey of the readers to determine
the appropriate course of action. Surveys can be extremely useful, not
only for determining what people want to happen on a specific issue, but
for the other benefits they can provide:

-   Once it is documented what the readers want, it is much easier to
    explain to the malcontents why you need to reject their submissions.
-   Readers feel the moderator is listening, and allowing them to help
    improve the group.
-   Often you receive other comments that are not a part of the issue on
    the table that you find useful to incorporate into your group's
    moderation.



### [17.3. Commonly perceived problems with moderation](#17TOC){#17.3}

**Censorship** - People are afraid they won't be able to get their idea
out to the masses if the moderator doesn't like it. You are strongly
discouraged from ever telling someone *"I don't think this should be
posted to the net"* when you get a submission. It's almost always
possible to say *"toplevel.mygroup isn't the right place, have you
considered net.framus?"*

We should also emphasize that only the moderated groups are affected,
the unmoderated groups will still exist for those who want total freedom
and lower quality or higher volume. (Hopefully you'll be able to take
some of these high volume newsgroups and reduce their volume to a
manageable level, along with increased organization.) This is only true
for groups that are paralleled by unmoderated groups.

**Time delays** - When someone posts something to an unmoderated group,
most of the net sees it within two days. When submitted to a moderator,
you introduce a delay, and you submit to the net from a different place
which might introduce an additional delay. Depending on the nature of
your group, it may be very important that you process submissions
promptly. A lively discussion will die out if turnaround is worse than
about one day. On the other hand, groups such as comp.sources.* and
[rec.humor.funny](https://web.archive.org/web/20071021065408/news:rec.humor.funny)
probably can easily tolerate more delays. There have been moderators
who've gotten way behind on traffic; the result has been bad feelings
toward the moderator, and in extreme cases, a newsgroup that dies out.



### [17.4. Vocal minority](#17TOC){#17.4}

As moderator of a newsgroup, prepare to be flamed by a vocal minority.
Assuming you do your job reasonably well, most of the satisfied readers
will remain silent. Whether you deserve it or not, you will receive
annoyed criticism from readers typically of the form:

-   Why did you reject my article?
-   Who made you God?
-   How dare you get sick/go on vacation/neglect the newsgroup for your
    real life?

Remaining calm in the face of this sort of criticism is the best
defense. If there are actual facts under the heated rhetoric, address
those calmly and ignore the tone of the criticism. Apart from that, your
best defense is just to ignore the poster especially if the complainer
seems to be the only one whining. Resist the temptation to have the last
word in an argument, even if the argument is in public. Drawn out
bickering will only serve to undermine respect for you and your role.

It helps to have form letters to deal with some of these questions,
particularly the first two. [See Appendix B.] Keep the charter of the
newsgroup handy too.



### [17.5. Anonymous postings](#17TOC){#17.5}

On some newsgroups, the moderator will facilitate anonymous postings by
stripping identifying headers from submissions, if so requested. On
other newsgroups, the moderator requires that all submissions be from
identified accounts, going so far as to reject all postings submitted
through anonymous remailers. In choosing your policy, you should be
aware that even 'identified' accounts may have very little connection
to a real person. For all practical purposes, most user accounts on
large commercial network providers such as
[earthlink.com](https://web.archive.org/web/20071021065408/http://www.earthlink.com/)
and
[aol.com](https://web.archive.org/web/20071021065408/http://www.aol.com/)
are anonymous - the user chooses what, if any, identifying information
is visible.

No matter what policy you choose for your newsgroup, it should be
documented clearly in the group's periodic policy posting. It might
also be wise to let the group's readership decide the policy, by
holding a vote.

## [18. Answers to general questions](#18TOC){#18}

The following section is a frequently asked questions list with answers.
They are listed in no particular order.



### [18.1. How big is my group's readership ?](#18TOC){#18.1}

Use to be the best way to determine readership was via the newsgroup
reports that were posted monthly by Brian Reid <reid@pa.dec.com> to
[news.lists](https://web.archive.org/web/20071021065216/news:news.lists).
This is no longer supported. The real answer is **"Guess"**.



### [18.2. What mechanisms guard the group from unauthorized "Approved:" headers ?](#18TOC){#18.2}

None. The best process is for the moderator to read the group from
another site and cancel anything posted to his/her group by
'outsiders'. (You should try to do it from another site, in general,
because the type of person who posts their own stuff to a moderated
group frequently puts your "official" site in the Path: line in an
attempt to keep you from seeing the posting.)



### [18.3. Have any moderators gotten paid for what they do ?](#18TOC){#18.2}

Yes. Sometimes a moderator's employer understands the importance of
news moderation, and the effort involved in doing a good job, and allows
the employee to perform some moderation tasks during working hours, or
on the employer's equipment. This potentially gives the organization
greater visibility through an Organization: header or signature file in
the moderator's postings. While the moderator is not being directly
paid for moderation duties, their normal compensation covers time spent
working on the newsgroup.

The group
[comp.research.japan](https://web.archive.org/web/20071021065216/news:comp.research.japan)
received a grant from the U.S. Office of Naval Research to help support
the operation of the group. There have been other research oriented
groups that have received support, but to-date moderation is usually a
volunteer position with no compensation other than a grateful community.



### [18.4. Why are readers complaining of lost articles ?](#18TOC){#18.4}

A complaint a moderator hears from time to time concerns lost
submissions. There are several reasons for these complaints.

-   The reader is unaware of the group's moderated status

    The reader replies to an article or submits a new one and does not
    see it appear within minutes in the newsgroup they are reading, as
    is the case for unmoderated newsgroups.

    Solution: Advertise the moderation status in the newsgroup in the
    group's periodic posting.

    Solution: A somewhat more effective solution is to use a moderated
    newsgroup .signature file. That way, new readers will be much more
    likely to see it than even a weekly periodic posting.

-   Reader turnaround expectation time

    A reader may wish to see the article reviewed and posted even before
    the moderator gets to it.

    Total Turnaround time, barring unusual network problems, may be
    calculated as follows:

    **T = T1 + T2 + T3 + T4**

    T1 == Time for the submission to the forwarding site for the
    newsgroup from the site it is submitted [ 0.5 day ]

    T2 == Time for the submission to be processed at the forwarding site
    and transferred to moderator's email address [ 0.5 day ]

    T3 == The suggested turnaround time by the moderator [ X days ]

    T4 == Time a submission will take after posting at moderators site
    to propagate to the authors [ 1 day ]

    T = 2 days + X days. For example: If a moderator has a turn around
    time of 1 day, it can take up to 3 days for an article to re-appear
    at the submitter's site.

    Solution: Make the total expected turnaround time available. Readers
    will know to wait before complaining their articles are lost.
    Request they wait at least 'T' time before flagging their articles
    as lost.

-   Misconfigured local news software

    Readers may complain that they are posting/sending articles which
    the moderators never see. None of the articles from that site ever
    reach the moderator(s). It is possible the site was configured
    correctly and in an update to the software something went wrong and
    articles no longer reach the moderators.

    Solution: If all the previous options have been exhausted. Ask them
    to pursue the following:

    1.  Send a test submission. [if it fails continue on]
    2.  Talk to news@_user_site for an explanation.
    3.  Talk to usenet@_user_site if news@_user_site fails to reach
        a human being.
    4.  Talk to root@_user_site for mailer logs to check if the
        submissions are going out of the site.
    5.  In the meantime, request the reader to post through an alternate
        way by sending submissions to:
        -   Mail2News gateways. e.g., group-name@cs.utexas.edu,
            group-name-news@starbase.yale.edu
        -   email submission directly to the moderator's submission
            address

-   Reader continue to complain

    At this time, don't rule out the possibility of readers
    intentionally creating the problem make moderator(s) appear
    incompetent or to appear as 'victimized' by the moderators or any
    political agenda of their own.

    It is recommended, moderators be upright and honest and inform the
    readership of what is being down to track the lost articles.



### [18.5. Readers complain of articles being deleted after a day](#18TOC){#18.5}

Every system that runs the news software has its own set of article
expiration times set by its news administrator. The admin sets the
expiration period depending on how many groups they carry and how much
disk space is available. As a full news feed is over 100 MBytes a day
and rising, some groups are set to expire very rapidly. That is probably
what is happening to the articles your users are worried about. Most
news admins expire articles faster in groups they think are less
important, to make space for those they think really matter. For
example, some sites keep alt. groups only 1-2 days but keep the comp.*
groups much longer.

Tell the readers having the problem to talk to their local news admins.
Most will extend the life of a particular group their users say they
find important to them.

There is a way that you can indicate that your articles should not be
expired so quickly as the rest - the Expires: header. However, this
should not be used for normal articles as it is not reasonable to try to
override the local news admin's policy on how to use the limited disk
space on their systems. If your group has an FAQ or other regular
monthly information posting, though, you may like to use the Expires:
header on that article - look in
[news.answers](https://web.archive.org/web/20071021065216/news:news.answers)
for lots of [FAQ
articles](/web/20071021065216/http://www.landfield.com/faqs/), many of
which will have an Expires:

Note however that, partly because of misuse of the Expires: header in
the past, some systems no longer support it and expire all articles at
the same rate. The only real way your users can be sure of keeping the
articles long enough is for them to get the support of their local news
admin.

19. Passing the torch



The worst time for a moderator is when they realize that they can no
longer provide the time needed to keep their newsgroup responsive to the
submitters and the group's readership. It is hard to give up something
that has been enjoyed in the past and to admit to yourself that it is
time to move on. That time will come for all moderators at some point.
The best moderators are the ones that recognize it is time and then
tries to make the transition as easy for the new moderator as well as
the group in general.

When it is time, there are a few ways to proceed in finding a
replacement.

-   Post a message to your group or some other appropriate group
    requesting one or more volunteers to take over moderation duties. Be
    prepared for many responses coming back. Also be prepared for no
    responses coming back.
-   Directly offer the position to someone you feel would do a good job,
    such as your backup moderator, and then announce it as a done deal
    to the group.
-   Usenet moderators can post to the moderators mailing list and ask
    for a replacement.

Some have even resorted to a vote in the past but this is not
recommended as it is not a win/win situation for the moderator or the
group.

Once a replacement moderator is selected, inform the group of the change
in responsibility and introduce the new moderator to the group. It
should not be the new moderator's job to do a self introduction. You as
the departing moderator should do so. Also, take the time to thank those
who have helped you along the way.

If you are the moderator of a Usenet newsgroup you will need to follow
the procedures specified in the [Changing Moderators section of Appendix
A:](/web/20071021065646/http://www.landfield.com/usenet/moderators/handbook/appendixA.html#A.2)

20. Acknowledgments



Sections of the text in this document are based on and taken from
emailed responses that appeared on the moderators list and
moderators-advice mailing list. The following people contributed in that
fashion.

I would also like to thank the moderators-advice list for being patient
through the many revisions that they saw go by.

Finally, the author wishes to express his heartfelt thanks to

for help in writing and re-writing sections, reviewing the document,
answering my silly questions and for making the document's creation
much easier. **Thanks!**

## Appendices

### [Appendix A: Usenet Specific Newsgroup Moderation Information](#ATOC){#A}

For new Usenet newsgroups, draft charters and moderation policies should
be made clear in the Request For Discussion, and final versions should
be in the Call For Votes. The process of creating new Usenet newsgroups
is discussed in

["How To Create A New Usenet
Newsgroup"](https://web.archive.org/web/20071021065506/http://www.faqs.org/faqs/usenet/creating-newsgroups/part1/)

posted periodically to
[news.admin.misc](https://web.archive.org/web/20071021065506/news:news.admin.misc)
and
[news.answers](https://web.archive.org/web/20071021065506/news:news.answers).



#### [A.1. Discussion lists for Usenet moderators](#ATOC){#A.1}

Two mailing lists have been set up to facilitate communication between
moderators. They are described below. These lists are there for your
benefit. Use them. New moderators may feel worried about showing their
ignorance in front of the list of their new found peers. Don't! These
lists are there to help new Usenet moderators. Usenet moderators are
generally extremely helpful. Don't try to struggle through when a
simple request will make your new tasks easier.



##### [A.1.1. moderators-advice](#ATOC){#A.1.1}

The group 'moderators-advice' was formed from a volunteer group of
Usenet moderators in Fall of 1993. The goal of this group is to come up
with some practical general guidelines for moderated groups on Usenet,
in the form of a moderators' handbook (this FYI).

One of the goals of 'moderators-advice' group is to assist, guide and
answer questions for moderators of Usenet. To facilitate this process,
this document has been compiled. It is hoped that this document gives
basic information and general guidelines about the moderation process.

If you have general questions about the moderation process please send
them to moderators-advice prior to posting to the entire moderators
mailing list.



##### [A.1.2. moderators](#ATOC){#A.1.2}

A general discussion list for Usenet moderators is:

[moderators@isc.org](https://web.archive.org/web/20071021065506/mailto:moderators@isc.org)

All changes -- additions, address changes, deletions:

[moderators-request@isc.org](https://web.archive.org/web/20071021065506/mailto:moderators-request@isc.org)

The traffic on this mailing list varies. Most of the time it is low or
quiet, if some discussions starts, it may go up to several messages a
day. Almost all Usenet moderators subscribe to it.

Incoming Usenet moderators are normally added by default.



#### [A.2. Changing moderators](#ATOC){#A.2}

The official list of moderators is maintained by David Lawrence
<tale@isc.org>. The list is posted periodically to the newsgroups
[news.lists](https://web.archive.org/web/20071021065506/news:news.lists),
[news.groups](https://web.archive.org/web/20071021065506/news:news.groups)
and
[news.answers](https://web.archive.org/web/20071021065506/news:news.answers).
It is titled

["List of Moderators for
Usenet"](https://web.archive.org/web/20071021065506/http://www.faqs.org/faqs/moderator-list/part1/)

When a change occurs, the current moderator needs to send a message to:

[moderators-request@isc.org](https://web.archive.org/web/20071021065506/mailto:moderators-request@isc.org)

indicating the change to be made. The following information must be
supplied:

-   The name of the new moderator(s)
-   An address where requests and administrative info should be sent.
    Normally this address is "FOO-request" for submission address
    "FOO".
-   The address for submissions to the list. It is better if this is not
    the name of the newsgroup itself, but something similarly
    descriptive.

The message to initiate the change should only be sent when the old and
new moderators are ready to actually make the switch.

It is best if the new moderator also sends a message to the address
listed to say hello. This will help speed the change.

David will update the list and mail it out to all sites acting as Usenet
moderator mail forwarders.



#### [A.3. Usenet moderator replacement concerns](#ATOC){#A.3}

In the past, it has generally been decided (though not quite
unanimously) that a moderator may not be removed by the group's
readership. This topic is a recurring one on the moderators mailing list
where there are those who feel Usenet needs a way to remove moderators
who have quit supplying their services to a newsgroup or who are
otherwise not fulfilling their duties in a satisfactory manner. To date
there is no accepted process for removing a moderator.

When a moderator has not been posting for a very long time the
readership can get angry at the moderator and their inactivity. Members
of the readership have also become vocal when the moderator failed to
follow the charter of their group when selecting articles to post to it.
Whatever the reason, when this happens members of the group's
readership have flooded associated groups with "Off with their head!"
or "The moderator of 'your.group' is a worthless ... !" messages.
Things start to get ugly at this point.

Most moderators when confronted with this situation will try to find a
peaceful way out. It may be that a polite message posted to your group
explaining the reason such as "real work has gotten in the way and it
is temporary situation" will calm the troubled savages. The solution
may entail finding a co-moderator/backup to assist with the workload or
find a permanent replacement. Some moderators just ignore these types of
problems and continue as if the complainers do not exist.

The later approach does have problems that you should be fully aware of.
A rabid readership can't really knock you out of the moderator position
but they can damage your net.reputation with barrages of constant
complaints in unmoderated discussion groups relevant to the one you
moderate. You may end up spending time responding to messages when you
could be using that time to post to your group. In any case, be prepared
for a nasty situation if you chose to ignore the problem.

In the end, you must make your own decision on how to deal with the
problem. But please remember that your group is a net.resource to many
people and when it is not functioning smoothly, it is not useful.



#### [A.4. Group Charters](#ATOC){#A.4}

These are important! *Don't* lose 'em. They often come in very handy
when it's necessary to quote chapter and verse to a recalcitrant
loudmouth. And if you wish to make changes to it, make sure that you get
some sort of public consensus that the changes are reasonably
acceptable.

For recently created Usenet groups (since sometime in 1990), group
charters are available at

[ftp://ftp.uu.net/usenet/news.announce.newgroups/](https://web.archive.org/web/20071021065506/ftp://ftp.uu.net/usenet/news.announce.newgroups/)

They are archived by hierarchy and newsgroup name.



#### [A.5. Submitting articles through public Usenet Mail/News gateways.](#ATOC){#A.5}

If you do not have direct access to Usenet news, you can still moderate
a Usenet newsgroup. This can be done by submitting articles to the group
via electronic mail, instead of posting them directly to the group.
There are a several 'public' mail/News gateways. Each one has their
own ways for addressing syntax. The three most common ones are:

-   Site:
    [cs.utexas.edu](https://web.archive.org/web/20071021065506/file://cs.utexas.edu/)
    Syntax: newsgroup-name@cs.utexas.edu
    Example: To send to the newsgroup
    '[comp.compilers](https://web.archive.org/web/20071021065506/news:comp.compilers)',
    address the message to

    comp-compilers@cs.utexas.edu

-   Site:
    [newsbase.cs.yale.edu](https://web.archive.org/web/20071021065506/file://newsbase.cs.yale.edu/)
    Syntax: newsgroup.name-news@newsbase.cs.yale.edu
    Example: To send to the newsgroup
    '[comp.compilers](https://web.archive.org/web/20071021065506/news:comp.compilers)',
    address the message to

    comp.compilers-news@newsbase.cs.yale.edu

-   Site:
    [pa.dec.com](https://web.archive.org/web/20071021065506/file://pa.dec.com/)
    Syntax: newsgroup.usenet@pa.dec.com
    Example: To send to the newsgroup
    '[comp.compilers](https://web.archive.org/web/20071021065506/news:comp.compilers)',
    address the message to

    comp.compilers.usenet@pa.dec.com



#### [A.6. Usenet Moderated Newsgroup Archive List](#ATOC){#A.6}

This article, posted monthly in
[news.lists](https://web.archive.org/web/20071021065506/news:news.lists),
lists the location, maintainer and other general information about the
archives of moderated newsgroups. In most cases, the archives listed are
the location the moderators of the individual newsgroups consider
official. Those that are not considered official but are available are
marked with a **'**'** on the Newsgroup: line.

This is not an all encompassing list of archives for each group. Only
the archives that the moderators consider official or one recommended
archive for the newsgroup is listed. It is solely up to the moderator as
to which sites are to be listed. Updates to this listing will only be
allowed from the newsgroup's official moderator as listed in the
periodic posting titled

["List of Moderators for
Usenet"](https://web.archive.org/web/20071021065506/http://www.faqs.org/faqs/moderator-list/part1/)

maintained by tale@isc.org (David C Lawrence).

Moderators, to submit additions or changes, send email to:

[mod-archive-faq@landfield.com](https://web.archive.org/web/20071021065506/mailto:mod-archive-faq@landfield.com)

### [Appendix B: Canned Messages](#BTOC){#B}

All moderators get a certain amount of wildly off-topic submissions, and
it helps to have a form letter that you can send to clueless folks,
without having to take the time to figure out why they might have been
posting to your group, or where they should have sent their post, or
whether it was their brain or their software that erred.

Here are a few types of canned responses that you may want to have handy
to save you time and effort:

-   Read the FAQ, where the question you asked is answered.
-   Your message wasn't posted because it was similar to several other
    messages just posted, but thanks anyway.
-   Your question was answered by past messages, here's how to look in
    the archives.
-   You have been taken off the mailing list [if your group is two-way
    gatewayed to a BITNET list] because mail to you bounced. If your
    mail now works go ahead and resubscribe.
-   To subscribe or unsubscribe to the mailing list, send a message to
    blah.
-   Your message was cross-posted to other moderated newsgroups and the
    policy of this newsgroup is no cross-posting. It appeared on this
    one but no others.
-   Various responses pointing people at on-line resources.

When a spamming message is received, just throw it away with no response
at all, particularly if it was cross-posted to a bunch of equally
irrelevant groups. There is no reason to alert the spammer to the fact
that the message wasn't posted. If it seems like it might be useful,
send a polite note to **usenet@** or the **postmaster@** the spammer's
site.



#### [B.1. C News Duplicate headers message template](#BTOC){#B.1}

Dear postmaster/usenet administrator:

I am the moderator of <insert your group here>. I receive emailed
submissions for the group. As I get a lot of submissions, it can
sometimes be rather time consuming to get incoming articles ready for
posting. You appear to be running C News, which has the annoying habit
of inserting duplicate sets of headers when the transport software sends
the posting from your user to me. While a single posting like this
isn't a problem by itself, after the 100th or 1000th time it gets
rather tiresome, and it's *very* simple to fix.

Explanation: in C News, the newsbin/relay/injnews script is used by
inews to do site-specific header bashing. When it discovers that the
newsgroup is moderated, it invokes mail to send off the article to the
moderator (via mailpaths). Unlike B News and INN, where time has been
spent to configure how to use the mail transport directly (to merge the
news headers in with the mail headers), C News blindly punts the article
into "mail" which is a user agent, which often refuses to accept
"header-like" stuff at the beginning of a message as part of the RFC
822 header block. In essence, mail will often implicitly put a blank
line at the beginning of the message, so the headers carefully crafted
by injnews end up as part of the body instead of the mail headers.

The solution is simple - change injnews to call the mailer (usually the
transport) in such a way that injnews' headers are included in the mail
headers. In relaynews/injnews, there is the following line:

mail "$moderator" <$censart

Change it to call the mail transport directly. If you're using sendmail
or smail, simply change "mail" to be the full path. Eg:

/usr/lib/sendmail "$moderator" <$censart

Most other transports, such as MMDF or PP should be just as simple.
Please note that injnews is intended to be modified for local site
policy, so you won't be voiding your warranty ;-)

If you're not using sendmail or smail, or simply wish to test this, try
typing:

<your mail transport program <your address> Subject: it worked

hello

It should appear in your mailbox with Subject: properly recognized. If
the subject isn't recognized, then it didn't work, and "Subject: it
worked" will appear in the body.

If you have any questions, please don't hesitate to contact me. Thank
you for your time,



#### [B.2. Thanks for FAQ comments](#BTOC){#B.2}

Thank you for your comments on the <FAQ title here> FAQ. I'm updating
the FAQ now, and am including your corrections or additions as
appropriate. Expect to see them in the next posting.

<moderator's-fullname> <moderator's-email-address>



#### [B.3. Inappropriate submission](#BTOC){#B.3}

*(Begin form letter.)*

The message below was submitted by you to the moderator of <newsgroup>
either by posting a message to the group, or by sending E-mail to the
group's submission address, or by sending mail to the group's
administrative address.

Your message is not appropriate for posting to <newsgroup>.

<insert reason here>

<Description of your newsgroup here>

(End form letter.)

<moderator's-fullname>, Moderator of <newsgroup>



#### [B.4. Get a Clue](#BTOC){#B.4}

*(Begin form letter.)*

The message below was submitted by you to the moderator of <newsgroup>
either by posting a message to the group, or by sending E-mail to the
group's submission address, or by sending mail to the group's
administrative address.

Your message is not appropriate for posting to <newsgroup>.

<Description of your newsgroup here>

Unfortunately, I do not have the time to make specific suggestions as to
where your question or post should go but some ideas are included below.

If you are new to Usenet, you should probably read the posts in
[news.announce.newusers](https://web.archive.org/web/20071021025533/news:news.announce.newusers)
(n.a.n.) -- if they are not available in your newsreader, they also
available by anonymous FTP in
[rtfm.mit.edu:/pub/usenet/news.announce.newusers/](https://web.archive.org/web/20071021025533/file://rtfm.mit.edu//pub/usenet/news.announce.newusers/)*

A few that are most likely to be immediately helpful are:

-   [A_Primer_on_How_to_Work_With_the_Usenet_Community](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/usenet/primer/part1/)
-   [Answers_to_Frequently_Asked_Questions_about_Usenet](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/usenet/faq/part1/preamble.html)
-   [Emily_Postnews_Answers_Your_Questions_on_Netiquette](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/usenet/emily-postnews/part1/)
-   [Hints_on_writing_style_for_Usenet](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/usenet/writing-style/part1/)
-   [Introduction_to_the_*.answers_newsgroups](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/news-answers/introduction/preamble.html)
-   [Rules_for_posting_to_Usenet](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/usenet/posting-rules/part1/)
-   [What_is_Usenet?](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/usenet/what-is/part1/)

To find what groups are relevant for your question, you might scan
through your local list of newsgroups (your .newsrc file on most Unix
systems), to see which group names seem related. Then subscribe to those
groups, and look at some of the recent traffic, to make sure that your
question is suitable for the group. (For example, questions about
Microsoft Windows belong in
[comp.os.ms-windows](https://web.archive.org/web/20071021025533/news:comp.os.ms-windows).*,
not
[comp.windows](https://web.archive.org/web/20071021025533/news:comp.windows).*)

On some systems, you will be able to look at a file containing a
one-line description of the purpose of each newsgroup (the
'newsgroups' file), or at a longer description of the purpose and
contents of each newsgroup (the newsgroup charters.) Ask your local news
administrator if these resources are available on your system.

For widely-distributed newsgroups, you can also find the one-line
descriptions in the following n.a.n postings:

-   [List of Active Newsgroups, Part
    I](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/active-newsgroups/part1/)
-   [List of Active Newsgroups, Part
    II](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/active-newsgroups/part2/)
-   [Alternative Newsgroup Hierarchies, Part
    1](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/alt-hierarchies/part1/)
-   [Alternative Newsgroup Hierarchies, Part
    2](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/alt-hierarchies/part2/)
-   [Alternative Newsgroup Hierarchies, Part
    3](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/alt-hierarchies/part3/)
-   [Alternative Newsgroup Hierarchies, Part
    4](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/alt-hierarchies/part4/)

The 'List' posts describe newsgroups in the comp, misc, news, rec,
soc, sci, and talk hierarchies. The 'Alt' posts describe newsgroups in
the alt, bionet, bit, biz, clarinet, gnu, hepnet, ieee, inet, info, k12,
relcom, u3b, and vmsnet hierarchies. They will not describe groups that
are available only in your region or institution.

If these sources of information do not suggest some newsgroups which
might be appropriate for your questions, you may wish to post on the
newsgroup
[news.groups.questions](https://web.archive.org/web/20071021025533/news:news.groups.questions),
whose charter includes helping users find newsgroups appropriate for
their questions. Please consult the above-listed sources before posting
on
[news.groups.questions](https://web.archive.org/web/20071021025533/news:news.groups.questions),
however.

Very few sites carry all available newsgroups. Your local newsadmin can
help you access newsgroups that are not currently available, or explain
why certain groups are not available at your site. If your site does not
carry the newsgroup(s) where your post belongs, do NOT post it in other,
inappropriate groups.

Think very carefully before cross-posting to more than one, or perhaps
two, newsgroups. It is considered highly inappropriate to broadcast your
message to a wide selection of newsgroups merely to have more people
read it. Follow the general rules of Netiquette (Usenet etiquette)
described in the
[news.announce.newusers](https://web.archive.org/web/20071021025533/news:news.announce.newusers)
postings above.

Once you decide what newsgroup(s) are relevant to your question, make
sure that you're not asking questions that are frequently asked and
answered. In addition to looking at recent traffic in the group, check
whether your question is included in an FAQ (Frequently Asked/Answered
Questions) list. Most FAQs are archived at
[rtfm.mit.edu](https://web.archive.org/web/20071021025533/ftp://rtfm.mit.edu/pub/usenet/),
in directory /pub/usenet/your.group.name, if they're not available in
your newsreader in the specific group or in *.answers. Many groups also
have a periodic introductory post that describes the content and purpose
of the newsgroup - if one exists, you should read it before posting.

A listing of many of the periodical postings on Usenet can be found in
n.a.n. or its archives, as

[List of Periodic Informational Postings, Part
[1-20]](https://web.archive.org/web/20071021025533/http://www.faqs.org/faqs/periodic-postings/)

Following these suggestions will help not only to ensure that your post
reaches its intended audience, but to make Usenet more useful for all of
us.

(End form letter.)

<moderator's-fullname>, Moderator of <newsgroup>



#### [B.5. Test elsewhere](#BTOC){#B.5}

*(Begin form letter.)*

The message below was submitted by you to the moderator of <newsgroup>
either by posting a message to the group, or by sending E-mail to the
group's submission address, or by sending mail to the group's
administrative address.

The <newsgroup> is not an appropriate place to send test messages. If
you wish to post a test message, there are newsgroups for that purpose,
such as
[alt.test](https://web.archive.org/web/20071021025533/news:alt.test),
[misc.test](https://web.archive.org/web/20071021025533/news:misc.test),
and
[news.test](https://web.archive.org/web/20071021025533/news:news.test).
Messages sent to the *.test newsgroups are automatically acknowledged
by daemons running at many sites. If you want to test your site set up
for posting to a moderated group, post your test message to the group
[misc.test.moderated](https://web.archive.org/web/20071021025533/news:misc.test.moderated).

(End form letter.)

<moderator's-fullname>, Moderator of <newsgroup>

### Appendix C: Tributes

Any person who moderates a newsgroup for over 10 years should have it
documented somewhere so others can appreciate the effort and dedication.

Our first tribute goes to Gene Spafford <spaf@cs.purdue.edu>.

For 12 years between April 1981 until April 1993 Gene (spaf) maintained
and posted *THE* "Usenet periodic postings" to the net. The postings
included the

-   [A Primer on How to Work With the Usenet
    Community](https://web.archive.org/web/20071021065715/http://www.faqs.org/faqs/usenet/primer/part1/),
-   [Introduction to
    news.announce](https://web.archive.org/web/20071021065715/http://www.faqs.org/faqs/news-announce/introduction/part1/preamble.html),
-   [Answers to Frequently Asked Questions about
    Usenet](https://web.archive.org/web/20071021065715/http://www.faqs.org/faqs/usenet/faq/part1/),
-   [Rules for posting to
    Usenet](https://web.archive.org/web/20071021065715/http://www.faqs.org/faqs/usenet/posting-rules/part1/),
-   [Hints on writing style for
    Usenet](https://web.archive.org/web/20071021065715/http://www.faqs.org/faqs/usenet/writing-style/part1/),
-   [Usenet Software: History and
    Sources](https://web.archive.org/web/20071021065715/http://www.faqs.org/faqs/usenet/software/part1/),
-   [What is
    Usenet?](https://web.archive.org/web/20071021065715/http://www.faqs.org/faqs/usenet/what-is/part1/),
-   [How to Construct the Mailpaths
    File](https://web.archive.org/web/20071021065715/http://www.faqs.org/faqs/mailpaths/part1/),
-   [List of Active
    Newsgroups](https://web.archive.org/web/20071021065715/http://www.faqs.org/faqs/active-newsgroups/),
-   [List of Moderators for
    Usenet](https://web.archive.org/web/20071021065715/http://www.faqs.org/faqs/moderator-list/part1/),
-   inet Checkgroups,
-   non-inet Checkgroups,
-   and others.

He also managed the moderators mailing list during that time. The
moderator community and the net as a whole owe Spaf a debt of gratitude
for his dedication and BS&T. Thanks Spaf!

> "Usenet is like a herd of performing elephants with diarrhea --
massive, difficult to redirect, awe-inspiring, entertaining, and a
source of mind-boggling amounts of excrement when you least expect
it." --spaf
