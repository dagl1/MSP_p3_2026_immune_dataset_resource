# MSP_p3_2026_immune_dataset_resource
Git repository for MSP 2025/2026 p3 project for finding, summarizing, and curating immune omics datasets

## Table of contents
- [Project overview](#project-overview)
  - [The goal](#the-goal)
  - [A general checklist](#a-general-checklist)
  - [Data handling (optional)](#data-handling-optional)
- [Report/presentation](#final-report-and-presentation)
  - [Report](#report)
    - [What should it include](#what-should-the-report-include)
    - [Writing tips](#writing-tips)
    - [Feedback](#report-feedback)
  - [Presentation](#presentation)
    - [Organising the presentation](#organising-the-presentation)
    - [Presentation tips](#presentation-tips)
- [Problems](#problems)

## Project overview
The original description of the project:

The immune system is essential to human health, and its dysfunction is cause and symptom of many diseases, yet despite this foundational role it is often overlooked and relevant data underused. Many tissues suffer immune-cell invasion as part of the inflammatory response, leading to tissue biopsies being “contaminated” by immune cells, as well as many blood-based methods implicitly measuring immune function. This data can be explored and investigated through a myriad of methods; The Systems Biology department (MaCSBio2) is keen to utilize pathway analysis and metabolic modelling to elucidate differences between samples on the immune level, but lack curated datasets to do so. 

Therefore in this project students will dive into literature to identify datasets of interest, become proficient in evaluating RNA-seq data, and if time/skill allows perform various computational quality checks. In doing so the students will gain first-hand experience in an important aspect of research, namely data acquisition and its critical evaluation. Even students mainly interested in wet-lab will find that validating their results or explaining novel insights often requires the ability to correctly and systematically assess datasets from various publications and appraise their methodological and academic value. 

To successfully perform these tasks, students will learn about different RNA-sequencing methods and the various normalization schemes which are often employed. During the project the aim is to find datasets that could be used to explore immune function or its effects and summarise these systematically, thereby creating a valuable resource for querying the immune system. This resource will set the standard for the department in terms of curating and collecting datasets for similar and other topics. 

### The goal 
The goal of the project is to identify papers that have interesting (human) data, specifically RNA-sequencing (next-generation preferably, microarrays are not particularly interesting in general), and/or Proteomics, as well as Metabolomics.
Large sample sizes, matched data, interesting interventions, or large coverage in their tissues or disease-phenotypes are key. Personally my work focusses on metabolic modeling, so tissues or datasets related to metabolicly-relevant phenotypes are going to very interesting; but datasets that have samples from every tissue in people of different ages, with blood-based metabolimics and some oxygen measurements could also be very interesting. Identifying the study procedure, data availability, important limitations, or potential use cases will be key in this project. This requires an understanding of the available methodologies, and if you are interested in programming, cleaning and downloading the data. I currently do not have specific goals for 
such data, but once collated and presented neatly, a new analysis might just come up that wasn't possible (or even considered) before seeing the availability of the data.

Some specifics that could help you focus on a particular topic: datasets of tissue biopsies relevant to metabolic disease. Think for instance insulin resistance in liver, fat, or muscle tissue (these tissues are obviously affected by decreased glucose-metabolism, which we could easily model). Contrast this to something like epilepsy where the main focus might be differences in overall connections within the brain, something that (at least at first glance) is not really metabolically relevant.

Related to immunology, spleen and lymph nodes (as well as blood-based measures) will have many of the cytokine producing cells, and thus biopsies of these tissues, especially in studies where there is dysregulated hormone/cytokine homeostasis.

Diseases of interest are (but not limited to) those that are known to affect metabolism, such as Hemochromatosis, but potentially also just anemia (this appears to affect iron metabolism in heart tissues, which might be difficult to come by in a biopsy sense).
Metabolic nonalcoholic fatty liver disease datasets are also interesting targets, as they have clear metabolic implications.

Besides an interesting (disease) population, tissue, and good study protocol, a study becomes increasingly worthwhile to look into if it has large sample size, or measures many additional things (blood based measures, or transcriptomics/proteomics of multiple tissues per participant).

Then finally, any study that includes matched proteomic and transcriptomic data would be amazing for one of my main projects (matched here meaning things like: 
https://www.embopress.org/doi/full/10.15252/msb.20188513 which right now is the input of this cool paper, but they (and thus I too) could do much more interesting things were we to have like 1000 samples worth of matched data: 
https://link.springer.com/article/10.1186/s13040-025-00434-z 

These are just examples of things you could focus on, but anything goes really. If you instead find some datasets with which to compare long non-coding RNA in an interesting disease, that is cool too. 

### A general checklist
Not an exhaustive checklist, but something to start the evaluation process (please expand this list as you see fit):
 - What was the study protocol (study groups, type of intervention, time-series or not) 
  - What data did they collect (RNA, proteomics, metabolomics)
    - What sample size for each type of data, are the data matched?
    - What type of samples were there?
    - What exact method did they use (e.g. illumina sequencing, paired end or single end;
    isobaric Mass spec, or LFQ/ibaq mass spec)
    - Is the data available, in what form (e.g. csv file, with gene symbols, or ensembl identifiers) is it?
    - Is the data already normalised?
    - What is the quality of the data, what is the quality of the study as a whole?
  - Any interesting conclusions drawn from the study?
  - What could this be used for?
  - What still needs to be done to make this useful in case some parts are not available or normalised

### Data handling (optional)
In case you want to perform more computational analyses or implementations, the following points would always be useful:
  - Apply the same normalisation (for RNA-seq GeTMM), for all types of data, batch correct with COMBAT
  - Attempt to transfer to ensembl IDs from other genes
  - Do some quality checks (at your own discretion)
Additionally things like applying read-alignment, or running Maxquant (for proteomics) could be of interest in case the data
isn't available in easily-readable formats.

## Final report and presentation
While the work you will do, and the documentation, will be super useful for research
purposes, you will also need to summarise your work and present it to MSP. As they might
not be as interested in the exact details, especially for the presentation the goal
would be to communicate what you have done, and what impact this work will have. For the
report I think having that in there is important too, but here you would also be able to
(in summary) discuss what work you have done, what is still open, and the challenges or
future outlook there is in this work. There are a lot of peptides, and the insulin task
took me a very long time to work out - while it is true that parts are reusable - I would
think you will not have finished all of them at the end. Therefore, I will most likely
let other students coming after you read your report. It would thus be nice if it
includes the things that went well, and which things could go better or which require
extra focus.

### Report
#### What should the report include
This will be quite dependent on what the final focus will be and approach you took. 
Of course, it should always aim at explaining what the scope of the work, the why, 
the what, and then shortly introducing the how. I think we can discuss a proper setup
in the future during the project, as things will have taken shape at that point.

#### Writing-tips
Academic writing, writing well, and writing very well is a difficult skill to learn.
Writing nice prose is something that is difficult, and which should necessarily be your
aim. Instead your aim should be - in order - be specific, be clear, be concise, write
in a nice manner. 

To be specific means to read what you write and **try** to misinterpret it. Things that
happen commonly is the referring to a particular concept, while meaning something
slightly different. It very often is clear what you *mean*, but what you wrote is not
what you meant. Another common problem in being specific, is the switching of topics
halfway through a paragraph, while not explicitly saying so. 

To be clear, remember to keep the amount of not-explained information to a minimum. When
you discuss a new term, quickly resolve any type of uncertainty. Readers have trouble
keeping many things in memory, so if you are going to discuss a new topic X, don't first
discuss all the ways it can be used, how people think about it, and then explain what
X actually is. It is difficult to properly contextualise the arguments you are
providing, if the reader doesn't yet know what X is. Keep the flow of information
limited and try to organise paragraphs together. Additionally remember to string
together topics in a way where one paragraph feels like it leads into the next. And if
it really doesn't, then adress that. Make sure the reader gets the feeling you are aware
of this abrupt change (you could use a sentence like "Viewed from an entirely different
perspective, one might also ..."). 

For writing concise, write your arguments. Then attempt to reduce unnecessary
information or merge sentences together (this is thus on an information level 
where you might be able to get the same point across, without needing both points);
afterwards you go through it and attempt to reduce the amount of words. Certain ways of
saying things are naturally more wordy than others. Think of: "On the other hand" vs
"Alternatively".

For writing well/nice, tips on the actual wording are difficult. What is important is to
make sure that the reader is taken along in the story, that there is some type of
cadence in the rhytm of your sentences and a paragraphs. Don't have too many super short
paragraphs, don't have too many very long paragraphs. Similarly for sentences,
alternate, try to imagine the reader and how they are feeling (potentially saying the
text out loud in their head) while reading your text. Think of natural pauses, and make
sure that you don't repeat yourself in ways that give the feeling you forgot about the
fact you wrote it before. 

This last point is a common occurence: you might have
discussed topic X in a part, then later you reintroduce the topic as if it is the first
time. Such occurences will feel odd and discordant to your readers. It might indicate
that you didn't reread your story, but moreover it indicates that either before it
wasn't necessary to explain, you didn't believe in your explanation from before (which
then means you wasted the readers time), or you might believe the reader forgot (making
assumptions about your reader). If you do want to harkon back to something, you can
always say: "as discussed earlier, topic X plays an important role in ... the current
results further point to such a role".

I recommend using a citation manager (I personally use Zotero, but any is fine) to add
citations to your document. This is especially nice when you need to use a referencing
style that uses numbers in text: you don't want to have to change the order of all the 
citations because you add or remove single reference. Citations managers will do this 
for you automatically. Similarly, if you need to change referencing style, the manager 
will do so for you automatically. I do realise it might not work that well when writing
a shared document, but as your BTR period follows directly after this, tip might be
useful there even if you can't use it in a shared google docs.

#### Report feedback
I am somewhat stringent on what I consider good writing - note that I do not mean the
style, there are many things I like do not like, but I acknowledge that much better
writers than me use other styles. Instead I am not particularly forgiving on vague or
incorrect statements (even if I could interpret it in a lenient manner and get what you
are trying to say). My assessment of your report will be done in part to provide you
with feedback that I believe will be useful, and thus I will assess you (at least
related to the feedback you receive, less so the grade) as if you are experts. Good
writing is not dependent on where you are in your academic journey; of course, in
grading I will take into account you are Bachelor students. Nevertheless, I will gladly
provide (a lot) of feedback on your reports if you provide me a draft (which I will
check and provide feedback on within 2 working days). It might then also be nice to have
a meeting to discuss the exact comments.

If you follow this route, and implement changes based on the feedback, then you of
course will be graded well. I will also give an (approximate) grade I would give to any
draft. This sometimes, together with potentially a lot of feedback, can feel very
negative: it is not, these are learning oppertunities, and generally we learn best
through mistakes. 

On rereading, I feel the above makes it sound as if I am going to put a red cross
through your draft, rip it in half, and tell you to do it all over. I assure you that
won't be the case, I have however noticed that in general the feedback you receive by
other tutors is typically tailored to your current level, and as such it might feel
overwhelming to get my feedback. Of course we first have to see, it definitely could be
the case that I say "wow nice work, here are some small pointers"!

### Presentation
With the presentation I think you can go a lot of different ways, although in all cases
the important point will be to focus on communicating the what, the why, and the how.
Other students might not care that much about what exactly you found, although an
overview or visual representation will be nice. What they will care about is
understanding what you did, how that might be useful, what difficulties there were, and
how you overcame them. What will the future hold, how did you document your work, and
provide them with a feeling of understanding on why this was valuable.

#### Organising the presentation
I think here you can do almost whatever, I would just make sure that just like in
writing, the audience is taken by the hand in understanding what is happening. Leave out
unnecessary details, instead make sure that they conceptually feel like they get what
you did. A general structure with intro, methods, results, discussion, might not be as
relevant - we should check what the rubric is, and what requirements there are to the
overal structure.

You should think of questions people might ask: "oh so you just did a literature
review" or "could you not just use available pathways from wikipathways". Make sure to
get before those in your presenation, that way you don't sound defensive, instead making
the audience feel you understand the scope of what you did, and why that is useful. What
it was, and what it wasn't. 
Other questinos you might want to just think an answer to, in case they will be asked
(generally it is easy to think of some common questions, an exercise that is worthwhile
to pursue regardless when making a presentation, as it might point out specific
weaknesses in your story/flow that you can fix already).

#### Presentation-tips
A presentation should feel like a concise story, that is well laid out, and that is
presented with confidence. The audience needs to get the feeling that you fully
understand everything about it. Don't make it sound like more or less than you did, be
honest and believe in the value of your work (if you make it sound bigger than it is,
then that implies you feel the value isn't big enough on its own). 

Don't read from slides, don't read from text, preferably don't even have full text
memorised. Try to instead think of a story in your head, think of what the slide needs
to look like for that story, then during the presenation just tell that story. Of cours
you can (and possibly should) rehearse, but rehearsing and memorising aren't the same.
Don't have too much text on your slides, don't make it too fancy, have clear images, and
most importantly, do not repeat your slides except in special circumstances. This last
part happens a lot in student presentations: a slide names several important processes
involved in something, and the student will (without adding anyting) name them all in
order. Sometimes you can't avoid it, but in most cases you could either add extra text,
or mention something like: "it is involved in several processes, which you can see on
screen, the most important ones are x and y".

I personally think that students spent too much time on making presentations look fancy
instead of just neat. I do admit that many people seem to like colours or creativity in
the presentations they observe, however if that takes seven hours, which could have been
spent on improving the logic or flow of the presentation, I personally doubt its
wortwhileness. Neat looking presentations generally have the same information at the
same location (titles always exactly at the same location at the same font size; text
and images generally having designated locations; if using animations, using the same
general order where they appear (if you go left to right once, keep doing that for all
slides)). This helps with keeping people focussed, as they know where to look and
somewhat what to expect. This then also gives you the ability to conciuosly break this
rhytm to make a point or to point something out. Be conscientious with your story
telling!

## Problems
I very much hope that there will be no problems during the project, neither between your
collaborative effort, nor with my supervision. For the latter, there is always the
possibility to involve my supervisors (the two people also listed for the project), and
of course discuss things with me. 
For interpersonal problems between you (someone not doing anything, a fight, or anything
else), please contact me (preferably after talking between each other) and I can help to
mediate or see if anything is up. Don't wait till the peer-review stage to come with
accusations or comments. Giving and receiving criticism is difficult and uncomfortable
(generally moreso for the receiving part), however it is an important part of working
together, and in many cases one can do so in a civil manner. Neverthelss my office (PHS1
B3.007)is almost always open, and you can always contact me through email or just walk
by! 
