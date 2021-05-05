# CEDEC Breath of the Wild Talks, UI Design

*author: [Matt Walker](https://medium.com/@gypsyOtoko/this-is-a-reposting-of-my-twitter-thread-summarizing-articles-of-the-botw-cedec-talks-which-can-be-91e9be85de51)*

*transcribed to markdown: [Fletcher Porter](http://fletcherporter.com)*

This is a reposting of my Twitter thread summarizing articles of the BotW
CEDEC talks, which can be found here:
<https://twitter.com/gypsyOtoko/status/915430391447674880>

Thanks to [@Nibellion](https://twitter.com/Nibellion) and tonyh24613 from Gaf
I’ve been alerted to articles based on the other BotW CEDEC talks — so how
bout a new thread?

[title slide](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui01.jpg)

Next up is the talk, “The Aim of BotW’s UI — Immersive, Impressionable UI”
(original article here: <https://t.co/XKV7zCYunN>). Being that their aim for
BotW was to reconsider Zelda conventions from the ground up, they discussed
how they achieved their goal of creating UI that is instantly recognizable as
a change, but seamlessly integrates with the game world in 4 categories —
graphics, font, design and animation. Their overall concept being, “only
essential UI”.

Graphics — goal was to be understated so nothing would stand out in a negative
way, coalescing information so there wouldn’t be as many places players would
have to look.

![understated button prompt](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui07.jpg)

For the title menu they chose to make proper use of empty space instead of
making the selections large.

![most of the title screen is empty space](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui08.jpg)

(余白 means empty space, just like keikaku means plan.)

To help unify the UI they adopted a color they called “Zelda White”, which has
a bit of yellow. This was used in the package and logo as well!

![pure white versus zelda white](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/html/ui10.jpg.html)

Font — they prioritized borderless, simply colored text with zero frills. The
overseas fonts were custom made, but for Japanese they used “Logo G Black” for
Katakana and “Raglan Punch” for Kanji — intending for the Japanese text to be
both powerful and nostalgic, italicizing to make it easier to read. They
applied this to the logo font for a cohesive feel.

![japanese font selection](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui11.jpg)

![japanese and latin typography](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui12.jpg)

(Note how the in-game fonts match with the logos for both Japanese and
international versions.)

UI Design — direction was to only display information when necessary, which
gives the screen more breathing room.

![lots of breathing room around UI elements](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui13.jpg)

The Pro HUD was actually created because NoA/NoE asked to clean up the screen
and get rid of even more UI elements -which lead to a heightened sense of
immersion.

![the pro hud has very few UI elements](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui14.jpg)

They designed the Sheikah Slate in tandem with the artists and chose to
differentiate its design and give it an ancient feel by adding more decoration.

![several of the ancient shiekah tech objects in the game](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui15.jpg)

They acknowledge that the lack of a tutorial was intentional to strengthen
immersion, and only display minimal UI elements so players wouldn’t feel
guided by the hand. They applied different animations to the UI in order to
make things more noticeable after decreasing noticeability by making UI and
fonts smaller.

![several animated ui prompts, including health decreasing, stanima drop after a jump, item pickup, and using a buttom prompt](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui17.jpg)

One example — hearts light up white when you’ve taken damage. Their method —
“Display simple UI and make it appear high quality”.

They created a tool they could use to capture textures and modify as necessary
for this.

![shader trickery used to make the game over screen high-quality](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/html/ui18.jpg.html)

(Image shows an example of how the capture tool was used for animation — first
they captured the Game Over text, then they applied a distortion texture and
animated, the result as shown on the bottom.)

They only had 2 UI designers who wouldn’t be able to handle everything alone,
so they worked with the programmers to implement little tricks. Expanding on
NCL’s proprietary "LayoutEditor" tool in a "data driven" fashion, allowing
designers to place and animate screen nodes, and giving programmers control
over them. Up until BotW, designers needed programmers in order to implement
data into the game, so with BotW it was changed so that the game screens could
be previewed on top of each other, over the running game.

![a screen capture of their layout editor](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui19.jpg)

![contrasting their old process flow for previewing UI and the new flow](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui20.jpg)

(This slide shows how their workflow changed. Previously they would have to
create an asset, check it in a viewer, pass into the build and then finally
check in-game. In BotW they would create, then preview in-game, then finally
implement.)

The game map was split into 120 sections that could be dynamically loaded,
with 4 levels of zoom. This included distinguishing non-open areas with
separate colors, so they needed to create 2,344 different screens, which would
have been impossible manually, so the map was procedurally generated, textures
would be generated for each section every night.

![showing off all the many textures that needed to be generated for the map](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui21.jpg)

Finally, they give examples of how they utilized their "screen capture"
technology to add filters & color adjustments to create UI. Image shows how
they composed the gear select screen, capturing the environment, masking and
redrawing.

![show link standing in front of the enviromnet, some ui being added to that picture, and a black recrangle added to that](https://game.watch.impress.co.jp/img/gmw/docs/1078/846/ui24.jpg)


