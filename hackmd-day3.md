---
permalink: /hackmd-day3/
---

#  2020 November, Focus CoE instructor training days 3

## Links

- Course page: https://coderefinery.github.io/2020-11-02-instructor-training/
- Schedule:https://coderefinery.github.io/2020-11-02-instructor-training/#schedule

###### tags: `workshop`


Outline and slides: https://psteinb.github.io/hpccarpentry-mini-intro/

- introduction to hpc carpentry: https://psteinb.github.io/hpccarpentry-mini-intro/slides-hpccarpentry.html#/title-slide

* [HPC Carpentry](https://github.com/hpc-carpentry)
* Target audience: skilled scientists, novice HPC
  * Have never used shared system
* Means lots of new jargon for them
* Working on communcation between instructors and learners
  * Manage expectations on both sides
* There is always diversity and no recipe to solve this
* HPC Carpentry repos are at:
  - [hpc-carpentry/hpc-intro](https://github.com/hpc-carpentry/hpc-intro) (very active repo)
  - [hpc-carpentry/hpc-shell](https://github.com/hpc-carpentry/hpc-shell) (some activity)
  - [hpc-carpentry/hpc-python](https://github.com/hpc-carpentry/hpc-python) (no activity)
  - [hpc-carpentry/hpc-chapel](https://github.com/hpc-carpentry/hpc-chapel) (legacy repo)
* Lesson repo can contain configuration for multiple sites simultaneously
* Fitting in
  * Archer2: https://www.archer2.ac.uk/training/courses/
* Questions and comments:
  * Good that we can maintain something central and still maintain the site customisations
  * What is HPC experience?
    * No coding in the intro lesson, mostly mechanics of using an HPC system
  * What about the Chapel material, is that usable?
    * Not actively maintained right now
    * Is Chapel the best vehicle? (That's a tough question anyway because everyone has an opinion)
  * Why the "HPC" moniker when this applies to other areas?
    * That's a fair comment, but the idea is to remove the "fear" when HPC is mentioned


### Break until 02:00pm

### Devising Material Overview

- Slide deck on lesson design: https://psteinb.github.io/hpccarpentry-mini-intro/slides-lessondesign.html#/title-slide

* Details and further reading: [Greg Wilson, Teaching Tech Together, 2019, CRC Press](https://teachtogether.tech/en/index.html#)
* Use pre-workshop surveys to ensure the learners match the learner profiles
* Formulation of learning objectives 
  + [Bloom's Taxonomy](https://teachtogether.tech/en/index.html#ref-Ande2001)
  + [Fink’s Taxonomy](https://teachtogether.tech/en/index.html#ref-Fink2013)
  + Use the taxonomies when defining our learning objectives!
* Hard to get prerequisites right
  * Having other eyes on your material helps do this better
* Lesson design:
  * Backwards design covered last week
    * Bottom-up approach
  * Constructive Alignment
    * Learning objectives -> learning activities -> assessment and feedback ... (and then repeat)
    * More top down approach
  * Both are iterative!

### Break until 02:55pm

### Learning Objectives 1

(Exercise for all, groups of 2, 10 minutes plus 10 to compare)

Formulating Learning Objectives can be hard. We introduced [Bloom's Taxonomy](https://teachtogether.tech/en/index.html#ref-Ande2001) in the presentation. This exercise is for you to exercise this.

Before you start this exercise, give yourself a rating (5 stars = you will complete this exercise with ease, 1 star = you will struggle with this exercise and likely not complete it). Write this rating down here (with writing this down, you signal us that you want to participate):

- `4 X ***`, `2 X **`, `2 X *`


Join up in pairs and formulate one sentence for each of the taxonomy categories (typical verbs to use are listed in brackets at the end of each bullet).

> ## Bloom's Taxonomy

> - **Remembering:** Exhibit memory of previously learned material by recalling facts, terms, basic concepts, and answers. (recognize, list, describe, name, find) 

 * ssh: name the command and list it's parameters
 * scp: Name the basic structure of a scp call: `command source destination` 
 * ssh: Can the student explain what does the `ssh` acronym stand for?

> - **Understanding:** Demonstrate understanding of facts and ideas by organizing, comparing, translating, interpreting, giving descriptions, and stating main ideas. (interpret, summarize, paraphrase, classify, explain) 

 * ssh: explain what the command does
 * scp: Paraphrase the similarity of SCP to CP - across physical limits of computers.

> - **Applying:** Solve new problems by applying acquired knowledge, facts, techniques and rules in a different way. (build, identify, use, plan, select) 

 * ssh: use the command to log in to a new cluster / server
 * scp: Build : - Use SCP to transfer a set of files or folders 

> - **Analyzing:** Examine and break information into parts by identifying motives or causes; make inferences and find evidence to support generalizations. (compare, contrast, simplify) 

 * ssh: compare the local environment to the remote environment (to contrast source and destination machine)
 * scp: Compare : compare to rsync and ability to know when to to use which (simplify this!)

> - **Evaluating:** Present and defend opinions by making judgments about information, validity of ideas, or quality of work based on a set of criteria. (check, choose, critique, prove, rate) 

 * scp: Rate approaches to share scientific data (cloud versus shared folder on parallel filesystem versus central [ftp] server)
 * ssh: choose whether to use ssh to do a given task

> - **Creating:** Compile information together in a different way by combining elements in a new pattern or proposing alternative solutions. (design, construct, improve, adapt, maximize, solve) 

* ssh: solve a security problem using ssh
* scp: Design an approach to share scientific data to more than 3 destinations (on a daily basis).
* ssh: Can the student modify the following ssh command to be able to log-in directly into the directory /home/dir1?: ssh username@login.hpc.xxx.xx.uk

As an example, choose one of the following topics:
- `ssh`
- `scp`
- any single command from the HPC domain that you could teach

At the end of this exercise, each pair should have at least 6 sentences available - one for each of the categories above.



Room3
Q1: << Is the student able to recognize the various `ssh` related commands? >> 
[Remember] 
Q2: << Can the student explain what does the `ssh` acronym stand for?>>
[Understand] 
Q3: << Can the student use the prior knowledge on `ssh` commands to access Archer facilities?>>
[Apply] 
Q4: << Is the student able to break down the following command `ssh -X -l username login.hpc.xxx.xx.uk` ?>> 
[Analyze] 
Q5: << Choose which of the following sentence is correct:
a. `ssh username@login.hpc.xxx.xx.uk` 
b. `ssh login.hpc.xxxx.xx.uk@username` 
[evaluating]
Q6: << can the student modify the following ssh command to be able to log-in directly into the directory /home/dir1?:
ssh username@login.hpc.xxx.xx.uk>> 
[creating]

## Lesson development within focusCOE

slides by Alan O'Cais: https://psteinb.github.io/hpccarpentry-mini-intro/slides-focuscoe.html#/title-slide
  - challenge: grasp learner profile to motivate entire content and relate the two 

### Break until 04:05pm

### Breakout session

* Assuming 3 breakout rooms, possible episodes are:
  * [01-why-bother-with-performance](https://fzj-jsc.github.io/tuning_lammps/01-why-bother-with-performance/index.html)
  * [02-hardware-performance](https://fzj-jsc.github.io/tuning_lammps/02-hardware-performance/index.html)
  * [03-benchmark-and-scaling](https://fzj-jsc.github.io/tuning_lammps/03-benchmark-and-scaling/index.html)

* Are the objectives of the episode clear?
  * Are they reflected in the episode content?
* Is the content clear?
  * If there are metaphors, are they clear? Can you suggest improvements?
  * Are the examples clear?
    - Can they be done in a reasonable amount of time?
    - Are there potential pitfalls?
    - Are they motivating?
  * Is something missing?


**Room 1**
[01-why-bother-with-performance](https://fzj-jsc.github.io/tuning_lammps/01-why-bother-with-performance/index.html)

Objectives:
- `Understand the link between software performance and hardware` this is quite general. The lesson for me focusses on `Understand the link between software performance and hardware on a job submission level` on holistic level, i.e. take LAMPPS as is and work with the job submission etc.
- `Identify the different methods of enhancing performance` the material falls short of this in my view (profilers are missing and all the HPC machinery); I'd propose to tailor it more, e.g. `Identify the different methods of enhancing efficient and effective use of available resources`

Metaphors:
- `Say you are the chef in a restaurant and every dish that you do is perfect. You would be able to ...` rather tricky to deduce the metaphor from the text - it would be more helpful to have a figure or an image
- The metaphors here seems to explain, when you have more chefs they can cater a large crowed. Can the same quality be dilivered. Do you use the same menu for a 7 course meal and large crowd. I would rather use something like a delivery bussness or postal service. More people invloved more deliveries can be completed at a given time. 
- The chefs metaphor. First impression: "ugh, so much text!" Second impression: "yeah! useful metaphor!" -> suggest to replace by image and shorter text.

Examples:
- `Calculate CPU hours` is a very general (if not detached exercise); it might be worth considering to have a central exercise/demo to use in the exercises
- How about adding a discussion exercise which plots compute time as a function of number of cores and/or nodes and the group discusses:
  - 1) what number of cores they would choose
  - 2) how they could obtain this plot for their problem/application/job
- check the use of `simple` or `just` (see e.g. https://github.com/FZJ-JSC/tuning_lammps/pull/42)

What is missing:
- The memory aspect. This page seems to only focus on the CPU part of the question. Sometimes we scale to more cores not only to get more CPU but also to get more memory.
- The resource choices also affect queue time. In my experience some users don't really care so much whether the run takes 1 day or 2 days but they care a lot more about how long it queues.
- It seems time to solution is central to this episode but time to solution is not only runtime but queue time + runtime so it might be good to comment on what parameters may affect queue time.

description of walltime and CPU Hours are confusing, it may make sense to get rid of CPU Hours ?

**Room 2**

[02-hardware-performance](https://fzj-jsc.github.io/tuning_lammps/02-hardware-performance/index.html)

* Are the objectives of the episode clear?
  * Are they reflected in the episode content?

    * Need to define objectives
    * What question does the first section address?
    * The first question is vague. I'm not sure the content adresses it. Same goes for the third question
    * The second question is addressed clearly.

* Is the content clear?
  * If there are metaphors, are they clear? Can you suggest improvements?
    * Seems dry without examples
    * Lots of very dense text in the lesson
  * Are the examples clear?
    - Can they be done in a reasonable amount of time?
    - Are there potential pitfalls?
    - Are they motivating?
  * Is something missing?



## Lesson Portability

slidedeck: https://psteinb.github.io/hpccarpentry-mini-intro/slides-portability.html#/title-slide


# Feedback

## designing a parallel coding lesson

- people think they would need between 3-4 h and more than 10h (majority
- to prepare, people think they need min 21-26h up to more than 70h

## after this course, do you require more or less time to prepare

(Mostly require more)

## general feedback: what we need to improve? something that you didn't understand?

- some parts on the coderefinery is unclear, why we discuss the general part on `https://hpc-carpentry.github.io/hpc-intro/` ?  It's unclear why we should use the templates presented today (even if very helpful)  
- more examples for code teaching, particularly using smart tools 

## general feedback: what you liked? something that you did understand?

- a lot of material to use as homework and expand
- pre-material reading
- material to use

---
*always ask questions right above this line*

