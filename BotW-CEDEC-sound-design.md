# CEDEC Breath of the Wild Talks, Sound Design

*author: [Matt Walker](https://medium.com/@gypsyOtoko/this-is-a-reposting-of-my-twitter-thread-summarizing-articles-written-about-the-cedec-botw-dev-266c34fd30e8)*

*transcribed to markdown: [Fletcher Porter](http://fletcherporter.com)*

This is a reposting of my Twitter thread summarizing the BotW CEDEC talk on
sound design, which can be found here:
<https://twitter.com/gypsyOtoko/status/915547728062459906>

This thread is for the CEDEC sound session: “BotW — The Open Air Sound Playing
a Massive, Breathing World”. Link:
<http://game.watch.impress.co.jp/docs/news/1078827.html>

![title slide](http://game.watch.impress.co.jp/img/gmw/docs/1078/827/html/sound01.jpg.html)

They required the kind of sound design that would heighten the immersion of
being in Hyrule, relaying the rules of the world and the material of the
objects located within, and the sense of air flowing through that world. It
was something the sound director couldn’t explain with words, so he chose to
make a concept video during production to help explain this and shared it with
the composers, sound designers, programmers, planners and artists.

To heighten this immersion they chose to express that which could not be seen
through sound — separating into several categories: environmental sounds, base
noise, water sounds like rivers and waterfalls, birds chirping, grass
bristling, insects, the wind, footsteps, etc. Wind sounds were created using
noise as a base, spawning 3 different sound sources to twirl around the
player, eventually adding footstep noises — which were recorded on site in
Kyoto.

The base noise — the foundation for all environmental noise is a faint air
sound which changes depending on whether you’re indoors or out, or near water,
and also changing base on nearby plant life, time, organic activity or rain

For music, they started with the idea to restructure what music really means
for a Zelda game. So they first chose not to play a looping song on the
over-world. This meant that they’d place an emphasis on the environmental
sounds — those being the only thing you would always hear. With this they
found that they were missing something — nothing to accent certain moments,
that feeling of arriving somewhere special. So they chose to play music at
special places, and to play random phrases occasionally to break up the
monotony. In doing this it’s less apparent that the music has looped over a
long period of time.

This still felt too simple, so they chose to play music in places like
villages. They made these songs dense, made them all unique, and placed them
as emitters on specific areas of the map to make it feel like you were in just
one place of a vast world. These emitters were made so as not to feature any
special progression, then change from this environmental music in stages as
you proceed into the area, which also expands the role of the field’s design.

All the different music and sound effects were each given a priority and
volume to help decide what should take precedence and when — note how
environmental sound effects stop momentarily while in battle.

Next they go into their development environment. Normally the sound team takes
orders from game designers and artists and creates sound based on those, but
for this title they worked proactively. So normally that would mean they would
get an order for “shield surfing” for instance, including all of the little
details such as the change in sound based on speed, playing a different sound
for the edge as it turns, etc. That style requires specialists that will be
able to pick out the finest details to achieve something of high quality,
which it does, but that requires that they also have an complete understanding
of the whole project design spec and schedule, or else spec changes could be
costly.

They realized this would be devastating to the project, so to avoid that they
improved their workflows, using tools, libraries, working between sections so
as not to burden the sound team with work they wouldn’t have to do.

They introduced 3 tools into the mix: SLink, allowing designers to click an
actor in game with their mouse and bring up a sound table where they could
then specify their sound and test it out — which also worked for animation.
AssetBinder, their asset manager tool with search, filter, single and batch
volume adjustment, automatic conversion and version control.

They also decided to “leave it up to machine” in regards to tasks to minimize
necessary work, using Jenkins to randomly place sound emitters for the
environmental sounds throughout the field. This allowed for various parameters
such as only placing bird chirping around trees, but not small trees, stumps
or dead trees. Finally, they made it so that non-sound members could set
sounds as well — so allowing the scenario writers to set cutscene voice, for
instance.
