# Spotify
 
Spotify Data 

This week I wanted to take a dive into Spotify data that was most recently updated April 2021.
I downloaded this data set from kaggle and was able to sift through some song correlations dating all the way back to 1992. This data set was incredibly large (roughly 600k tracks) so I filtered the data to only show songs uploaded to spotify in 2021-  narrowing down my data set made it a lot easier to work with. 

Questions I started off with:
What initially interested in me, prior to analysis, was what variables in a song made it popular?
What are the top 10 most popular songs? 
Was there a correlation between a certain variable and popularity?
Was there a correlation in popular artists and variables in songs?
With a bit more skill in data analysis/coding, I would have liked to be able to create a formula that would predict song popularity.


Methodology and Analysis:
I started by importing the csv data set into Pandas. I then narrowed down the data set to filter for the year 2021. This cut the data down by quite a bit and allowed me to focus in on a more granular level at songs that have been released this year. 

I wanted to start by simply looking at the most popular songs. The songs were ranked from 0-100 in a popularity score, where 100 is the max. Below are artists, along with the specific track they produced in 2021,  ranked in order of popularity. 


While it was helpful to see top artists ranked by popularity, I wanted to drill down further and focus on variables and correlation to popularity. I started this part of my analysis off by plotting a heatmap of correlations in Pandas. As you can see from the below chart, 1 is the highest level of correlation and it decreases from there. The diagonal line his 1 in places where the variables match each other - ex. “popularity’ lines up with ‘popularity”. The highest correlations below are energy and valence, hitting a score of 0.44. The second highest and most notable is danceability and valence, hitting a score of 0.41. This made a lot of sense to me as Valence describes the musical positiveness conveyed by a track. Positiveness can therefore likely be associated (and correlated) to energy and danceability. This also seems to make sense as positive songs have a good energy and can make you want to dance.

I found it very interesting that on average in 2021, the highest correlation to popularity is speechiness at 0.12. 
Speechiness: Detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value.



Since I wasn’t able to find a super high correlation between popularity of a song and the variables with high correlations, I decided to make a radar chart showing the first 5 songs to see what those looked like in terms of the variables. The top five songs in the 2021 data set are as follows:

Peaches by Justin Bieber

Caller License by Olivia Rodrigo 

Astronaut in the Ocean by Masked Wolf

Leave the door open by Bruno Mars

Fiel by Los Legendarios


The Variables I looked into are listed below, along with a description of what each one is. 

-Danceability - Describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity.
-Liveness - Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live
-Valence  - Describes the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).
-Energy -Represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale.
-Speechiness - This detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value.
	-Acoustiness -A confidence measure from 0.0 to 1.0 of whether the track is acoustic.


Graphic linked here: https://public.flourish.studio/visualisation/6676559/


Insights 

Based off the radar chart it looks the top 5 songs are high in danceability, energy and valence - which aligns with my analysis in pandas. What’s also interesting is that the 2nd ranked song by popularity - Drivers License by Olivia Rodrigo - is very high in acousticness, something the other 4 songs don’t have nearly as high rankings in. It would appear that if you want to produce a popular song on Spotify make sure it hits high in danceability, energy and valence. 

