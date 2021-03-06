---
title: Control Loops
layout: coursepage
---

Control loops are at the heart of how robot programming works. There are simple loops, and there are complex ones. But they all fall under the label of control loops.

At its heart, a control loop is decently self-explanatory. It is a loop that runs continuously (although it can sometimes be disabled), to control some aspect of the system.

### Open-loop controllers
Open loop controllers are loops that do not take input. They cannot adjust to error, or react to any user or sensor feedback. These loops are less common in the real world, as they don't have a lot of utility in any precision task. But they are used in some applications, because of their low cost and simplicity. Things like timers, washing machines, stepper motors and sprinkler systems use open-loop controllers.

Typically, if you can answer yes to the question "Should this action be taken regardless of anything?", you could probably use an open-loop controller.

### Closed-loop controllers
On the other hand are closed-loop, or feedback loop controllers. These are much more interesting in implementation, because they compensate for error and randomness in the real world.

<div class="credited">
<p><a href="http://commons.wikimedia.org/wiki/File:Feedback_loop_with_descriptions.svg#mediaviewer/File:Feedback_loop_with_descriptions.svg"><img src="http://upload.wikimedia.org/wikipedia/commons/thumb/2/24/Feedback_loop_with_descriptions.svg/1200px-Feedback_loop_with_descriptions.svg.png" alt="Feedback loop with descriptions.svg"></a><br>"<a href="http://commons.wikimedia.org/wiki/File:Feedback_loop_with_descriptions.svg#mediaviewer/File:Feedback_loop_with_descriptions.svg">Feedback loop with descriptions</a>" by <a href="//commons.wikimedia.org/w/index.php?title=User:Orzetto&amp;action=edit&amp;redlink=1" class="new" title="User:Orzetto (page does not exist)">Myself</a> - <span class="int-own-work">Own work</span>. Licensed under <a href="http://creativecommons.org/licenses/by-sa/3.0
" title="Creative Commons Attribution-Share Alike 3.0-2.5-2.0-1.0
">CC BY-SA 3.0</a> via <a href="//commons.wikimedia.org/wiki/">Wikimedia Commons</a>.</p>
</div>

A closed-loop controller takes some kind of input, and provides an output according to the input given. The output inherently changes the external system, changing the input once again. This continues forever, in a continuous sense.

It is known as a feedback loop because it does exactly that - adjusts to feedback. For example, you might have a simple 4-wheel car powered by motors. You want it to go to a certain distance, but no further. You would want some kind of sensor that measures the distance driven, and take input from that sensor to dynamically change the car's output.

Even using time as an input is still closed-loop. In the previous example, you might not care about being exact. You could just make a loop that runs the motors for a specific amount of time, after which you turn them off. This is debatably not using "system feedback", but under most reasonable definitions is still a form of feedback control - using some kind of changing input to control output.
