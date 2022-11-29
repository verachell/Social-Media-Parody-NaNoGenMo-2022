# Social-Media-Parody-NaNoGenMo-2022
Generates >50000 words of parody of social media

## Social Media Parody
### Usage - how to run this program

Please note: This code requires that:   
- ```ruby``` is installed on your machine and  
- you have the ```yeetwords.rb``` file from the YeetWords repository (see below for where to get it and place it).  

To run this social media parody, first download the contents of this repository into your working directory. You will also need to download the ```yeetwords.rb``` file from the [YeetWords repository](https://github.com/verachell/YeetWords) (I used v 1.2.0 of YeetWords for this).

Then in your command line, type  ```ruby yeetwords.rb parody.txt```

A file containing the >50000 words parody will be generated in html format. The html includes ficticious social media posts, newspaper entries, and more. 

The html will display correctly so long as you have it in the same directory as the css file provided in the repository (```w3.css```) - this is the case by default, but if you move the html file you will also need to move the css file.

### Overview
This parody consists of social media posts, real life activities, and newspaper reports (all ficticious).

This parody has a defined beginning, middle and end. A fair amount of templating was necessary to achieve this. 

This is not a case where the story's very plot comes seemingly out of nowhere, but rather where the rhetoric and repetition necessary for the parody is filled in by the algorithm according to the "bones" of the template. This template is written in YeetWords.

#### Things that change with each run of the program
Each time this Social Media Parody algorithm is run, the main character's names and the other usernames are randomized. The main character's occupation is also randomized, as are the popular items (one of which becomes part of the conspiracy). The supposed goal of the conspiracists is also randomized. Advertiser brand names are also randomized. Therefore a somewhat different story will be generated each time, but illustrating the same points.

### Credits

#### CSS
The [w3css stylesheet](https://www.w3schools.com/w3css/) is used for styling the HTML. 

#### Sources of words and phrases
Latin phrases translated into English came from https://parade.com/1247077/marynliles/latin-phrases/ and these were used as a source of content for aspirational ad brands in this story

Latin words came from https://reference.yourdictionary.com/other-languages/latin-vocabulary.html and were used as a source of potential names for aspirational ad brands

The list of things for trending items were crowdsourced from family, aiming for unusual and/or aspirational items, a physical item/object, large in size, and not a living thing 

Anarchist phrases came from the Project Gutenberg book [The Right To Ignore The State by Herbert Spencer](https://www.gutenberg.org/ebooks/34649). The content of the book was processed as follows for use in this social media parody: individual phrases were isolated (phrases defined as anything between commas and between certain other punctuation, with the punctuation removed in the process). This isolation was done using [this gist](https://gist.github.com/verachell/44047995f244fcea726613ceb99531c5), resulting in a series of unpunctuated phrases. Phrases from this list were used together (in random order) to produce political rhetoric.

Sentences about the weather came from https://github.com/verachell/Horror-Story-with-Monster-NaNoGenMo-2020 - the positive, neutral and negative weather sentences were combined into 1 set of weather sentences.

The list of places came from https://github.com/verachell/Hero-quest-NaNoGenMo-2019

Newspaper names were in part created manually, and also from words in https://powerofpublish.com/newspaper-names/ and https://www.namesmore.com/newspaper-names/

Animals, emotions, large nouns, clothes bottoms, portable nouns, positive adjectives, tree types, and some colors are from https://github.com/verachell/English-word-lists-miscellaneous-categories/

Past tense verbs (verbed) present tense verbs (verbing) and interjections, adverbs and conjunctions are from https://github.com/verachell/English-word-lists-parts-of-speech-approximate

Html color names (e.g. red, goldenrod, aliceblue) came from https://htmlcolorcodes.com/color-names/ - names were pasted into a spreadsheet and extracted the column of interest with just the names in it.

Newspaper colors were hand-selected from the full list of html color names to allow light beige or gray backgrounds.

Face emoji codes came from https://www.w3schools.com/charsets/ref_emoji_smileys.asp (pasted into spreadsheet and isolated the column of interest - in this case the decimal html code)

Angly emoji codes were hand-selected from the full list of face emoji codes

Male and female first names were obtained from the Top Names Over the Last 100 Years from the Social Security Administration of the USA, https://www.ssa.gov/OACT/babynames/decades/century.html which at the time of downloading were from the years 1921-2020, and comprised the top overall 100 most popular names for each gender.

Surnames came from: Powell, Kimberly. "Top 100 Most Common Last Names in the United States." ThoughtCo, Feb. 16, 2021, thoughtco.com/most-common-us-surnames-1422656.

### Word count and how it was calculated




