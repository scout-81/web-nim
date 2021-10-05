# Web NIM

This is a version of NIM that has an unbeatable bot algorithm

The only code that needs attributed is the for loops, for displaying the game details, and how global variables work.
Everything else is original.

* [For loops][for-loop]
* [How global variables work in JS DOM][js-dom-vars]


It's also hosted on Github Pages [here][github-pages], so you can try it with out needing to download it.

* * *

Nim has been played since at least the 16th century[[1][1]], and in it's time has had many versions. This version, you pick how many you want to remove from the "pile", ether 1 though 3. The last person to collect all of the pieces of the pile wins. You go first, the bots move is calculated at the same time your move is displayed and calculated.

That is the same text that is displayed on the actual page, the only difference is the citation.

* * *

## QR code project?

This project was originally supposed to be a QR code game, where all of the HTML data is stored on a QR code.
Unfortunately, I was never able to get the HTML to display in the browser with "data:text/html," in the address bar.
I also tried base64 encoded text with "data:text/html;base64," but didn't work either.

If you know how you could fix this, please fork this repository and submit a pull request..


I include the source code with comments so editing this should be easy.
There is a compressed, less human readable version that is almost 3 times smaller in file size then source.
I would recommend the compressed version for transmission, over web, or any other means.

* * *

## How does this thing win every time?

I don't know if you have already played and repeatedly tried to beat the bot.
But it's mathematical imposable to beat the bot, as long as the player goes first, and everyone plays by the rules, the bot will win every time.
A good example of this is Dr NIM[[2][2]], a board game that was made in the 1960s. It was able to beat the player every time.
Stand-up Maths (Matt Parker) made a video about it, you can watch it [here][dr-nim-vid], it's just under 12 mins long.

#### The algorithm, in depth

This is the algorithm, the variable NUM is the number the player has chosen 1, 2, or 3 (because the player goes first), the variable AI is the move the algorithm produced.

> AI = 4 - NUM

Here is a truth table of player moves and AI moves


| Player Move | AI Move |
| --- | --- |
| 1 | 3 |
| 2 | 2 |
| 3 | 1 |

The main way of winning Nim is to let your opponent go first, and follow the table above, if your opponent takes 2, you take 2. The main way of thinking of this is to split up the pile in to 3 sections with 4 each. Like this #### #### ####. Unfortunately for you, it's imposable to win against anything using this algorithm.

I may make a fork of this that won't play a perfect move on the first turn, meaning the player could have a chance at winning.

* * *

## Source Code
Source code is available in this repository, just look for "source.html" in the Code section, or find it [here][page-source].

* * *

#### Citations

* [For Loops on Mozilla MDN Web Docs][for-loop]
* [Global variables (JS Scope) in JS DOM on W3Schools][js-dom-vars]
* [(1) Nim on Wikipedia][1]
* [(2) Dr. Nim on Wikipedia][2]

###### Other Citations

* [This project on Github pages][github-pages]
* [Stand-up Maths YouTube video on "The Unbeatable Game from the 60s: Dr NIM"][dr-nim-vid]
* [The source code of this project on Github pages][page-source]

[for-loop]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/Unexpected_token#not_enough_brackets
[js-dom-vars]: https://www.w3schools.com/js/js_scope.asp
[github-pages]: https://scout-81.github.io/web-nim/nim.html
[1]: https://en.wikipedia.org/wiki/Nim
[dr-nim-vid]: https://youtu.be/9KABcmczPdg
[page-source]: https://github.com/scout-81/web-nim/blob/main/source.html
[2]: https://en.wikipedia.org/wiki/Dr._Nim
