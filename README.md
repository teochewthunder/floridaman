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

## JavaScript (TBC)
