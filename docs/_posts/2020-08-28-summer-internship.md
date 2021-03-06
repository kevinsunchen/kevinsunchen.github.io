---
layout: post
title: summer 2020 @ Cambridge Electronics
---

![headerpic](/assets/images/ceiheader.PNG)
<small>*layout visualizer - giddspy*<small>

this summer i had the opportunity to intern at [Cambridge Electronics, Inc.](http://www.gantechnology.com/){:target="blank"} as a software development/device modeling intern. CEI is a small power electronics startup based in Cambridge, MA that specializes in creating "3DGaN technology" -- gallium nitride electronics that utilize a 3D structure to achieve better performance. i can't really get into specifics since, as a remote intern, i was pretty far removed from the physics/electrical engineering nitty-gritty of it all; my role revolved around creating software that helps the engineering team better design, test, and generally mess with the electronics.

overall, i think this internship was a pretty positive experience: i created a product that i think is pretty rad, learned a good amount on a diverse range of topics (mostly non-technical!), and was fortunate enough to stay safe and stable throughout it all by working from home. this post will serve as a sort of explanation/record/reflection of that experience; hopefully as i write this i can think about the growth and missteps i made this summer, and hopefully in the future i can come back to this post and reflect on the growth and missteps i've made from now til then.

but before i get into more detail below, a brief explanation of my project: basically, the tools and processes that CEI was using for creating/modifying device designs were fairly clunky, pretty tedious, and prone to error (which is not ideal for electronics since the process of sending something to a foundry, getting it on a silicon wafer, testing it, etc. is quite laborious and expensive, i'd imagine). my job was to create new tools to overcome those hurdles, and my solution was "giddspy" (**G**raphical **I**nterface for **D**evice **D**esign with **G**dspy).

a not-so-brief overview
----------------------

first, a rundown of the background details and logistics of my internship.

i interned at CEI for 3 months, from June 1st to August 21st, working from home. my official hours were the standard 9-5, 40 hours per week/8 hours per day, but in reality this was more flexible due to remote work; i finished with 472 official hours. i was paid monthly through the Gusto online platform. i had one direct supervisor, Dr. Harbing Lou, and was the only intern working on this project. my supervisor's role was more managerial than technical; it was expected that i own this project from start to finish, and all technical and design choices were ultimately left up to my discretion.

i met with Dr. Lou at 5pm Eastern every day. these meetings were daily check-ins/briefings; usually we would spend around 15 minutes discussing things like the progress i made that day, anticipated challenges and potential solutions, things to do next, etc. if there were more complex issues to hash out, meetings would go longer, usually to about an hour. we also had occasional "customer feedback interviews" -- essentially, when i reached appropriate milestones, we would schedule a meeting with the engineering team (which was the bulk of CEI, including the CEO) to either

1. demonstrate what my program could do and get feedback on what they think it should do,
2. having sent them a copy of the program a few days prior, get their feedback after trying it out,
3. some combination of the above.

after these meetings, i'd incorporate the feedback into the project alongside working towards new milestones and implementing my own fixes and improvements. 

i also had a "side task": importing some of the company's existing device layouts from the various representations they were before (Python scripts, GDSII files, etc.) into my program. this was an interesting process; i was basically testing my program on real future use cases as i was writing it. this back-and-forth of being both developer and user really pushed me to constantly generate ideas on adapting the program to be more intuitive, flexible, and functional. it was also oftentimes frustrating -- a lot of improvements to the program would render previously-imported layouts incompatible in some way or another, so there was a lot of redoing and patching on that front too.

as the summer drew to a close, i had a few final goals/milestones to wrap up:

the first was obviously to produce the final, polished version of the program so that the engineering team could start using the final product right away. they had been tinkering with various prototypes/in-development versions over the course of the summer, so at this point, they had a pretty good idea of how the program worked, what to expect from it, and what they wanted it to do.

the second was writing documentation for the program (which i used Sphinx/ReadTheDocs and ReStructuredText for) -- both user documentation and code/API documentation. this was a pretty time-consuming task: on the user side, importing the layouts and using my own program all the time made me pick up a lot of tips, tricks, and useful info that i wanted to share in the docs; on the code side, there was just quite a lot of code. and the implementation choices i made in some places were probably pretty confusing/perhaps even dubious at times. and on top of that, i needed to document the program's API that allowed users to run some handy things in a script, which brings me to the next task.

the third task was to produce an example script utilizing the program's API to essentially automate the process of putting together multiple device layouts into one big multi-layout GDSII file, which would then be sent to foundries for manufacturing (more detail below).

the last task was a final demonstration + presentation to the engineering team and the CEO where i discussed various aspects of my work, including:

- what i achieved over the summer and the final state of the project
- the motivating goals behind the project, how they shifted over the creation/iteration process, and what i did to reach them
- strengths/weaknesses of the program and how i envisioned it'd fit into the company's workflow for maximum effectiveness
- design and implementation challenges i faced and the solutions i came up with, either to address them or to work around them
- future work to be done/improvements to be made

and so on 8/21, my first summer internship officially ended. i had given my final presentation to the team the day before; my last day was mainly just finishing up the other tasks and doing one last meeting -- or "exit interview", as he called it -- with Dr. Lou. i demonstrated and explained the script i made for the third task, updated him on my status on the other tasks, and discussed my summer experience with him. with that, my last official day concluded -- except i spent the next 2-3 days finishing the documentation and further cleaning up the code before finally sending in the final version.

after 3 months, 472 official hours and an unspecified number of unofficial hours, and idk how many lines of code, i was done.

the project
-----------

the project itself consisted of a two main components, the GUI and the API. for most of the summer, my work was focused on implementing and fleshing out the GUI, since this would encompass the bulk of the functionality needed for the API as well. as such, the code was structured so that modules/classes powering the GUI's backend could be used independently by importing and calling appropriately.


reflections
-----------

in progress -- check back soon!
