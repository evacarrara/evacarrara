---
layout: post
title:  "Cicero and Vergil as Fragments?"
date:   2021-04-18 2:00:00 -0500
categories: 
---

Alternate title: or how visualization and turning Nonius into (moderately, for a classicist) big data can pay off.

So last week I promised I'd post more about Nonius' citation of Cicero and Vergil. As the most frequently cited authors by Nonius in Book 4, it just makes sense to look at their data in isolation. Below I'll post a few visualizations and some discussion of each, and then I wrap up on the topic of "where do we go from here?" For info on how I used RStudio and ggplot to get here, see last week's blurb on method, or check out the .tsvs in my [repo](https://github.com/evacarrara/republatfrags/tree/main/Tabular%20Nonius).



## Vergil

![img1](/evacarrara/assets/vplotb.jpg)

As mentioned last week, Vergil is Nonius' favorite author to cite in Book 4...by a long shot. And of Vergil's works, the Aeneid is far and away his favorite to cite in terms of characters, just about doubling the sum of citations of the Georgics and the Eclogues (known here as the Bucolici, which Nonius calls them). As for his citation of the Aeneid, check out these two similar yet different visualizations:

![img2](/evacarrara/assets/vplotf.jpg) ![img3](/evacarrara/assets/vplotf1.jpg)

So here we can see that while general character length of citation remains the same across all twelve books of the poem, the number of times he cites Book 1 are disproportionate to the whole (and the last two books seem comparatively under-cited). Character length is what we might expect to see, given that from what I can tell (as a non-Nonian scholar!) he generally cites whole lines (or two) of hexameter, whereas the various period lengths of prose allow for more variation. But the question of why some books are cited more than others, if not an error in the data, is open.

## Cicero

Cicero, the second most cited author, is a more mixed bag. First of all, look how many *different* works Nonius cites:

![img4](/evacarrara/assets/cplota.jpg) ![img5](/evacarrara/assets/cplotb1.jpg)

Even given this variance, the *De Officiis* comes out way on top. But something I think pretty weird is happening here too- Nonius cites Cicero both as 'Cicero' and as 'M. Tullius', with the latter the far more common way of reference. Since my dissertation deals with Cicero's naming practice, it's pretty interesting to see the tables turned here. Moreover, Cicero seems the preferred way of citation for some works (the Tusculan Disputations, De Or, and the Catilinarians)-- is this Nonius' choice, or is he just repeating the way Cicero is cited in his sources? 

Finally, here is a look at how Nonius cites Cicero according to headword, or rather, according to the alphabetic structure of his own work. We can see that our boy Cic shows up a lot more under words beginning with C than at H. A better viz for the future will be one that shows the proportion of Cicero (and/or Vergil) citations for each letter.

![img6](/evacarrara/assets/cplotb.jpg)


## the Data Potential of the Project

While none of this may be totally earth shattering research, as someone who works on fragments saved by Nonius, it's interesting to think about Vergil and Cicero here as intentional fragments. What would our idea of Vergil's Aeneid look like if, like so many lost works, we had a much larger and clearer window into only the prefatory or introductory material, Book 1? If we lost a lot of the Italian half of the poem? And for Cicero, whom we often introduce to students as a political blowhard through his speeches, how does he look if we have fewer than 10 citations from the Catilinarians? 

And so as I'm reaching a pausing point in this project, having manipulated and repurposed one full volume of Lindsay's three, I want to ask what was, and can be, gained from these methods and approaches. For Nonius specifically, it's the wider, distant reading of authors that *appear* so well-known to us that has been illuminating to me. Like Ted Underwood does for the modern English 'canon' in *Distant Horizons*, methods like these are not fool-proof, but it does open a view I hadn't seen, and pose questions I hadn't thought to ask. And though many of these larger scale observations on Nonius' citation method have been noted before, using computational methods allows us to double check the (sometimes tedious) work of scholars who noticed these trends analog-ly a century ago.

For me as a scholar and curious human, the potential outweighs the pitfalls, especially since, if well documented, the pitfalls can be studied, known, and avoided. I'm not so worried about the doomsday scenario when humanities jobs will be consumed by data analysts, mathmeticians, and machines, but I do think that the realities of academia right now lend themselves to learning and using these methods. Knowing how to efficiently tabularize your data, or how to update and criticize a text meant to be machine-read, are basically just new tools of textual criticism. As many important and useful projects within the umbrella of 'Classics' show, Greek epigraphy doesn't have to be pitted against TEI XML-- we need people who can do, or who at least have working knowledge of, both. Though this project isn't a direct part of my dissertation, I've incorporated some of the methods and big picture questions into my more traditional work. 

Like Catherine D'Ignazio and Lauren Klein write in [*Data Feminism*](https://data-feminism.mitpress.mit.edu/), "The work of data science, like all work in the world, is the work of many hands. Data feminism makes this labor visible so that it can be recognized and valued." On a personal level, I think one of the biggest benefits to these methods has to do with labor and visibility. As an active union member in a right to work state, and as a low-paid graduate assistant, I constantly struggle with the genius complex of academia- the idea of the individual who works long hours, is brilliant with languages, theory, and writing, is always grinding, hustling, who has their great idea just hit them one day in the shower (and who will one day merit a tenure track job)- that's not me, and I suspect it's not most of us. The reproducible methods and collaborative nature of these sorts of computational projects can help with transparency and accountability. I didn't choose to go to graduate school to spend all my 'free' time trying to publish in a pay-walled journal, but I do want to make a contribution, however brief and however small, to our knowledge of the past. Don't get me wrong; I'm not naive about big data being a magic cure-all. But there is something to be said for just...posting your work online. Sharing with others. Visualizing topics in new and interesting ways. And in this respect, trying out computational methods has been really freeing while at the same time frustrating; I'm not sure yet another field in which we expect people to just *have* competence (or one in which we reward those who overstate their competence) is what Classics, or humanities in general, needs. In this light, in making public all the messy steps it takes to get there, I hope to add to a growing body of people and scholars willing to try, to mess up, to collaborate. 