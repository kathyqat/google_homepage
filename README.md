# google_homepage

This project is for building a visual copy of the Google.com homepage from scratch. It is a way to practice and demonstrate the HTML and CSS that I have self-taught through The Odin Project's (TOP) [Full Stack Development](http://www.theodinproject.com/courses/web-development-101/lessons/html-css) course.

Codepen link: https://codepen.io/kathyqat/pen/ExjgNOM

Overall, I'm quite pleased with my work :)

I was quite stubborn and wanted to solve the problem without looking at the navbar guide that TOP suggested. It did take me longer than necessary, but because this was my first real work, I wanted to make sure that I had a solid grasp of the concepts. I didn't want to just follow along with the example like in Free Code Camp lessons. I'm not shy about Google-ing an issue, but it felt like an easy way out if I used the guide and not something that I thought to Google myself. Maybe I'll go back in later and make the code even more responsive. It has some degree of responsiveness, especially compared to some of the student solutions that I've seen. Please don't dispel the illusion and try making the viewport too small.

Some methods that were tried but didn't work:
1. Using background: url(); to put the magnifying glass icon in the search field. The image was able to be sized and positioned properly, but the opacity could not be changed and I didn't want to simply find and use a grey version. On second thought, this way is probably smarter and more robust.
2. Using flexboxes to position the header items in a row. I thought I could make use of flex-start and flex-end values, but realized it was too much tinkering to separate the header into two sections and deal with all of that.
3. Using repeat(auto-fill,minmax()); to create the columns. I knew the space between "Store" and "Gmail" would change size, so I thought I could fill extra generated space with columns. Problems were that column thickness was too hard to adjust and the right side of the header kept slightly moving as the width of the viewport changed. I did try auto as the min and max value separately, but then it made the columns too thick or too thin. The Sign-in button would wrap when the columns were too thin and that was frustrating too. I spent the most time trying to make this work. In my defence, I had only seen auto in place of where min-content would be used and it functioned the same.

Weird things that I don't know why it works like that: 
1. The Sign-in button was too high. Trying to manually declare the height for the button and the header didn't work. I could finally change the height after declaring align-self: center. I don't know why just declaring the height didn't work or even why it had to autofit to the cell.
2. The footer would ignore the display: grid when I tried to position: absolute the footer. I don't know why so I gave up on that and turned the whole body into a grid. It was then much easier to stick the footer at the bottom.
3. If main's position was too far away from the top, it would move the footer away from the bottom. Why?? Best I can describe what happened, it's like part of main's box would stick out from the bottom of footer's box. Using vh or % instead of px would yield the same result. I made main align to center to not worry about it.

Something useful that I learned but didn't end up using in the final code: 
grid-column: span 1/last-line;

This makes the element span 1 column and end wherever the last line is. Effectively ensuring that the element is always in the last column.

Side note: I didn't know README could be edited on Github and now I have too many commits from just minor editing on here.
