---
layout: post
title:  "Experiments in Topic Modelling Nonius Marcellus"
date:   2021-03-09 6:51:21 -0500
categories: 
---

I worked with my sample set (the entries in Nonius Marcellus, Book IV, under Letter E) this week to try some basic topic modelling. I used the Topic Modelling Tool and the [Quickstart Guide](https://senderle.github.io/topic-modeling-tool/documentation/2017/01/06/quickstart.html) here. I should preface this that I have no clue really what topic modelling is even after reading Underwood's book and [blog](https://tedunderwood.com/2012/04/07/topic-modeling-made-just-simple-enough/). My basic steps:

* first, I split my cleaned plain text into 27 files by headword (so *eligere*, or *evadere*, e.g.). 
* next I made a metadata csv, but since all my files are from the same author, text, and volume, I added a category called "infinitive?" to see if maybe part of speech is relevant. 
* I ran these through the topic modelling tool a few times, doing 10, 5, 20 topics, and settling on 10. This was the stage I was most unsure about- the stopword list that the tool provides is in English, and I thought it might be more time and effort at this stage than it is worth to come up with my own Latin one. For future projects this will probably be necessary. At any rate, I don't know if the computer can...read...Latin? and so I also don't know how much variance I saw in these results, which I'll talk more about below.
* I tried a pivot table, but since my files are all from the same text and author, I wasn't getting anything too interesting.
* Finally, I created reference folders and files from texts in my larger repo. I started with Cicero's dialogues the *Cato Maior*, *Laelius*, and *De Republica*, and also tried Priscian.

# Results?

## Nonius 

For the Nonius topic models, I could not make sense of them no matter how many variations I ran. A big issue is likely that as a dictionary, with subheadings and examples cited from other authors, many of the topics were just uses of the headwords themsleves. 

### Sample topic generated:

"*exegit exanclari* quam *extulit* molestia *ecferri* inpunitatis pavor *exuat exuit* aestu siti asperque *exornabant* suam vivat subiectum breviter disserere vocat"

The italicized words are all headwords, and *quam* and *suam* should be stop words.

### Another topic generated:

"lib ii vergilius tullius de lucilius aeneidos est atque ut ad terentius iii evadere cum excipere plautus iv te georgicorum"

This topic is interesting, as it is almost all author names, titles of texts (and some stray references to book numbers), and what should be stopwords (de/est/atque/ut/ad/cum/te). This makes sense, since Nonius is mostly definitions and citations. But I don't need a tool to know that.


## Reference texts

### Cicero

Compared against Nonius, the topic modelling did a much better job with Cicero, possibly because his narratives are more straightforward. For example, of the first three topics,


0.	nec senectus senectutis senectute turn senectutem aetatis mortem senem senex aetate senes senibus vires diu corporis eum adulescentes viribus tamquam
1.	est ut cum qui esse ad sed quod de enim quae quam si aut 5 se etiam autem quidem sunt
2.	amicitia nec amicitiae turn om rell amicitiam amici amicitias amicorum amicis ge inter amicum quamobrem tarn amicos scaevola po1 lq

though 1 is made entirely of stopwords, the other two correspond to the texts subtitled *De Senectute* and *De Amicitia* pretty well. Compared to Cicero, we can guess that Nonius cites previous authors (Cicero included) explicitly more.

### Priscian

I tried Priscian because I thought that while Cicero was more canonical, it wasn't an even comparison. Since Priscian writes on grammar and uses citations in a similar way to Nonius I decided to give him a shot. 

This model came up with topics I likewise couldn't make sense of, just as with Nonius. The authors were more spaced out in these topics rather than bunched together in one in Nonius. 

# Conclusion

I don't really have any. I had no issues running the tool, but coming up with meaningful results is another story. I wonder if increasing my sample and text size from individual entry to all entries under one letter would help. Having a list of stopwords definitely would-- but unless I make every headword a stopword, which will create a problem when a headword is used in the citation or definition of an unrelated headword, will this result in topics dominated by the headword? I also wonder about finding an adequate referent. Since Nonius is writing, well, using citations of Republican Latin, any Republican text like Cicero might cause issues, since Cicero is a topic of Nonius'. 

ETA: I didn't know how to spell Modeling, went with a double L, and lost

