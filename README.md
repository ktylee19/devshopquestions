About this app
--------------

This is a help queue to be used by MIT students in 6.01: Introduction to EECS.  

(This is a modification of the questions app used on Montly Meteor Devshops in SF.  For original project, go [here](https://github.com/meteor/devshopquestions)

There is one design lab and one software lab session each week, where students 
collaborate in order to complete their given labs, after which they receive a 
"check-off" from a lab instructor, teaching assistant, or lab assistant. 

Instead of having students raise their hands in order to receive help and check-offs from the instructors and assistants, a help queue was create in order to provide help to the students during the session.  This creates a fair, queue-based system so that students are not wasting theiri time following instructors adn assistants around the lab and that all students get equal opportunity for attention.  


Questions
---------

Each question has a one-line description of their problem and the question. We
encourage users to put their real names and their location within the devshop so
someone can find them to answer the question.

App allows users to login with their GitHub account to have a control over their
question if they want to delete it or to mark as "answered". Also the app would
auto-fill their name from GitHub as well as their user picture.

Question can be marked as answered, deleted or edited by the creator or an admin.

App allows anonymous questions and questions by guests just in case the asker
doesn't have a GitHub account or doesn't want to share it.

Banner notification
-------------------

There is a small one-line banner notification from devshop organizers on the top
of app interface. Usually it is about something happening on the event right now.

Examples:

    There is a skeeball competition upstairs! Be sure to post your highest score!

or

    Free flushots are on the second floor!

Admins
------

Admins can modify/delete/mark as answered any question. In addition admins can
flag the question as "difficult" to ask for more help from core developers.

Admins are configured in http://helpq.meteor.com/admin panel and
added by their Kerberos usernames.

Deployment
----------

For some reason jquery.more plugin works incorrectly when all js code is
minified and concatenated. Right now, I deploy with `--debug` option.

Update: the real story is about CSS minifier. We were hitting some random bug
with minification of bootstrap theme and jquery plugin. The minifier update
landed on devel which will fix it. Whenever there is a new
template-engine-preview release with the merge of 0.6.4 or 0.7 - it will be
fixed.