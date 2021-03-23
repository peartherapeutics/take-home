# @peartherapeutics/take-home
## Introduction
In this exercise, you will be retrieving text from a free public facing API and performing a basic sentiment analysis using an open source library called *sentiment*. No knowledge of sentiment analysis algorithms is necessary for this exercise, and any complexity in that domain will be abstracted away by the library itself.

## kanye.rest

kanye.rest is a free REST API for getting random Kanye West quotes (Kanye as a Service).

![Kanye Angry](images/kanye_angry.png)
> "Just stop lying about shit. Just stop lying."

![Kanye Happy](images/kanye_happy.png)
>"I'm a creative genius"

An HTTP GET request can be made to https://api.kanye.rest, and a random Kanye West quote will be returned in the following JSON structure:
```
{
"quote": "Sometimes you have to get rid of everything"
}
```

## sentiment

sentiment is an MIT licensed open source node library that can be found at https://www.npmjs.com/package/sentiment. You can perform a sentiment analysis of a quote using the following syntax:

```
var sentiment = new Sentiment();
var result = sentiment.analyze('Sometime you have to get rid of everything');

```
The result of the sentiment analysis will return an object with the following properties:

- <b>Score</b>: Score calculated by adding the sentiment values of recognized words.
- <b>Comparative</b>: Comparative score of the input string.
- <b>Calculation</b>: An array of words that have a negative or positive valence with their respective AFINN score.
- <b>Token</b>: All the tokens like words or emojis found in the input string.
- <b>Words</b>: List of words from input string that were found in AFINN list.
- <b>Positive</b>: List of positive words in input string that were found in AFINN list.
- <b>Negative</b>: List of negative words in input string that were found in AFINN list.

## Instructions
Write a program that will perform a sentiment analysis on 12 random Kanye West Quotes and summarize the average sentiment of those quotes. Examples of possible summaries: 
- You might want to average the score of all quotes
- You might want to count any recurring positive or negative words
- You might want to highlight the most positive and most negative quotes.

There is an opportunity here to be creative and come up with your own analysis (if you want). You can do something as simple as write a script that outputs your summary directly to console, all the way to something more complicated like creating a single page web app that shares your summary in a more colorful way.

There is no right or wrong answer, and there is no time limit. You are encouraged to not spend more than a few hours on this project, as we want to be respectful of your time. This is an opportunity for you to showcase your engineering skills, so do your best and be prepared to talk about your solution in person.

