# Data Visualization Project - Udacity Data Analyst Nanodegree

## Summary
This is a data visualization project for the Udacity Data Analyst Nanodegree.
Data was collected from the [CDC Wonder Database](https://wonder.cdc.gov/), and
then cleaned up in the data_manip.ipynb and data_manip_v2.ipynb iPython
notebooks. The project shows the top 10 causes of death in an interactive
visualization. The visualization can be found
[here](http://bl.ocks.org/enyeartj/raw/23057bb33ec0bd199fb57f7384142af3/). The
first and second drafts can be found in index1.html and index2.html. The final
draft is in the link just mentioned or in index.html.

## Design
I decided to use line charts because they work well for time-series data like
this. Even though each line gets plotted separately, I made sure that each line
had its own separate color so that there would be a dual visual encoding to help
reinforce the impact of the visualization. I went with a "martini glass"
narrative structure: The stem of the martini glass is the visualization cycling
through the different causes, and then the cup of the martini glass is the part
where the user gets to interact with the data and can choose their own adventure
so to speak.

## Feedback
On the Udacity Data Analyst Nanodegree forums, I received
[this feedback](https://discussions.udacity.com/t/project-feedback-top-10-causes-of-death/234457/2?u=jbroshek):
> Hi @jbroshek,
>
> your visualization looks great and congrats on completing the first draft. However, here are some observations which you can include.
>
> As the theme is to narrate a story, it would be great if you could automate the selection process, instead of manually clicks.
> you can see that the trend in heart disease deaths is declining, may be you can highlight that.
> axis labels should be aligned instead of overlapping in the graph itself.
> instead of dynamic upper limit in the y-axis, choose a constant value.
> you can see the animated version here for your reference.
>
> [http://bl.ocks.org/vishy730/raw/3fffab0646e5d183eee4f1aa925fef1b/](http://bl.ocks.org/vishy730/raw/3fffab0646e5d183eee4f1aa925fef1b/)

On the Udacity Data Analyst Nanodegree Google+ group, I received the following:

#### Khaled Salah:
> hello john,  I usually don't comment on visualization but I really like yours, your color choices, data choices and the way the axes range changes between each data. But there are two things that bothered me, 
> 1- the animation at the first, goes two fast + it run when I open the graph which gives no time to understand what the data are about or what the axes have inside, may be alittle  slower animation with some popup messages to explain your graph.
> 2- the second point it's not important but I want to say it anyway, the range of the Y-axis for some diseases it's wide but for others it's small  just like "Breast Cancer" it goes from 41K to 42K, so the graph may show false expectation for the rises and falls. 
>
> but at all it's really a good graph which gives me new information about number of deaths for different diseases over time, well done (Y)

#### Luiz Gustavo Schiller:
> Hi John, I really liked your visualization. Nice colors and animations. Very good storytelling. The only thing I would suggest is to sort the diseases by the most recent death rate. This way the rightmost end of the chart will not decrease from breast to colon cancer for example.
> Keep up the good work!

#### Kurt Jonske:
> Great work, similar to Khaled the most pressing thing i'd rec is to make sure your y-axis is similar or you point out % change since inception.

#### Kevin Vo:
> Hi John, your visualization is great.
> Some feedbacks:
> - I notice that the legend is very far on the right of the window. I suggest you create some div to add your svg and legend in a same place. ( See the attached photo)
> - I think you should have give people option to combine multiple lines into 1 chart. For example, if I click on diabete and colon cancer, it will show two lines on the chart. And we can select/deselect any options we want.
>
> Would you mind take your time provide me some feedback for my visualization on the below post? Thank you very much.

From the first to the final draft, I applied the following changes based on the
feedback received:

1. I fixed the bottom of the y-axis to zero so that the data doesn't look
too misrepresented between causes. (I kept the upper limit dynamic because
I felt that seeing the growth in scale from one cause to the next makes
for a more memorable visualization).
2. I slowed down the animation so that you can read the labels and see
what's going on before it switches to the next cause. (If you think it's
still too fast, let me know).
3. I expanded the summary to highlight a few specifics and explain how to
use the interaction (although, hopefully it is self-evident).
4. I sorted the causes by number of deaths on the last year as opposed to
total number of deaths like I had originally.
5. I added divs so that the legend comes out next to the chart as opposed
to way off to the right or overlapping.

## Resources
#### Mike Bostock
- [Three Little Circles](https://bost.ocks.org/mike/circles/)
- [Thinking With Joins](https://bost.ocks.org/mike/join/)
- [Axis Component](https://bl.ocks.org/mbostock/1166403)
- [Multi-Series Line Chart](https://bl.ocks.org/mbostock/3884955)
- [Chained Transitions](https://bl.ocks.org/mbostock/3903818)

#### Jerome Cukier
- [animations and transitions](http://www.jeromecukier.net/blog/2012/07/16/animations-and-transitions/)

#### d3noob
- [Simple graph with grid lines in v4](https://bl.ocks.org/d3noob/c506ac45617cf9ed39337f99f8511218)

#### [CDC Wonder Database](http://wonder.cdc.gov/cmf-icd10.html)
Centers for Disease Control and Prevention,
National Center for Health Statistics. Compressed Mortality File 1999-2014
on CDC WONDER Online Database, released December 2015. Data are from the
Compressed Mortality File 1999-2014 Series 20 No. 2T, 2015, as compiled from
data provided by the 57 vital statistics jurisdictions through the Vital
Statistics Cooperative Program. Accessed at
[http://wonder.cdc.gov/cmf-icd10.html](http://wonder.cdc.gov/cmf-icd10.html) on Dec 1, 2016 12:04:51 AM.