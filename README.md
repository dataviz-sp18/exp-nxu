
Assignment 2: Experimenting with visual design (20 points)
==========================================================

For this assignment, you need to create, design, implement, and analyze an experiment testing some principle or rule of visual design. Look to the readings from our units on ["Design and evaluation"](../notes/day3-notes.html) or ["Science, art, or somewhere inbetween"](../notes/day5-notes.html) for inspiration. Your experiment should be implemented a la Cleveland and McGill/Heer and Bostock using Amazon MTurk to obtain research participants.

Key requirements for the assignment:

-   You must run an experiment. There must be a randomization component so that you can accurately draw conclusions about causality from the data, and you must have actual results to discuss.
-   It must test a principle of visual design. It does not have to be publication-worthy in size and scope, but there should be a clearly developed question, hypothesis, data/methods, results, and conclusion to it. The write-up will probably take 3-5 pages of text and graphs.
-   It should be reproducible. The analysis of your results should be conducted using programming and a script or R Markdown-style document. Data files should be stored in your repo and accessible.
-   It should be ethical. As a class assignment, this does not require IRB approval. However only collect and analyze demographic or personally-identifiable data if there is a specific purpose for it. If you have any questions about this, **you must speak with me before collecting the data**.

Researchers at the University of Rochester have developed [an excellent guide](http://amandapogue.github.io/Qualtrics_Tutorial/) for running basic cognitive experiments using [Amazon Mechanical Turk](https://www.mturk.com/mturk/welcome) and [Qualtrics](https://sscs.uchicago.edu/page/qualtrics). You are strongly encouraged to mimic this approach, but if you have experience running experiments feel free to utilize a different approach. I expect your analysis to likely be conducted in R, but you can use Python or an alternative software package if you desire.

Setting up accounts
-------------------

-   Setup your [Amazon MTurk account](https://www.mturk.com/mturk/welcome)
-   Setup your [Qualtrics account here](https://sscs.uchicago.edu/page/qualtrics)
    -   **DO THIS EARLY**
    -   You need to first create an account on Qualtrics, then email <ssc-server-support@lists.uchicago.edu> acknowledging that you are using Qualtrics for the class.

Working in a team
-----------------

You may work with up to two other students in the course if you choose. When you create the repo for the assignment, be sure to create a team so that the other team members have read/write access to the repo.

Grading
-------

Grading will be flexible. I will not grade you on whether you find significant or insignificant results. You do need to actually run the experiment in order to receive credit. I'm looking for the following things:

-   Is the question relevant to visual design?
-   Can the experimental design accurately answer the question?
-   Were the results generated accurately?
-   Is the analysis accurate?

Submission details
------------------

[Create your assignment repo through GitHub Classrooms.](https://classroom.github.com/g/WtfroPll) Submit your analysis as a single R Markdown document rendered using the `github_document` output format.[1] The repo should also contain a copy of the generated data file and documentation of the survey and the treatment/condition versions of your graphic.

Your submission is due by **11:00am on Tuesday, May 1st**.

[1] Use `html_document` if needed to properly render your graphs.
