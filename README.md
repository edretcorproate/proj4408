# Web Dev Starter Code

## Overview

Website accessibility

In the beginning the accessibility concepts were confusing. But after reading some articles I got through the basics.
I finally learned how to use firefox to inspect for accessibility components which helped me to code accessibility into
my project. I got some help for some of the content that was hard to understand. But it was overall good.

FYI Couldn't get audio to be accessible successfully.

To View / Run:
Livepreview in CS Code will show you the website on your local computer and itll let you
navigate on it like the real website.

To Compile:
Not applicable

## Sources and Credits
https://colorjs.io/docs/contrast

## Accessibility Lab Answers
Color

1. The text is difficult to read because of the current color scheme. Can you do a test of the current color contrast (text/background), report the results of the test, and then fix it by changing the assigned colors?

In terms of testing when I open the index into my browser and Right-Click and go to "Inspect Accessibility Properties" using
firefox, I can then go to Check-For_Issues: and select contrast. There each text-leaf is contrasted against its background to
determine read-ability. There's a text ratio and the end result tells me whether or not the contrast of the text and background is good or bad automatically.

To fix this you either change the text or the background, I did both because my lighter green fixed the majority of problems, however the blue hyper link and the white "welcome" text were not good color ratios.

* Changed .nav, article, footer, .secondary back-ground color from green (0,128,0) to (6, 255, 6).
* Changed .secondary back-ground color from green (6, 255, 6) to rgb(255, 235, 155);
* Changed html background from #dde to rgb(0, 0, 255);

Semantic HTML

1. The content is still not very accessible — report on what happens when you try to navigate it using a keyboard.

When using tab it doesn't navigate correctly, everything that wasn't labeled correctly were inaccessible.

2. Can you update the article text to make it easier for screen reader users to navigate?

* First, I added <p></p> elements around each paragraph to fix the size of the text for readability.

* Added Several headers: 
<h1></h1> to "Welcome to our wildlife website"
<h2></h2> to "The trouble with Bears"
<h3></h3> to "Habitats and Eating habits"
<h3></h3> to "Mating rituals"
<h4></h4> to "About the author"
<h5></h5> to "Add comment"
<h5></h5> to "Comments"
<h6></h6> to "Related"

3. The navigation menu part of the site (wrapped in <div class="nav"></div>) could be made more accessible by putting it in a proper HTML semantic element. Which one should it be updated to? Make the update.

It should be replaced from <div class="nav"></div> into <nav class="nav"></nav>.

The Audio Player

1. The <audio> player isn't accessible to hearing impaired (deaf) people — can you add some kind of accessible alternative for these users?

"To provide deaf people with access to audio content, you need to create text transcripts. These can either be included on the same page as the audio in some way or included on a separate page and linked to." -Mozilla.org

2. The <audio> player isn't accessible to those using older browsers that don't support HTML audio. How can you allow them to still access the audio?

We do this by creating our own custom controls for the audio that will not only make it keyboard accessible but also support many browsers.

The Forms

1. The <input> element in the search form at the top could do with a label, but we don't want to add a visible text label that would potentially spoil the design and isn't really needed by sighted users. How can you add a label that is only accessible to screen readers?

Basically you would Add <label></label> around the <input type="search" name="q" placeholder="Search query"> and <input type="submit" value="Go!"> elements respectively. You can test if a label is correct by using inspect accessibility properties just as I described earlier.

2. The two <input> elements in the comment form have visible text labels, but they are not unambiguously associated with their labels — how do you achieve this? Note that you'll need to update some of the CSS rule as well.

You put the name and comment in a label: <label>Your name:</label> and <label>Your comment:</label>

The Show/Hide Comment Control

1. The show/hide comment control button is not currently keyboard-accessible. Can you make it keyboard-accessible, both in terms of focusing it using the tab key and activating it using the return key?

Yes, change <div class="show-hide">Show comments</div> to <button class="show-hide">Show comments</button>

The Table

1. The data table is not currently very accessible — it is hard for screen reader users to associate data rows and columns together, and the table also has no kind of summary to make it clear what it shows. Can you add some features to your HTML to fix this problem?

Other Considerations?

1. Can you list two more ideas for improvements that would make the website more accessible?

Here are some improvements:
* Added <label></label> to "Your name:" and "Your comment:" and around
"Enter your name" and "Enter your comment" div wrapper replaced with label
wrapper

* Added <label></label> around audio controls

* Added aria-label="image1"
* Added aria-label="image2"