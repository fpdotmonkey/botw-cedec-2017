# CEDEC Breath of the Wild Talks, Sound Design

*author: [Matt Walker](https://medium.com/@gypsyOtoko/the-final-botw-cedec-session-as-far-as-i-know-is-from-the-engineers-botw-project-management-c30f4e42598e)*

*transcribed to markdown: [Fletcher Porter](http://fletcherporter.com)*

The final BotW CEDEC session (as far as I know), is from the engineers — "BotW
Project Management — Seamless from Prototype to Final Product!"
<http://game.watch.impress.co.jp/docs/news/1078888.html>

![title slide](https://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec01.jpgg)

This session focused on 3 topics: project management, dev pipelines- using
TA’s as an example and QA. First focus was on their new tool coined the "Zelda
Editor" — the kernel of project operations.

![The zelda editor, with several screen captures behind it](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec02.jpg)

![more screen captures from the zelda editor](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec03.jpg)

They adopted the "Framework Approach" to development — first setting
guidelines and then adding on from there. They relate their milestone
definitions to running on a track — for the first lap they’d set up the
framework and create a proper, fun prototype, for the second lap they would
run through full production, and for the 3rd lap they would polish the product
as much as possible.

They also established restrictions for what wouldn’t be allowed for each
"lap". For the first lap — no implementing anything that wasn’t core to the
game, for the second they focused solely on producing and getting together all
necessary assets — no polish. As such, they used assets from previous games
such as villages and NPCs — including enemies and bosses during the prototype
lap.

![several characters reused during the second lap of development](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec05.jpg)

This meant that artists were focused on planning what they would create, and
validating their implementation methods during the first phase. In the second
phase there was a large volume of assets that needed to be managed, and they
found that their conventional task tools couldn’t cut the mustard, so they
gave Zelda Editor the ability to attach tasks to data within the editor,
putting effort in to ensuring that they wouldn’t end up with any "lost tasks".

![tasks assigned to element in the game world](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec07.jpg)

This meant that all temporary data would see proper progress. Conventionally
project management would be done manually, but now tasks were being aggregated
and automatically updated — ensuring correct information, management and a
relatively accurate project burn down chart by the end.

![spreadsheet of project tasks](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec08.jpg)

![graph of number of tasks to be completed](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec09.jpg)

The final lap focused on brushing all data up to final quality. Bugs were
managed as tasks for this project, using Zelda Editor for quick bug reporting
in-world. Model and texture size validation was done automatically, though
things like how items burned or whether weapons were floating in water as they
should, were checked manually.

Next, one of their TA’s (Technical Artists) discussed pipelines. They begin by
explaining that at Nintendo, above all else the most important thing is the
fun. This needs to be first and foremost in everyone’s mind, regardless of
occupation, and they have to tune until the very end to ensure it. "I am
certain that it's this persistence that leads to the highest quality." The
challenge the TA's took on, then, was creating a new development style that
would be able to produce that quality given the massive number of assets, and
knowing full well assets would have to be done and redone.

Their focus would be on ensuring a stable DCC environment. Assets were created
in Maya and Photoshop, with many different plugins being used by many artists
— so if something didn’t sync up it could block a large number of devs. They
created a dedicated software launcher for all the artists to ensure that they
were running the same dev environment — syncing Maya preferences and running
automatic tool tests. Errors reported at an artist’s terminal would be
automatically sensed and reported for quick handling.

![screen captures of the launcher and maya preferences](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec14.jpg)

![exceptions from Maya Python would be automatically reported](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec15.jpg)

They chose Havoc for their physics engine, and expected this to be a key
component of the fun, and also knew that there would be a large amount of
physics data that would have to be dealt with — even then, they chose not to
have any artists that would specialize just in physics. So they decided that
multiple artists would have to be able to stably mass produce physics data.
Their solution was to ensure that their Havok environment wasn’t accessible —
instead it would be funneled through DCC tool plugins to simplify the physics
data workflow. They also made checks to ensure that no dangerous physics data
could make its way into the ROM.

![screen captures of software launcher and Havok Content Tools, which wasn't accessible to developers](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec16.jpg)

They automated LOD creation, knowing that assets would experience spec changes
and retakes. In terms of automation they give the shrines as an example —
automating the merging process for model parts creation and placement,
allowing them to polish until the very end. In terms of animation — when
software versions were raised models, rigs and animation data updates were
automated.

They then shift gears to talk about how they managed versioning in order to
ensure smooth build workflows. Especially considering that they had partner
companies helping out, they set it up so that executables and resource
versions would match up at download time, and gave devs the ability to select
from multiple ROMs- so if they were having trouble they could recover from a
different ROM.

In terms of resource pipeline they knew that resources always needed to be
correct and able to be passed off to the next dev. While a dev is loading a
patch for an asset the dev could use a temporary resource, which would be
cleaned up during conversion by Jenkins. They also had a difference table for
packaged assets, prioritizing individual resources when a difference is
detected. This meant that artists only had to upload individual resources at
any given time. In the interest of stability, however, they automated
conversion with Jenkins, regardless of the resource.

There were 3 things they needed from the build pipeline: speed, frequency and
stability. For speed — resources could be loaded from the local PC, copying
just the executables and taking down the version number during build. For
frequency- main ROMs were built once every 5 minutes, building different
targets for different platforms at different frequencies as necessary (debug
versions would be built more frequently). For stability- build error
notifications would be sent to specific personnel, so you’d avoid a situation
where "someone needs to take care of it" — the person in question would get
right on it. They’d run smoke tests on hardware, and if something failed
they'd remove the ROM and specify who needed to fix what over chat.

They needed the ROM pipeline to couple with tasks so that devs would know
which ROM their work was reflected in, and they needed devs to get
notifications when a ROM was created. Jenkins would automatically update task
statuses so that the tasks themselves would serve as ROM build notifications.
In the end, the number of manual submits from the staff was 52%, while from
Jenkins it was 48%.

The final topic was QA, their starting point being that not only should the
build be bug free, but should also be fun. So QA’s role was to ensure that the
devs could perform as many reiteration loops as possible. So they focused on
reducing the amount of time it would take for devs to find things, and kept a
database of information for data, tools, tasks and devs. Queries were designed
to be easily performed by anyone, and information relating to the game field
would be plotted on the game map with the field task view — so it was easy to
get a look at overall completion rates for the game.

They had a "Game Over View" that showed where players experienced game over
the most, and chose to implement auto saves. Devs could also share queries
with the database viewer. Data experiencing problems could automatically
generate a task. Here they once again go in to the idea that they chose to
debug from the start — when they had their first test play they experienced
617 freezes in the span of 2 days. This is when they realized they’d need to
nip the problem of a massive bug count in the bud, even though the natural
reaction from members of the team initially was that if they had the time to
debug, they should focus on furthering implementation instead.

![a notification (perhaps build related?) pops up on screen in the game](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec32.jpg)

They merged their bug management and task management systems into the Zelda
Editor and held a team wide meeting to explain how to use it. They also
implemented a function they called “ZELDA_ERROR” to make problems more
noticeable. The programmers originally created this function in the interest
of preventing freezes, and in the end they had 6000 different ZELDA_ERRORs
strewn throughout the game. They also implemented hot reload so data could be
fixed on the fly. Being able to report bugs from the game was a great help for
debugging, and would automatically log the player’s coordinates, scene
switches, event and dungeon information. Based on that info the person who
found the bug could figure out who they should send the bug to.

![some error macros they used in code](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec33.jpg)

![a comparison of how the build looked in game versus on a computer](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec34.jpg)

![a demonstation of what the flow looks like when you find a bug](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec35.jpg)

The final two images here are notable — the first showing bug count graphs for
comparison. The graph on the left shows the bug count for a past Zelda title
(maybe Skyward Sword?), indicating the first spike being the E3 build, and
then the second spike being the final debug phase. The graph for BotW is shown
on the right.

![graphs of bug count in an old zelda game and in botw.  note that in botw, the curve is remarkably smooth](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec36.jpg)

This final images shows percentage of bugs and bug counts per source: red being from debug testers, geren from automatic tests and blue reported by the dev staff themselves.

![a pie chat of share of bugs found.  developers found the most, followed by automated tests, and then testers](http://game.watch.impress.co.jp/img/gmw/docs/1078/888/tec37.jpg)
