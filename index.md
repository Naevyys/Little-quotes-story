---
title: Little Quotes Story
layout: default
---

{% capture site-title %}
  {{ page.title | default: site.title }}
{% endcapture %}

{% capture site-description %}
  {{ page.description | default: site.description }}
{% endcapture %}

<!-- Missing image sources -->
{% include banner.html
  title=site-title
  image_url="assets/images/donkey-elephant.jpg"
  description=site-description
  isHeader=true
%}

If you follow US news, you’ve noticed that right-leaning news outlets talk about Donald Trump more positively than left-leaning ones. We were interested in determining if this translated into right-leaning news outlets selecting more positive quotes from Donald Trump.

{% include plots/0_2.html %}

There seems to be a difference, let’s investigate if this applies to all Republicans and Democrats!

We would therefore like to generalize this observation to answer the following questions:
-	**Is there a difference in the way left and right-leaning news outlets quote people?**
-	More generally, **what is the quoting style of different groups of news outlets?**

To answer these questions, we will use Quotebank, a repository of 175 Million quotes collected from a wide variety of English-speaking news outlets.

<!-- {% include plots/0_1.html %} -->

{% include banner.html
  title="Evolution of Quoting Style"
  image_url="assets/images/apolitics_word_clouds.jpg"
  description="Analysis of the evolution of quoting style over the years 2015 to 2020."
%}

[Intro]

<!-- [Biases in our data. Do we want to use a [dedicated page](/biases) for them?] -->

{% include plots/1.1.html %}

Here we show the distribution of mean quote length per outlet per year. We see that apart from a few outliers, it stays between 18 and 22 words. The mean quote length for all news outlets increased from 20 to 21 words between 2015 and 2020.

{% include plots/1.2.html %}

This shows that news outlets have on average slightly positive quotes (polarity score >0). However this positivity has been following a negative trend between 2015 and 2020.

**Interestingly, there seems be two distinct populations, one below the average (0.07 to 0.11) and another above it (0.125 to 0.16). Could these groups correspond to news outlets of different political orientations?**

Next, we divided the news outlets in three groups based on their political orientation : Left-leaning, Right-leaning and Neutral (no difference is made within a group, meaning no degrees of left or right). **This should allow us to determine if the 2 populations we observed correspond to the political leaning of the news outlet.**

{% include plots/1.3.html %}

Right-leaning news outlets have a higher mean quote length than left-leaning ones for all years. Between 2016 and 2020, the difference between left and right-leaning news outlets' mean quote length stays constant at about 1.3 word.

Furthermore, they both follow the same evolution as the average mean quote length. This suggests the increase of quote length in news outlets is a general pattern which is independant political orientation.

**This graph seems to support the idea of different quoting style between left-leaning and right-leaning news outlets. Let's do the same with polarity score and see if our theory holds.**

{% include plots/1.4.html %}

Left-leaning news outlets's quotes are more positive than right-leaning news outlets across all years. Left-leaning news outlets's positivity increased between 2015 and 2020, while right-leaning news outlets stayed more or less constant. Neutral news outlets changed the most, their quote mean polarity score decreased from 0.15 to 0.11.

**We don't see left-leaning on one side of the mean and right-leaning on the other as we had hypothesized. However, there is still a notable difference in the polarity score of left and right-leaning news outlets, which supports our thesis for different quoting styles between right and left-leaning news outlets.**

# Conclusion

This yearly analysis of quoting style has yielded several inputs. 
Between 2015 and 2020, quotes have on average been getting longer (20.2 to 21.2 words), are generally positive but are getting less positive (0.128 to 0.116 polarity score).

**Looking at differences in the quoting styles of left and right-leaning news sources, we found that left-leaning news outlets have on average shorter and more positive quotes than right-leaning outlets.**

{% include banner.html
  title="Quoting style according to political orientation"
  image_url="assets/images/republicans_word_clouds.jpg"
  description="Analysis of the quoting style according to the political orientation of news outlets and of the speakers they quote."
%}

**Dwelving deeper into this difference in quoting habits, we were interested in assessing if left/right-leaning news sources quote Democrat and Republican speakers differently. For example, would left-leaning news outlets quote Democratic speakers more (more and longer quotes) and more positively?**

For this analysis we decided to focus only on the most quoted Democrats and Republicans within the previously selected news outlets. Find out more about the selection process in our notebook.

{% include plots/2_1.html %}

Surprisingly, quotes from Democratic and Republican speakers are very closely distributed between the different news outlets. There is only a bit more of the quotes from Democratic speakers in left-leaning news oulets, and a bit more of the quotes from Republican speakers in right-leaning news oulets (about 1%).

**It seems like there is not much difference in how much websites of different political leaning quote Democratic or Republican speakers. Let's see if instead there is one in the way they quote !**

{% include plots/2_2.html %}

This plot shows that speakers affiliated to the Democratic party have on average longer quotes than speakers affiliated to the Republican party (by 1-2 words), in neutral, left, and right-leaning news outlets. 

Furthermore, and in accordance to our previous results, we find that there is a difference in mean quoting length between left-leaning, neutral and right-leaning news outlets, with left leaning outlets using shorter quotes and right leaning outlets using longer ones.

**Democrat speakers have longer quotes than Republicans, independent of the leaning of the news outlet. Let's now look at the quote positivity.**

{% include plots/2_3.html %}

First, left-leaning news outlet quote Democrats more positively than Republicans, and right-leaning news outlets quote Republicans more positively than Democrats. **Therefore we observe the expected pattern where news outlets quote the speakers from their own political orientation more positively those from the opposite one.**

Second, Democratic speaker are quoted more positively in left-leaning news outlets than in right-leaning news outlets and Republican speakers are quoted more positively in right-leaning news-outlets than in left-leaning news outlets. **More surprisingly, neutral news outlets quote more positively than politicized news outlets, for both Republican and Democratic speakers. This indicates that a more negative quoting style is associated with politicized news outlets.**

Third, we observed that the polarity score of the most quoted speakers belonging to any of the two main US parties is lower than mean polarity score for all speakers found in the first part of the analysis. 

**Therefore we've found that politically oriented top speakers are quoted more negatively on average than either less quoted political speakers or apolitical speakers. Let's look into this more, are apolitical speakers quoted more positively, or could it be that the top speakers are actually quoted more negatively than less quoted speakers?**

{% include plots/2_4.html %}

Following our discovery that the top political speakers had less positive quotes than the average, we decided to compare quotes from top democrat, republican and apolitical speakers. 
We observe that top apolitical speakers have almost 3 times the polarity score of top Democratic or Republican speakers.

**Therefore we indeed have this pattern where, amongst the top speakers, apolitical speakers' quotes are 3x more positive !**

We also see that on average, the top speakers (here) have more positive quotes than standard speakers (previous analysis).

**Here we must reject our hypothesis that top speakers are on average quoted more negatively than less quoted speakers. It seems that low positivity of top political speakers is more than compensated by the high positivity of top apolitical speakers.**

# Conclusion

**Democrat and Republican quotes are simiarly distributed amongst news outlets of different political leaning. Democrats have longer quotes in all of them. News outlets quote the speakers from their own political orientation more positively those from the opposite one. FInally, we've seen that politicised news outlets and politicised speakers both lead to generally more negative quotes. It looks like politics is just more negative overall...**

{% include banner.html
  title="Quoting style according to news source factual reporting"
  image_url="assets/images/democrats_word_clouds.jpg"
  description="Analysis of the quoting style of news outlet depending on their factual reporting score."
%}

**We've observed a quoting style difference between left and right-leaning news outlets. However this division according to political leaning does not explain all the quoting style variation. Therefore we decided to group news outlets according to a new parameter: their factual reporting rating. Our hypothesis is that news outlets with higher factual reporting would keep longer and more neutral (less positive) quotes. We are also interested in determining whether neutral website have higher factual reporting than politicized news outlets.**

Among the websites we are assessing, the factual reporting rating ranges from mixed to high.

{% include plots/3_1.html %}

Mixed and high factual reporting have mean quote length around 21 words, whereas mostly factual new outlets have a mean quote length of 18 words.

*We do not have our hypothesised linked increase of quote length and factual reporting.*

{% include plots/3_2.html %}

Once again we have mixed and high factual reporting quite close together at around 0.069 and news outlets with mostly factual reporting at 0.066.

**Therefore quote positivity does not follow factual reporting in a linear fashion**

{% include plots/3.3.html %}

Here we've separated our news outlet political leaning value with subvalues of left/right, differentiating between left/left-center and right/right-center. All center and extreme values were merged.

We see that very political websites have a lower factual reporting, and that neutral and left/right-center are indiscernable.

**It looks like going from neutral to a moderate political leaning does not impact the factual rating of news sources. However, having a very clear left/right political leaning is associated with a significantly lower factual reporting rating.**

# Conclusion

**From what we've just seen, it doesn't look like variations in factual reporting and quoting style are really linked, or at least not in a linear way. However, we did confirm that very politicised websites have lower factual reporting than neutral or moderatly politicised one.**

{% include banner.html
  title="Principal component analysis"
  image_url="assets/images/merged_word_clouds.jpg"
  description="It's time to let our data shine by itself!"
%}

[PCA here]

{% include banner.html
  title="Sources"
  image_url="assets/images/boxing-gloves.jpg"
  description="Insert description here"
%}

The data used for our analysis originates from the dataset [Quotebank](https://drive.google.com/drive/u/0/folders/1R-GVIdxU3jkQb5zU0uG9044Vynh9nYR1) for the years 2015 to 2020. Information on the speakers was extracted from [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page). Scores for factual reporting and political leaning of news outlets were taken from [Media Bias Check](https://mediabiasfactcheck.com/). The banner word clouds were generated with our speaker data using [this website](https://classic.wordclouds.com/).
