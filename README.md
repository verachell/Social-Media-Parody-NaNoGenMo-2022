# Social-Media-Parody-NaNoGenMo-2022
Generates >50000 words of parody of social media. Output is an html page.

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

This parody has a defined beginning, middle and end. 

This is not a case where the story's very plot comes seemingly out of nowhere, but rather where the rhetoric and repetition necessary for the parody is filled in by the algorithm according to the "bones" of the template. This template is written in YeetWords.

#### Things that change with each run of the program
Each time this Social Media Parody algorithm is run, the main character's names and the other usernames are randomized. The main character's occupation is also randomized, as are the popular items (one of which becomes part of the conspiracy). The supposed goal of the conspiracists is also randomized. Advertiser brand names are also randomized. Therefore a somewhat different story will be generated each time, but illustrating the same points.

#### Story template outline
![diagram of story template](https://github.com/verachell/Documentation-Images/blob/26372a7f91ccc035b7aedc6a6806194afa956a58/social-media-parody-documentation-images/StoryTemplateOutline.png)

### Credits

#### CSS
The [w3css stylesheet](https://www.w3schools.com/w3css/) is used for styling the resultant HTML. 

#### Images
All images e.g. as social media posts and as profile pictures were generated using https://github.com/verachell/Image-Generator-from-Photo-Subsections from photos I took myself

#### Sources of words and phrases
Latin phrases translated into English came from https://parade.com/1247077/marynliles/latin-phrases/ and these were used as a source of content for aspirational ad brands in this story

Latin words came from https://reference.yourdictionary.com/other-languages/latin-vocabulary.html and were used (in conjunction with colors and tree types) as a source of potential names for aspirational ad brands

Trending items were crowdsourced from family, aiming for unusual and/or aspirational items, a physical item/object, large in size, and not a living thing 

Anarchist phrases came from the Project Gutenberg book [The Right To Ignore The State by Herbert Spencer](https://www.gutenberg.org/ebooks/34649). The content of the book was processed as follows for use in this social media parody: individual phrases were isolated (phrases defined as anything between commas and between certain other punctuation, with the punctuation removed in the process). This isolation was done using [this gist](https://gist.github.com/verachell/44047995f244fcea726613ceb99531c5), resulting in a series of unpunctuated phrases. Phrases from this list were used together (in random order) to produce political rhetoric.

Html color names (e.g. red, goldenrod, aliceblue) came from https://htmlcolorcodes.com/color-names/ - names were pasted into a spreadsheet and extracted the column of interest with just the names in it.

Newspaper colors were hand-selected from the full list of html color names to allow light beige or gray backgrounds.

Face emoji codes came from https://www.w3schools.com/charsets/ref_emoji_smileys.asp (pasted into spreadsheet and isolated the column of interest - in this case the decimal html code)

Angry emoji codes were hand-selected from the full list of face emoji codes

Sentences about the weather came from https://github.com/verachell/Horror-Story-with-Monster-NaNoGenMo-2020 - the positive, neutral and negative weather sentences were combined into 1 set of weather sentences.

The list of places came from https://github.com/verachell/Hero-quest-NaNoGenMo-2019

Newspaper names were in part created manually, and also from words in https://powerofpublish.com/newspaper-names/ and https://www.namesmore.com/newspaper-names/

Animals, emotions, large nouns, clothes bottoms, portable nouns, positive adjectives, tree types, and some colors are from https://github.com/verachell/English-word-lists-miscellaneous-categories/

Past tense verbs (verbed) present tense verbs (verbing) and interjections, adverbs and conjunctions are from https://github.com/verachell/English-word-lists-parts-of-speech-approximate

Male and female first names were obtained from the Top Names Over the Last 100 Years from the Social Security Administration of the USA, https://www.ssa.gov/OACT/babynames/decades/century.html which at the time of downloading were from the years 1921-2020, and comprised the top overall 100 most popular names for each gender.

Surnames came from: Powell, Kimberly. "Top 100 Most Common Last Names in the United States." ThoughtCo, Feb. 16, 2021, thoughtco.com/most-common-us-surnames-1422656.

The other words and sentence lists were created manually.

### Word count and how it was calculated
The output of this algorithm is styled html. This makes it non-straightforward to determine the word count, but it was ultimately possible to get an accurate word count, which I will describe here.

One problem with outputting *styled* html as is the case here is that the built-in YeetWords word count function is unable to distinguish between the front-facing words and the html words. We want to count only the front-facing words for NaNoGenMo and not the back-end style code. 

For unstyled html (no classes or styles), this issue has been taken into account within the YeetWords code and the built-in word count is accurate. So if someone was using html output merely to make the project viewable by a browser instead of a Markdown viewer, this poses no problem. i.e. things like ```"<h2>The following day</h2>"``` still counts correctly as 3 words since there are no additional spaces anyway caused by the html elements.

But for this project that is heavily styled with classes and/or custom inline styles, additional spaces of necessity are added, and these will cause an inflated word count. For example:
```"<span title="_TOOLTIP_" class="w3-hover-text-green" style="color:gold;text-decoration:underline">https://link.yw/b...</span>"```

In this instance, the only front-facing word is ```https://link.yw/b...``` (1 word) and we want to count it only as 1 word for NaNoGenMo purposes, but based on the number of spaces, YeetWords will count it as 4 words (more, if TOOLTIP expands out to more than 1 word, which it usually is). You can see I have already completely minimized the number of spaces in the styles and classes to those only strictly necessary, and this is the case throughout the entire project. Still, the internal word count reported via YeetWords is overestimated in this situation, for the reasons mentioned just above. 

To get around this issue and come up with an accurate word count, I first considered trying to account for the back-end words. I did this by subtracting from the YeetWords word count the number of times the = symbol appears. This is because classes and styles are what add spurious spaces to the word count, and these all require a = sign. I was able to calculate this incidence easily using```grep -o \= DOCTYPEht_6934.html|wc -l```  and subtract that number of words from the YeetWords word count.

That was a big improvement in accuracy but is still an undercount. This is because some sections of classes will have multiple classes added (which have to be separated by spaces), e.g.
```<div class="w3-green w3-hover-opacity">```
In the above situation, the one = sign actually is associated with 2 back-end words that need subtracting, not just 1.

Another cause of undercount with the = sign is multiple words within the tag. As an example, image alts:
```<img alt="indistinct profile picture"...```
The above has 1 = sign associated with 3 back-end words that we want to remove from the word count, not just 1. (A possible solution is not to have image alts, but I could bring myself to write html without image alts.) The tooltips are another example of one = sign being associated with more than 1 back-end word that needs subtracting, since all tooltips have multiple words.

Bearing in mind that one = sign can be associated with 1, 2, 3 or possibly even 4 or more(?) words, I decided another approach would be necessary. 

#### The final solution to obtaining an accurate word count
With the html page displayed in the browser, I did select-all and copy to obtain just the front-facing words. I then pasted it into Xed, a Notepad-like Linux program. Xed had the advantage of only taking the text (no images), leaving only the text on the page. I then was able to use the built-in document statistics function in Xed to get the word count. Initially I started removing the comment icons before doing the word count (which were also copied over) via find and replace, but then it became evident that this did not affect the word count. Xed presumably is only counting words that come from alphanumeric characters.

To ensure my algorithm produced a sufficiently long word count for NaNoGenMo, I empirically increased the quantity of loops it was doing at each stage until it generated well over 50,000 words as determined by the copy-and-paste method described above. I made sure it was longer than the word count by quite a bit just to be on the safe side.
