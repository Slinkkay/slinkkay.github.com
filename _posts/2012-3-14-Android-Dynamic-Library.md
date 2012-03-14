
---
layout: default
title: Dynamic Libraries
---

Since I have been developing Java I had always had an issue with how dependicies
are handled. I am defining dependicies as other libraries which an application
relies on in order to execute. The more software I write the more I realize that
90% of what I am doing has already been done and I am just writing the glue to
make it an experience. Sure there are some original pieces which I am writing
but nothing which does not depend on other libraries. 

Java users will be very familiar with the utility called Maven. Maven is a great
utility in theory. If you need something just define it in some file and when
you go to compile your application Maven runs and grabs it from the interwebs.
Now you have your library which you can run at any point in time. However, when
you go to distribute that application you are basically distributing that
library with your application. So say developer A has an application that
depends on "the worlds greatest library" and developer B has an application that
also relies on "the worlds greatest library". When the user downloads both of
the applications they download that same library twice. 

Personally that seems to be waste. Now what if a bug has been discovered in that
same library. In order to propagate that fix to the user the developers must
re-compile their applications and re-deploy. Now I understand that some
developers work around bugs defined in a library. So fixing these issues might
cause issues in the running application. However, if you are counting on an
library mis-behaving perhaps you need to look at how your making your
application. 

Now Maven has some features in place to help combat the exact issue that was
describe above. Instead of just asking for the latest version of the library
Maven allows you to specify the library version. I do not see any reason why a
user side implementation of a Maven type system could not have the same feature.
Now allowing specific implementations of a library is very much like reverting
back to what we had before. However, it does centralize the dependicies to one
single location and file so there is some benifit.

The reason I started really thinking about this is the mess that Android has
gotten itself into with updates. My device runs Android. 2.3.5 because I rooted
it. Most of the reason I did that was so that I could get access to some of the
new Android APIs which seems to have little to no native code changes (also the
black bar is MUCH better than the old one). So as a user I would like for my
device to update anything that does not require native code to update at my
beckon call.

I understand that this might user more memory and might hurt my user experience.
Since the entire industry is about user experience companies decide to just not
risk pissing off the internets and not update the software. But that does not
mean that people should not have the chance to try out the new stuff and work
around the limitations of the hardware. Just setup the device to not update by
default but if the user goes in and agrees that they are running software which
is not "optimized" for their device then they agree as such. 

Now how would one implement such a system is a little beyond me right now. But
perhaps that is something I can post research about and it might work.
