# GifTastic
A website that uses the giphy API to search gifs

## How it works
#### The website will show up with some initial buttons you can click to start a search of up to 12 images from giphy of the item you searched for. 

#### The add item bar can be used to add items to the bar for more search.

#### You can click on the still images of each gif shown to start the animated version.

## Thought Process

The idea behind it is simple. Start the code with an array of items I want to be as premade buttons. I then have a function called renderButtons to have each button dynamically generated and appended onto the bar.

To add more items, I simply assigned the #add-gif button to push the input into the array and call renderButtons again.

Using renderButtons I assigned the attribute "data-name" with the name of the item and in another function, displayGifs, assign that value into a variable called term so I can use this value to use the Giphy API.

Within the displayGifs function I used term, as previously mentioned, to set into queryURL for the ajax request. I set up a div to hold the rating and the image, and within the image I assigned multiple attributes: data-state, data-animate, and data-still so I can switch between animated GIF and still GIF by clicking on it. 

I used a document onclick function to implement this by using $(this).attr() to change the data-state and reassign the src of the image depending on what state it is in and apply the other one.

Another document onclick function is in place to run the displayGifs function once a button on the buttons bar on top has been clicked on.


## Demo Gif

A demo in the form of a gif can be found below
https://im3.ezgif.com/tmp/ezgif-3-fcbec9c5608e.mp4