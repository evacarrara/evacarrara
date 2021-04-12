---
layout: post
title:  "Visualizing Nonius"
date:   2021-04-12 12:30:00 -0500
categories: 
---


This week, I want to share some visualizations of the last week's tabular data. On my [repository](https://github.com/evacarrara/republatfrags), you can find plain text files of Nonius, their metadata, Book 4 tabularized, and the updated (more heavily regularized versions) of the tables used for visualization. Ideally I would use all of Nonius, but I'm still hammering out my methods- something my code reflects. And Book 4 is roughly equivalent in pages to Books 1-3 and Books 5-20, so it's not a *small* amount of text to work with. And so below I basically want to do some guided exploration of how visualizations can help make clear the many different dimensions of an author like Nonius, but also how some...sort of fall flat. Later in the week I'll post about his citation of Cicero and Vergil, but for now we'll look at the whole picture of Book 4. 


### a Note on Method

Using my .tsv from last week, I began messing around in RStudio with ggplot to see what sorts of things visualizations could tell me. The .tsv has been updated and cleaned a bit [more](https://github.com/evacarrara/republatfrags/blob/main/Tabular%20Nonius/nonm_bk4_4_11.tsv). In addition to cluster and editing and fixing errors, two new columns have been added: "headwordregularized", which goes further in subsuming all inflected variants under one headword, and "letter", which groups headword by first letter under which they are cited. My code will be available on my repo soon, and I'll edit this post then to reflect that. The tsv itself is in a 'tidy' format; each new 'observation' could have conceivably been a headword, but since I'm interested in how, when, and who Nonius cites, I made each obs. a citation, or what he quotes for each author. 

I spent more time than I'd care to admit trying to figure out dplyr's method of data transformation, and ended up using OpenRefine to filter out Vergil and Cicero. I was able to use dplyr to count rows and filter columns by count, but that was about it. A work in progress. Feel free to use my work, but please credit me (I'll get around to adding some official looking copyright stuff soon.) Also, this should go without saying but *lector (coder?) intende*: this is a work in progress, a learning experience, and done by a perpetual beginner- there's a ton of errors and things that could be better.


## Visualizing the whole Nonius

The following is a good place to start, though it is a bit basic, it makes clear who Nonius (and likely his sources also) cites the most. Note that Cicero and M. Tullius are two separate entries: more on that next week.

![img1](/evacarrara/assets/plotd32.jpg)

From this, we can tell that Nonius cites Vergil way more than the next two most frequent names in Book 4, Cicero and Lucilius. But this doesn't explain much about how or when he cites them. For that, check out the next viz that incorporates Nonius' structure into the mix:

![img2](/evacarrara/assets/plotg4.jpg)

Here we can see the pretty remarkable consistency with which Nonius cites, and some interesting patterns- Cicero seems to be cited more often under words beginning with 'C', whereas 'S' leans heavily into Vergil. For a different look at the same data, see this plot:

![img3](/evacarrara/assets/plotg3.jpg)

Below is a histogram that plots the length of citation (in characters) to the number of citations. I wanted to see if there was some 'sweet spot' and it does seem that around 50 or so characters is it, though see my previous post for caveats about the error built into this category until the text is perfectly cleaned. The lovely rainbow color show again the consistency across headwords.

![img4](/evacarrara/assets/plote1.jpg)

Finally, for an example of a viz that doesn't work so well, check out this plot made by faceting the authors out, but using the same standard of measurements. Though this isn't super aesthetically pleasing, it does a good job of putting Vergil's dominance into context. Some of the less frequently cited authors (like Sallust or Accius) are still cited fairly consistently across the alphabet, while others (like Sisenna or Ennius) have gaps between citations. Given what we know about Nonius' working methods, this might have something to do with the compendia he works from. 


As you can see, I like using R to plot- to me, it is easier than a program like Tableau, since I can control (and repeat) the code myself. This means that my plots aren't nearly as 'nice' as they looked when I tried a small sample in Tableau, but the scholarly conscience in me knows it's better to know the methods well, even if it's not as fancy. Plotting in general opens up new methods for interpretation I didn't quite notice before, even considering how much I've been working closely with Nonius. Since my diss focuses on Cicero's citation of historians, it's pretty interesting to zoom out and consider Cicero as 'fragmentary'- that is, someone who is cut up and quoted by a later author. How different would our idea of him look based on Nonius alone? I'll try to think about these and some other questions through visualization next week. 