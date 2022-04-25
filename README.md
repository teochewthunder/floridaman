# Florida Man Headline Generator
This basically generates a series of 8 headlines with randomized wordings.

## HTML
- `floridamanApp` div interacts with he `Vue` object.
- 8 divs with the class `headlineContainer`. Each one uses `getStyle()` t get a background image.
- Each one has an inner div with the class `headline`. Each inner div, in turn, has a h1 tag. 
- Each h1 tag has a headline with placeholders for randomized words. These are references to the `headlines` array.

## CSS
- `headlineContainer` has round corners and an outline. The `overflow` property is set to `hidden`.
- `headline` has a translucent black background to help the text stand out.
- h1 tags are styled to be white with a black outline, and the words are capitalized.

## Images
- Each image is a possible background image depending on the words used in the headline.
- The default image used is `floriaman.jpg`.

## JavaScript 
- `data`:
 - `headlines`: An array of objects. Each object has properties that are arrays consisting of one or more empty strings. These empty strings are used as placeholders, to be replaced by a random value later on.
 - `wordTypes`: An array of arrays. Each array has a key, and contains strings. These strings are words that will be picked from.
- `methods`:
 - `fillHeadlineArrays()`: accepts an integer as an argument and uses that to reference the `headlines` array. Calls `getOne()` for every emty string encountered in the element's sub-arrays.
 - `getOne()`: accepts an array as an argument and returns a random element from that array.
 - `getStyle()`: accept an integer as an argument and uses it to reference the `headlines` array. Goes through each word in that element's sub-arrays and picks one word at random (`getOne()` is also used here) that will be used as the background image. (That background image has to exist).
- on page load, the `fillHeadlineArrays()` method is called, once for each element in `headlines`.
