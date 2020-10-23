---
toc: true
layout: post
comments: true
description: A description of my first real team experience in a Zindi competition with Ronny, a friend of mine.
categories: [blog, competitions, zindi]
title: My first real team experience in a Zindi competition
image: /images/zindi-nlpx/nlpx.PNG
---

I love competitions, especially in data science. After getting started with machine learning, competing on Kaggle and Zindi became one of my favourite hobbies. But between the lack of time, computing resource and experience, I ended my first challenges closer to the bottom of the private leaderboard. Finally, I decided to listen to one excellent advice often given to people starting on Kaggle. I think it was something like this:
" To win, you need good ensembles; good ensembles are diverse. To get diverse ensembles, you need a good team."
Based on this advice, I became more open to working in a team. I did, for a Zindi competition and it worked: me and my friend finished [7th](https://zindi.africa/competitions/basic-needs-basic-rights-kenya-tech4mentalhealth/leaderboard) which is better than I did in any previous competition. No cash (yet) but a lot of learning.

## The team

My first real team experience was in a team of two, with Ronny Polle. If you don't know him, he's a medical student who likes researching challenging machine learning problems. I met him at the Deep Learning Indaba 2019 in Nairobi. For the [Basic Needs Basic Rights - Tech4MentalHealth competition](https://zindi.africa/competitions/basic-needs-basic-rights-kenya-tech4mentalhealth), we formed a team of two. The task consisted of classifying statements from Kenyan university students in terms of the mental health challenges they struggle with.


Overall the experience was quite pleasing and very different from working alone. The aspect I liked the most, apart from the obvious boost on the leaderboard, was the process when coming up with new ideas. A big part of scoring well on such competitions is coming up with new ideas fast and experimenting them. Unfortunately, generating new ideas after seeing the past twenty fail is not always an easy thing to do. When you are not alone, the burden of generating ideas is shared. Even better, your ideas bounce off each other to form even more ideas. So many that it eventually becomes hard to evaluate them all, which was not facilitated by the platform. On Zindi, the daily submission limitations are the same for both teams and individuals, meaning that each individual in a team can make fewer submissions than an individual working solo. These limitations can become frustrating before you even realize it. Despite the pains of having rigid restrictions in terms of submissions, the overall experience was a positive one.

## The learning experience

### What I learned concerning machine learning
In terms of machine learning, the main thing I learned during this competition is how important cross-validation is. In general, accurately evaluating your models is primordial. Without a proper way of determining the performance of your model, you won't be able to compare them, and know what is working and what is not. 
Apart from that, the challenge helped me confirm a few things:
* pretraining is important
* when the dataset is small, bigger models do not always help
* most of the performance boost comes from tuning hyperparameters
The few points mentioned above can seem evident for some, but the quality of the execution of those simple things is what makes a real difference.

### What I learned concerning data science competitions
Relative to competitions, what I learned comes down to this:
* "Seed every seedable": Zindi will drop you mercilessly if your code does not reproduce the results of your best CSV file, and rightly so. To avoid reproducibility issues, set a fixed value for every random seed that comes to mind. I wish we knew that earlier as the score of our best CSV file is better than the final best score on the private leaderboard.
* Keep every notebook: you can never really tell which notebook or code will give you your best score, so keep every single code file.
* Experiment ideas in quantity and quality: any method cannot truly be ruled out until we see it fail on the leaderboard, even then, big [shake-ups](https://www.theclickreader.com/how-we-lost-30000-on-a-kaggle-competition-2020/) are a thing. Trying as many ideas as possible, then testing them with cross-validation and the leaderboard is the way to go. 

## The results

In the end, I was quite satisfied with the results. Teaming up helped me get my first top 10 spot in a data science competition by finishing 7th. I also learned a lot with regards to both machine learning and competitive data science in particular. 
I didn't talk a lot about the final submission, because it was quite basic and was not anything innovative or interesting. The model used was a pre-trained RoBertA model with training and predictions made using 8-fold cross-validation. You can find it on GitHub [here](https://github.com/DrCod/Zindi-Tech4MentalHealth-NLP-Challenge)