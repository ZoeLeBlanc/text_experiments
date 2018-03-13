Very comprehensive introduction to Bokeh and Pandas! I enjoyed learning more about some of the functionality of these libraries, and I think you do a good job of 'narrating' the code.

I'll try to keep my review fairly short since Ben gave you a lot to work with.


#Overview Section: Greater Emphasis on Why than what
I see that Ben is pushing for more generalized skills, but I would push for you to address briefly why should someone turn their historical data into visual arguments. This pretty much assumed in the entire tutorial but I think it's worthwhile to talk about visualization as a way to test hypotheses or elucidate patterns. I would then move your bullet points about what you'll do in the tutorial to the The WWII THOR Dataset section where you could talk about your specific hypotheses. I would finish the overview section listing the skills you will learn/need to visualize historical arguments.

#The WWII THOR Dataset
I agree with Ben that you don't really go into the content of this data, which I think you could if you framed each graphing exercise as a way to test your hypotheses. Those bullet points from the overview could be reworked as questions that you want to explore in this tutorial. I do think the content of this dataset may be less exciting for some researchers so you might want to mention datasets used in other Programming Historian tutorials as alternatives. You also need to add a download tag to the dataset otherwise people have to manually copy and paste it into a file.

#Creating a Python 3 Environment
Agree with Ben that conda is not really standard for most people and that using a virtual environment that works with a standard install of python would be preferable. I'm not sure if Programming Historian has guidelines on this but my understanding is that Pipenv is the current gold standard. You can install it with pip and it manages all dependencies https://pipenv.readthedocs.io/en/latest/
Out of curiosity, why aren't you using the latest version of bokeh? From what I can see everything you're doing should be compatible so was wondering if you had a certain rationale.

#Bokeh Overview
I agree with most of what Ben wrote, and I think this section should actually be shorter and titled What is Bokeh? and that you could move the second and third paragraph to the end of the tutorial where you could talk more generally about Bokeh vs other visualization libraries.

#Adding to Your First plot
Mention that you should add these lines before the show method.

#The Bokeh ColumnDataSource
At line 72 "This approach to styling is mostly self-explanatory and this is an advantage of Bokeh, but you can see that sometimes Bokeh takes this too far. Some of its naming conventions are too verbose; for example, axis_label_text_font_size could probably just be called label_font_size since we already know we’re operating on an axis and the use of text and font seems redundant. Hopefully, this verbosity will be reigned in with future releases."
I think you can remove this aside or move it to the bottom of the tutorial if you have a section talking about Bokeh more generally.
Also the target locations seem like it would better with the mapping graph example, and I like Ben's idea using a different set of variables for the scatterplot example.


General comments:
- You tend to write about the code before showing it which I think is actually harder to follow than having the code first to copy and then explain what it's doing. I think if you could reverse the order in most places it would make your explanations clearer to the reader. I can list specific instances if you decide to reorganize.
- As mentioned earlier you aren't really presenting any hypotheses to test which makes it hard to understand the choices you're making or even the value of the visualizations. Even in exploratory data analysis you usually have a very generalized hypothesis to test. I think foregrounding these could help differentiate between which plots are appropriate for which questions. Also lines like "Interestingly, we’re not limited to just using column names for coordinates. We can also pass a column name for other parameters such as size, line_color, or fill_color. This allows styling options to be determined by columns in the datasource itself" p. 70 or "The order of this list determines the order that the columns will be stacked from bottom to top (after you’ve worked through this example, try switching the column order to see what happens). " p. 99 could be expanded to address how stylistic changes impact the argument of the visualization. I think it would be worthwhile to demonstrate how changing the styling of the graphs impacts the type of visual argument you make (I think the stacked bar chart could easily be used for this).  
- Agree with Ben on avoiding difficult list methods and I also had never heard of masking before. I personally prefer df.loc[df['COUNTRY_FLYING_MISSION'].isin(('USA','GREAT BRITAIN'))] but you could just link to this Stack Overflow post with a note that masking is just one way among many for selecting data in pandas https://stackoverflow.com/questions/17071871/select-rows-from-a-dataframe-based-on-values-in-a-column-in-pandas
- Finally the tutorial ends really abruptly. I think moving some of the Bokeh overview section to the end as a place to discuss other visualization/plotting libraries, as well as link to other useful resources would be helpful. You might also summarize the hypotheses you tested and what you discovered with these visualizations.

Overall I think you have really clear language for explaining the code that would be furthered if you spent some more time on framing your plots as ways to explore historical questions. You don't have to go crazy in depth but a line or two about what mapping vs bar chart etc... help visualize for historians would be really helpful for people new to visualization that might not understand how you're selecting which variables to graph.
