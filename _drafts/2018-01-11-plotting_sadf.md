---
published: false
---
## Plotting sadf

Sysstat, Postgres and dumb terminal.  

### And there was light

The sysstat package, which can be found on many linux based servers nowadays is very usefull. 
It can collect data about what is happening to your CPU, RAM... (http://bencane.com/2012/07/08/sar-sysstat-linux-performance-statistics-with-ease/)[Here is a good start.]

I won't get into specifics today, this is not the point. I would like to present it from the database perspective. It's all about persperctive. The Postgres user can access sysstat informations. And more interrestingly everything collected by `sar`. 

Sar can help you know what is going on right now and what happened in the past, since it collects information for each day of the month. It's a pretty big tool and a database administrator who is not acustomed with sysstat can very easily get confused. As opposed to NMON, you don't need to collect information to get a csv report or stream the collection live. This is more a forensic-like investigation type of tool.

So first let's use something much easier to use : `sadf`. Sadf works the same excepts it only gives information about each day of activity and can be exported natively in CSV files. 

### CSV you say ? 

Yes, you guessed it! You can graph that very easily too.

Imagine, you have no GUI, no graphs, no monitoring... Well, sometimes that's my case. 
Imagine, you cannot get any money to pay for the expensive fancy tools... (you might not have a say in that)

How can you graph things easily ? Well GNUplot can do just that for you, for free.
In case you didn't know, you can even graph in a linux terminal. 
The most basic being: the dumb terminal. 

(https://github.com/emerichunter/plotting_sadf/raw/master/sar_cpu_dumb.PNG)[picture of dumb term]
(https://github.com/emerichunter/plotting_sadf/raw/plottingsadfv2/plotting_sadf.PNG)[same with colors]

And the next thing you can do, when you have export display on, is use x11 terminal
[picture of x11]

But you need to get everything to work, and not spend too much time on this endeavor. 

So let's get a tool to do just that... Wait! I just made one! 


### Enters the Savior

Some time ago, I made this tool and recently I made it more dynamic so that it can take many different options. Because sometimes, this kind of things can help. 
If you are poor, you have nothing and no one is there to help you or provide you with any tool, this might save your life... or save you from a lot of trouble at the very least.

(https://github.com/emerichunter/plotting_sadf/tree/plottingsadfv2)[link to git]

### Deaf, dumb and x11

Well, with this you can also graph in .png. Graph any day of the month that you wish to see. 
Change the size of the display and even add colors to your terminal.
You can use X11 and png formats they both have been invited to the party!

I might add some reports in the future, like network stats, but this will do for now.
Enjoy!
