# It's Not You, It's The Algorithm
*What 500,000 reviews and 60,000 dating profiles reveal about modern love, questionable decisions, and why Hinge thinks it's better than everyone else — analysed by someone with absolutely no business judging anyone's dating life and yet*


---

## The Hook

Look. This project exists because dating apps are a $9 billion industry 
built entirely on the gap between what people say they want and what they 
actually do at 2 am on a Tuesday. Tinder democratised the swipe. Bumble 
gave women the first move. Hinge declared itself "designed to be deleted" 
with the confidence of someone who has never been left on read for eleven 
days. And somewhere in the middle of all this, 200 million people a month 
are trying to find something real in an interface optimised for engagement, 
not connection.

It also exists because I have lived enough of the single girl experience 
to have opinions. The kind that come from situationships, talking stages, 
and going on dates purely for the plot. The kind that comes from knowing, 
deeply and personally, that the path to finding something real is rarely 
a straight line and almost always involves at least one person who 
definitely wasn't worth the talking stage. And then, occasionally, against 
all available evidence and personal history, someone comes along who is 
just annoying enough to make you question everything you thought you knew 
about dating apps. Anyway. Here we are.

The algorithm didn't make us like this. We showed up this way. Someone 
had to ask the hard questions. It might as well be the girl who figured 
it out the long way round.

---

## What Makes This Different

- Did Hinge actually earn its "designed to be deleted" rebrand, or was it just really good therapy-speak?
- Why does every app have a completely different personality but the same one-star review?
- What are people actually saying when they're frustrated enough to open the app store and type?
- Can you look at 60,000 real dating profiles and figure out who everyone actually is — not who they're claiming to be?
- Does writing more mean wanting more — or is "casual" just doing a lot of heavy lifting at this point?

---

## Key Findings

1. **Hinge scored 0.23 VADER sentiment. Tinder scored 0.12.** Nearly double, with five times fewer reviews. Hinge quietly won the reputation war and didn't even make a big deal about it. Very on brand for an app that spent years telling everyone it was designed to be deleted.

2. **Tinder has trust issues, Bumble has a spending problem, and Hinge is just trying its best.** Three apps spent years carefully crafting three completely distinct personalities. One is the original. One is the feminist one. One is the emotionally intelligent one that definitely went to therapy. All three of them, with remarkable consistency, found ways to make their users feel insane for trying.

3. **Every app's sentiment dropped together in late 2020.** Correlation isn't causation, but a global pandemic absolutely is. The algorithm was fine. We were not fine. We downloaded TikTok instead and called it coping.

4. **The Commitment-Phobe wrote 107 words across their entire dating profile.** Ten essay prompts asking them to describe themselves and what they're looking for — and they looked at all ten and chose violence. The algorithm tried its best. They will absolutely still message you first.

5. **People who said they wanted something casual wrote 607 words about themselves.** That is not the word count of someone who isn't bothered. Casual is doing a lot of heavy lifting in these bios.

6. **Short kings, this one's for you.** Height correlated with literally everything else at 0.00. Not low. Not weak. Zero. For one brief moment in San Francisco history, being 5'7" was statistically irrelevant. This finding would not survive a 2026 Hinge dataset and we all know it. Cherish it.

---

## What A Dating App Product Team Should Do With This

**Trust & Safety —** Tinder's fake profile complaint rate didn't decline over five years — it flatlined. That's not a problem being managed, that's a problem being tolerated. Proactive detection before the review gets written beats reactive response after the user has already left and taken their one star with them.

**Monetisation —** Bumble's pricing complaints went from 15% to 40% of negative reviews between 2017 and 2021. The signal was there in 2018. When four out of ten frustrated users are specifically frustrated about money, adding another premium tier is not the answer. Fixing the value perception is.

**Product —** Hinge users love it because it feels different. Every feature decision should be tested against one question: does this make Hinge feel more like itself, or more like Tinder? The loyalty data suggests users notice when the answer is the wrong one. Quickly.

**Growth —** Five distinct user archetypes exist with measurably different behaviours. Arrange Marriage Material writes 1,325 words and fills 8.88 essays. The Commitment-Phobe writes 107 and fills 5.19. Growth campaigns that treat these as the same acquisition target are leaving significant segmentation value on the table — and probably also matching the wrong people together, but that's a separate problem.

---

## Project Structure
```
It-s-Not-You-It-s-The-Algorithm/
│
├── its_not_you_analysis.ipynb          # Full annotated notebook
│
├── chart1_reputation_trajectory.png    # Sentiment trajectory 2017–2021
├── chart1_reputation_trajectory.html   # Interactive version
├── chart2_pain_points.png              # Trust vs monetisation complaints
├── chart2_pain_points.html             # Interactive version
├── chart3_loyalty_signal.png           # Word frequency by rating per app
├── chart3_loyalty_signal.html          # Interactive version
├── chart4_dating_personas.png          # K-means persona clustering
├── chart4_dating_personas.html         # Interactive version
├── chart5_self_presentation.png        # Intent vs effort bubble chart
├── chart5_self_presentation.html       # Interactive version
├── chart6_compatibility_matrix.png     # Correlation heatmap
└── chart6_compatibility_matrix.html    # Interactive version
```


---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core analysis |
| pandas + NumPy | Data cleaning and manipulation |
| NLTK + VADER | Sentiment analysis on 500,000+ reviews and 60,000 essays |
| Plotly | Interactive charts |
| Seaborn | Statistical visualisation |
| scikit-learn | K-means clustering and feature scaling |
| collections | Word frequency analysis |

---

## Data Sources

**[Dating App Reviews 2017–2022](https://www.kaggle.com/datasets/sidharthkriplani/datingappreviews)**
681,994 Google Play reviews of Tinder, Bumble and Hinge. Chosen because 
review text captures what users say when they're frustrated enough to open 
the app store and type. The star rating is the temperature. The text is 
the story. And occasionally the text is unhinged in the most useful 
possible way.

**[OkCupid Profiles](https://www.kaggle.com/datasets/andrewmvd/okcupid-profiles)**
59,946 profiles from San Francisco, June 2012. Ten free-text essays, 
demographics, lifestyle data. Chosen because it's one of the only public 
datasets that captures what people write about themselves when they're 
trying to be attractive — not complaining, not reviewing, just hoping. 
The 2012 San Francisco context means it skews educated and pre-swipe-era. 
Worth noting. Worth studying anyway.

---

## What I Learned

The biggest surprise wasn't in the charts — it was between the star ratings 
and the VADER scores. The rating split was almost exactly even. But VADER 
reading the actual language found significantly more positivity than the 
numbers suggested. People write more generously than they rate. A three-star 
review often reads like a four-star one. The number is the complaint. 
The text is the hope. That gap changed how I approached everything that 
followed.

The trust and safety finding caught me off guard. Hinge launched with the 
cleanest metrics of all three apps — and then grew fast enough that the 
bad actors followed. Fake profiles go where the users are, always on 
schedule. The spike recovered by 2021, which means someone noticed and 
actually did something about it. That's more interesting than Tinder's 
flatline. A flatline means nobody tried.

The persona clustering was the most fun I've had with data. Five clusters 
felt like the most honest number — distinct enough to tell different stories, 
few enough to name without a legend. The Commitment-Phobe was not planned. 
It fell out of the data entirely. 10,586 people opened a dating profile, 
looked at ten essay prompts, wrote 107 words total, and called it done. 
The algorithm tried its best. Some people simply are not ready and will 
absolutely still message you first.

The OkCupid data is a 2012 San Francisco time capsule and the analysis 
treats it that way. Height correlating at 0.00 with everything would not 
survive a modern dataset where height filters exist and "6ft or swipe left" 
is a whole personality. What it offers instead is a portrait of dating app 
behaviour before photo-first swiping changed the rules — and that portrait 
is, against all odds, stubbornly optimistic. People tried. They wrote the 
essays. They showed up. The Commitment-Phobe aside.

---

## About

**Trupthi Raj** 

[GitHub](https://github.com/trupthiraj) · 
[Tableau](https://public.tableau.com/app/profile/trupthi.raj/vizzes)
