# Journal
---
title: "FlyAmbio"
author: "Joel Joby"
description: "A basic Plane which flies 300km/h"
created_at: "2024-03-20"
---

**TOTAL TIME SPENT OFFICIALLY: 40 Hours**

**TOTAL TIME SPENT unofficially: 80+ Hours**

^ includes those extra lunch breaks at school just looking for improvements!


```hour 1 and 2```

Today I decided to finally build something for hackclub highway so I went up and got a few ideas 

I already had a faint idea in mind, something related to rc... guess I never grew up from those toy rc cars eh?

But ofc, there isnt any fun in just building something someone else has already made, so I needed something new. 

I found [THIS](https://www.youtube.com/watch?v=vljy3lKIN-0) video online, and the brain wave ABOSLUTLY BLEW MY MIND. I knew what I wanted to make
I was gonna make an rc Plane. but not just any rc plane, I wanted to beat what was conventionally thought. I wanted to go FAST. 500kmph to be exact!

So I started my research, but looks like 500 kmph, was not exactly feasible to make on the budget that I had! 
Then I came accross [250km/h, Under 250 Grams V2
](https://lukeattubato.com/250kmh-under-250g-v2)
This was the first grounding source that I had, fully verified, and with a lot on info on how it was made. This was the starting point. The goal also had been moved slighly by now, targetting a speed of 300kmph (luke from the link above). I went though it throughly, and absorbed all the info that I could, learning from the mistakes he made, and what worked best for him. 


```hour 3-4```

on luke's website, he mentioned that his biggest inspiration was this guy called [MikeRX on RCgroups.com](https://www.rcgroups.com/forums/showthread.php?2921396-Minishark-Twinshark-build-experiment-UPDATE-250-GRAM-RACER-8S%21). This source turned out to be an absolute GOLD mine. He not only mentioned what he made, and what works, (This guy had been making these planes for YEARS), but the user interaction from other users there meant that every small detail that he missed was asked/mentioned by another user there. I had 1334 posts to go through. If I was going to make this plane, I needed to learn from the best, and MikeRX did look to be really good at what he did. 

```hour 5```

There was a LOT more info that I had anticipated, and took me a little more time to go through it that what I had expected. decided to finish reading it up, (there was another guy learning from mike's builds, so he had some usefull info int he same thread aswell), and then begin designing my own version of this daemon class rc plane!

# ``` ---> THE ELECTRONICS AND PROPULSION SYSTEMS```
```hour 6 and 7```
> So the first thing I need to figure out is the propulsion system. Did quite a bot of research, took me a while to get a hang of it. Turns out, unlike drone, propultion works  alot differently in planes. SInce they move so much all the time, 2 factors come into play. 
1. the static thrust
2. the top speed

>Static thrust gives us acceleration and is goverened by the rom of the motor, while the top speed depends on the "pitch" of the propeller, which is how much the plane moves forward per rotation of the propeller. If you have too much pitch, the motor will be overloaded for not being able to provide enough torque, will spin slower, and will burn, but if you have too little pitch, then the plane will have a very slow top speed. I have to find a balance between these 2, and find a motor that can take maximum load without heating too much. 

```hour 8```
>Then I figured out fianlly what the Kv rating on a motor really meant! It gave us the unloaded rpm of the motor per volt!
>A little browsing later, I had found what motor I needed. The F80Pro, rated at a whooping 1.2 Kwh!. It had a proven track record from [Drl's racer x drone](https://www.drl.io/racerx), But there was a catch. It was not availible at 2500 Kv anywhere in india. out of stock everywhere(almost). One site did have them, robokits on preorder, but they didnt accept international cards. So i had to settle for the iFlight XING 2203.5 motor, which was similar. I decided to give a call to robokits india afterall, and they had a new pellet of shippments ariving soon, and they told me they could add F80Pro motors on it on a special request. I decided that I would figure out the paying part later, and placed the order for the motors. 

```hour 9```
>Now that I had my motor decided, I had to find a good battery for it. Now this was very tricky. I had understood from mike and luke's posts that I needed atleast a 6s battery, meaning 25.2 nominal voltage, so that I could sping the motor to around 43000 rpm loaded. But these battries where hard to find. We need LiPo battries to get the maximum current, while being light. however, finding sites who sold these battries from repulatble sellers, and also accepted american cards was a piece of work... Finally found one that works for me, and decided to go with it, a 1100mah 6s battery, capable of delivering 110 Amps bursts. at 25.5v. should be able to handle what we throw at it easily. 

```hour 10```
>I already had in mind what flight controller I would use, had come accross it while searching for battries, so that was good I was goign to use a speedybee f405 wing running INAV to stabalise that plane, and make it easier to fly. also added servos while I was at it, but had to change the servos a little later for ones that could take more load, isnce we were going pretty darn fast.

```hour 11 and 12```
> I needed a GPS module now, to keep track if it got lost. there were a lot of options, but most of them were far to expensive to make sense. FInally I did find one that ran a slightly old algorithim, but if it works, it work!
> Had to get a way to talk to the plane, ofcourse, so I chose ELRS firmware based RX and TX units. They are very popular, and have known relaiability, and not too expensive like DJI systems. Sounds perfect. Finally found a rx and tx for my elrs setup, the cheapest I could find that still worked for my usecase. 

```hour 13 an 14 and 15```
Yes. You read it right. It actually took me more than 3 hours to find the right propeller, but I will only log 3 here. 
> I first went to mike and luke's blog to see what propeller size and pitch to use. also ran quite a few text based sims to find the optimal pitch so I can reach the target speed, and the right diameter so i dont overload the motor and burn it.
Finally settled with a 5x5 propeller, meaning 5 inch diameter, and 5 inch pitch. I will later modify this propeller like how I had learnt in those blogs to make it a 4x5 propeller and recude the load furthur.

```hour 16 and 17```
> WHY DOES NO ONE WANT TO SELL/MAKE GOOD PROPELLERS IN INDIA???
> FPV dosent have a very big market in india, so there arnt really many people who make and sell these propellers that I need. now keep in mind, I cant just use a normal plastic propeller. at 43000 rpm, a propeller will be experiencing a LOT of centrifugal force on it.
> as adviced and proved by mike, I needed a good propeller made from polycarbonate( similar to carbon fiber, but a composite using other materials along with carbon fiber).
> I wanted APC or German prop propellers since they are good reliable companies, but I had to settle for some locally sourced onces, since not a lot of sellers seem to import those proppellers into india, for the lack of market for them.

```hour 18 and 19``` 
> Now that I had most of the powersystem in place, I could finally look at some prospective escs to run the bldc motor, since these motors required a 3 phase AC input rather than a simple DC, so make them more efficient, run at higher rpms, and take that title of being drone motors!
> I decided to take into account that its going to go througha  lot of crashes initially, and I need a reliable escs that can take those hits. There were only 2 good choices, since we needed racing escs to be able to 
1. handle 6s
2. handle the intense stress of moving a prop with sunch a huge pitch
3. be very responsive and fast, since at those speeds, a second of delay is around 83 meters propelled forward.

>These escs were however very expensive. So I found an alternative, I found out that DRL had a branch in india called IDRL, and they had a MASSIVE store of second hand parts! unfortuanatly most of the parts are made for drones, but I did manage to find Formula f45 Emax racing escs imported from USA, barely used, which were perfect for the job. 

```hour 20```
>Now I needed the basic materials to make the plane. I searched a lot, but either sites were selling the materials at EXORBITANT prices, or they simply did not keep them in stock. I even called a couple of the biggest manufactures in india and asked the materials, but they refused to sell such small quantities of foam, balsa and other parts that I needed. However, when almost all hope was lost, thanks to a couple of active redditors, I came accross [vortex rc](https://www.vortex-rc.com/), and they seemed to have practically all I needed to make the body, including the carbon fiber rods, at veyr good prices.

```hour 21```
> I spent the next hour just finding the other small things that I needed to make the plane, some epoxy, 16 AWG silicon wires, XT60 connectors, brown paper at 150gsm, some nylon screws, solder, etc. I wanted to make sure I wasent forgetting anything.

```hour 22 and 23```
> Now for the fun part! (not so much)
> One thing that was COMPLETELY new in my design, was that no one else seemed to have been putting FPV into their planes, purely to save on weight. but with that bigger battery, I could afford to put in 20ish grams more without loosing too much speed. 
> I needed to however save as much money on these as possible, as the plane was already getting rather pricy. So i sacrifisede quality a little bit, and went forthe chespest parts I could find. This took QUITE a while, since I had 2 objectives to clear
1. finding the cheapest possible parts
2. Finding them on sites thats accept international cards.

>overall, I think I did alright with the electroinics and the propultion systems. 

>as per requirements, I make a couple of schematics on how everyting will be connected together as a schematic


INSERT IMAGE HERE



# ``` --->   THE OVERALL DESIGN```

```hour 24 and 25```
>Now that I had the size of my parts, I need to figure out,  what is the overall dimentions of the entire thing? Again, Mike's blog is plently usefull, but I want to try something new. I want to add a slightly bigger battery for more flight time, and make it more durable, since his balsa planes would absolutly shatter apon impact, and i am still a rookie flyer. 

INSERT IMAGE HERE




>Phew! That definitly took a lot longer that I wanted it to, but I want to get it right the first time round...

>I now have a basic idea of how my plane is gonna look, and its starting to show!
This step has required me to use the free credits from not just 1, but 2 chatGPT free accounts, to Verify is it looks about ok, and for making the frontal area and wing area calculations faster, since chatgpt is sooo good at math, definitly dosent halucinate all the time ;)
asked chatgpt to run a couple of sims aswell to see how well it thinks the plane would perform, and made a few tweaks according to suggestions.

>**I will take my design to a friend at school who has made something similar later, just to get that final satisfaction that it will fly.**

>```I know I verify too much, but i'm a measure twice cut once typa guy!```

>spoiler alert, this is NOT going to be the last time I have to modify the design...




>Got my design vetted by the frined at school, looks like its ready to proceed with the next step!

# ``` --->   THE MAIN WING```
```hour 26```
>Mike mentioned that he had sanded down his airfoil manually, but while that worked for him, I wanted to get this thing done the right way so took a couple lessons from chatGPT, and after verifying from a few more sources online, looks like MH-43 is going to be the perfect choice for this build. its thin, got low lift, very little frontal area, and super efficint at high speeds. as I said, perfect. 
Verified from the pics Mike sent on scaled mats, and decided to use a modified MH-43 airfoil. I was gonna use a 33% MH-43 airfoil, meaning that the thickness of the wing was going to be 33% of the origical MH-43 airfoil, therefore reducing frontal area, and hence the drag aswell. Found the airfoil at [airfoiltools.com](http://airfoiltools.com/airfoil/details?airfoil=mh43-il)


```hour 27 and 28```
>So now I have to get started on my CAD fo the main wing. I had found my airfoil and I knew the thickness that I needed, but uhh that was about about. So I checked how I can export that airfoil from the website into autodesk fusion 360, and It seems to give me a ```.DAT``` file with just the coordinates for making that airfoil... Oh come on man! wheres the CAD importable file format??? I started to trace the thing out manually instead, but 5 min in and barely anything done, I knew I needed a better way to get this done.



```hour 29 and 30```
>So I did the next logical thing that anyone would do...
I WROTE A AUTODESK PLUGIN JUST TO MAKE THAT AIRFOIL! So I wrote the code, uploaded that file, and clicked on. Belive it or not, IT WORKED! I swear to god I laughed for a solid 2 minuites... It was fianlly done! I now had the outline of the wind that I wanted to make, and it was time to get started on the actual thing!


```hours 31 and 32 and 33```

>I loaded up my file, and extruded that wing. what a beauty! Now I had to cut out the flaps for that wing, curve some corners, and get everything aligned right. 
But ofcourse, nothing is ever just as easy as I want it to be, now, is it? My PC was lagging to a point where moving the mouse too a second... (someone please donate me a GPU UwU)
>I realised half way through my design that it would be more aerodynamic to just strip the curved cylinder like thing and make it flat. That would increase the aerodynamics, and it would have reduced the drag at high speeds. 

```hours 34 and 35```
>OH SOMEONE PLEASE HELP ME!!!
almost threw my house at my laptop. I HAD FORGOTTEN TO GET THAT 33% AIRFOIL FROM AIRFOILTOOLS.COM, AND HAVE TO DO THE ENTIRE WING AGAIN. WHAT SINS DID I COMMIT IN MY PAST LIFE TO HAVE HAD THIS DONE TO ME??? 😭

>So with a very pissed off brain and absolutly no will to make it again, I did it. I made the entire wing again, with all the flaps, all the alignments, all the right corners, and had to go thought all that Lag all over again. suprisingly it look a lot lesser time to make it, since I already knew exactly what I needed to do. 

>In the end, I Finally have my wing ready, but I am too tired to  work more on it for today.

```hours 36 and 37```

> Its a new day, and time to make new mistakes!
I started off with the main fuselage body, and a little while later, the thing was actually starting to look like more than just a plank of wood. It looked like a giant Holy cross! We were finally getting somewhere.

```hours 38 and 39 and 40```
> So I finished the rudder and the horizontal stabalizer, I have the same airfoil for both of them as that of the main wing, it seems perfect, however the stabalizer has a 50% airfoil rather than a 33% as used by the mainwing, since at 33% it was far too thin. Same goes for the rudder wing. I decided not to have a flap on the rudder, as it didnt bring too much stability to the plane at that speeds, and a an extra servo increases weight. 

```hours 41 and 42```
>I put in the rest of the small details into the cad, the front motor, the propeller, and a couple of more details, trying to finish off the 3d model today. 
>Took a little longer than expected, had to work a few small errors in the model, and ofcourse, my PC wasent exactly trying to help me out :) but at this point, we finally have most of the 3d model ready! It looks like an actual plane now! super excited to actually build this now!

```hours 43 and 44```
>looked up more about INAV, the controlling firmware for our build, to help with getting the plane back if its lost, giving back telementry so I know when the battery is about to die, and ofcourse, to find out the actual speed at which its flying!
>Searched up what settings I needed to enable, and tinkered in their IDE for a while to get familiar with it. 

```hour 45```
>With everything almost ready, I decided to join a couple of discord servers full of people from everywhere, and asked for some tips, made a few tweaks, and looks likes it should now be ready to go!

```hours 45 to 49.5```
>belive it or not, formating and making this Journal too a LOT of time... I have tried to include as many details as possible, and logged all my failures, and successes. Hopefully this makes the cut!


    PS: This turned out to be a LOT of fun, so stay turned for a complete build log aswell!!
