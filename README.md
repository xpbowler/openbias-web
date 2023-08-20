[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE.md)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/xpbowler/2023ht6web.svg)


## Inspiration
In 2023, Canada forced social media companies such as Meta to remove Canadians' ability to read news on their platform. Five years earlier, 70% of the CBC's revenue was from the government. Large news corporations own multiple journals and write increasingly similar, biased, uninteresting and weak articles to promote their narrative. A solution against the constant unseen and unfelt propaganda was needed. We decided to tackle all those issues by creating OpenBias, a Chrome extension with crowdsourced data about the political bias of news articles.

## What it does
OpenBias consists of a website and a Chrome extension. The Chrome extension is always accessible no matter what webpage a user is on. If they're on a political news article, the user can open the extension and rate the bias (left-leaning or right-leaning) after reading. This data will be pushed to a cloud-based database and the average of all votes will be displayed in the pop-up. This information along with search features, displaying all articles, and a more detailed view is also available on the website. 

## How we built it
The Chrome extension was built using HTML/CSS/JS and called several node.js functions to write to our database. A manifest.json file allowed us to load the Chrome extension into our web browsers. The website was bootstrapped with React.js.

## Challenges we ran into
Accessing script files from the Google Cloud API or other sources was crucial to our project, however many important files were blocked by the Chrome extension host or the CORS protocol. This seems to be for safety reasons and we couldn't bypass them.

## Accomplishments that we're proud of
We're proud of having a functional cloud-based database that anyone with access to the Google extension can experience. The Google extension has features to read, update and create data in the MongoDB database. 

## What we learned
Through this hackathon, we learned about how to create Chrome extensions and the various security protocols that Chrome uses to protect its users. 

## What's next for OpenBias
OpenBias will expand to more and more users, solidifying the data we receive as statistically significant and representative of the population at large. As the number of websites and data points on our website increases, we plan to web scrape the websites and train a predictive neural network that will predict the political bias of any piece of text, including AI-generated text such as from ChatGPT. This will be actively used on our product with a low value (preferring human feedback more than AI) but will allow us to give predictions earlier when the number of votes is low. Additionally, this network could be made public to allow others access to an open, transparent way to identify political bias. It will help solve the rapidly growing issue of bias in generative-AI. OpenBias also has the potential to become a leading "fact-checker" type third party. Through transparent procedures, we may gain the trust of many news readers. This will prompt us into reviewing articles from certain news corporations as a third party and post stamps of approvals on unbiased and high-quality articles. The number of parameters to vote on will definitely be expanded upon using a drop-down menu, but those will just be a copy of the existing idea. Additionally, it would be important to track the IP address of voters or similar information to make it difficult to bot the votes.  Our main target was political news, but the applications of this idea don't have to stop there.

## Installation

Instructions:
1. Clone the repository
```
$ git clone https://github.com/xpbowler/2023ht6web
```
2. Install required dependencies
```
$ npm install
```
4. Run frontend
```
$ npm start
```
4. Run ```MongoDB``` backend
```
$ cd database
$ nodemon server
```
