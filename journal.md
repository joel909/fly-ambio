---
title: "FlyAmbio"
author: "Joel Joby"
description: "A basic Plane which flies 300km/h"
created_at: "2024-03-20"
---

TOTAL TIME SPENT : 40 Hours

##Day 1 (1-4 Hours)
Today I wanted to build something for highway so I went up and got a few ideas and I found out about building drones and it stuck a chord 
and i decided to make one later on during my reasearch on drones I felt I wanted to do something unique and I started my work with RC planes what made it cool would be that it would fly about 300Km/h Cuz i came across this really cool videa on yt. SO since I knew nothing I went deep dived into the topic and leared a few basics about this stuff wated tutorials and got a basic understanding about different kinds of mortor foams trasmitter battries and all sorts of stuff like that, I also started doing research about the design of the plane on how it would be designed and stuff i wanted a few vids and say a standard design which would have a propeller on the front and a wings and a flaps on those to move around and stuff also I got an intro about Airfoils and started tikering with it like on the site airfoiltools site.

##Day 2 (4-7 hours) I went and started learning about airfolis continuation from the last day I did a lot of study about how different airfoils impact the lift the speed and stuff like if u have a bigger cross section u can have lift but the drag is higher so it cant travel that fast but if its too thin it wont even fly lol, and i did all that after that i ran a few text based simulation i also spent some time working on understanding how to simulate and understand its readings so basicallly I took into account the frontal area the surface area and stuff and did some calculations to find a kida decent structure like i found out that mh43 from airfoiltools is the best for my use case also with 33% think neess not 100%
<img width="287" height="618" alt="image" src="https://github.com/user-attachments/assets/7e8c1a8f-9bb3-4a43-8dc1-7806af4fd35a" />



##Day3(7-10) 16th julyy MIDDDNIGHTTT so basically today was about thrust from the mortors to help me select the mortors i did some reasearch about static thruts (came across it as a problem in desgin) prop pitch and how these 2 make or break the aim for 300km/h also did some learning about rpm KV or mortors and stuff after I gained a decent understaning I made some calc and searched up mortos best for my case of 300km/h and i found a mortor for 2550KV but for some reason the propellor might not be able to hold it so i had to down grade and went for a safer option at 1950kv at 47500rpm with 6 cells

![AHH THE DESIGN I CAM UP WITHHH](<img width="306" height="643" alt="image" src="https://github.com/user-attachments/assets/bff12ae3-9a96-4c2b-92f5-470c5f3874cf" />
)

hours 10 -14  july 18th : I spent the time searching for different propellors and stuff and the making calculations based on it i went through some reddit posts and all that but turns out ill need a 14 inch one and i spent a lot of time looking at the site which had them they were available in the us but not in india so i needed to find a india specific platform to do this but i relaised that the popellor model i had found from alibabi was not right its pitch or something my friend told would not work so we got and started looking for more and then we settled one this one from robu
 <img width="502" height="674" alt="image" src="https://github.com/user-attachments/assets/ba81d2ba-5fc0-4e82-b088-643e1ee95b57" />
 minor change to design


hours 14-24: july 19th I spent this making my 3d model so I had no clue on how to make the air foil since obv idk and then i learnt that airfoiltolls gives me some co-ordinates I SPENT 2.5 hours trying to get that from just cor-dnates cuz I had to get the entire wing to my specifications so just traceing them would not help and + how much can i trace SO I DID SOME BRAIN STORMING AND MADE A AUTFODESK PLUGIN TO DO THAT for me and then i enterd the right values for it and it gave me hahahah soo happpy then i just had to exture it. then i had the flaps and stuff pretty decent took me a while to get them aligned perfectly since my pc was laging under the pressure of CAD running then I relaised hlf way through my design that it would be more aero -dynamic to strip the cureved cylinder like thing to just be flat that would increse the areodynamic and it would have reuced the drag
<img width="1133" height="624" alt="image" src="https://github.com/user-attachments/assets/9b280075-596e-45c3-a682-7236f6bd48e3" />


hour 24-30 july20 : i was looking for more inspiration and stuff on the thing and i ended up seeing this HJK thing and i compared mine to it and relaised mine to total shit so i sat and decided to make a few changes to make it look cool so a few changes that i made was that i modified the the hull design to be little more down to give that sharp look and then a few moment later i relaised that if i did thaet my battery would not fit in so i did one thing i would cut the center part of the rod to make space asthetics >> okay so u spent a good chunk of time figuring that out and then i moved the wings from the center to the top while doing that i landed at a discovery at the airfoiltolls site which i reilaise i can adjust the thinkneed and make my wings very thin obv it will be hard to take of first cuz less lift but the speed in air will be much higher cuz of low drag

hour 30-35 july 21st : i sat and made some calculations and it turns out it is true (my assumtions) and i needed a right combo beteen drag and lift and after going though more and more tuturial without finding the right intersection i landed at 20 or 30 would let my plane take of(just enough) and it would be minial drag i also considered a wing swapping desgin after take off too delusional right ik ik. and then i started with the schmatics also decided one a new flight controllers while doing that also i made the diagram for connection for the pcb to the battrey and the esc made the changes on the 3d model aswell

<img width="1268" height="518" alt="image" src="https://github.com/user-attachments/assets/221ccd38-f00a-40ce-9bdd-69510bcbb033" />


hour 35-40 : made chnages and i added servo mortors to the shematics i also added the mortor to the esc which in turn flight contorller i also plan on a comera so i was figururing out ways to mount that i also started doing some work on the 3d model it sccomodate the new wiriing and stuff, ALOS I RELAISE IT WAS  HUGE PROBLEM 
the cross section i had derived from had a wide frontal section even tho nothign could actually fit there so that space was just being lost so there was no point it would just make my plane less effecient so i did a lot of rework on my model almost build from 0 but this time i knew what do do so it  was quick
<img width="810" height="672" alt="image" src="https://github.com/user-attachments/assets/06950e21-6bd3-48fd-9d2a-e93436e8a72e" />
<img width="810" height="672" alt="image" src="https://github.com/user-attachments/assets/46fce8a0-0909-421b-bcf2-bd5a3c6326c0" />

<img width="741" height="661" alt="image" src="https://github.com/user-attachments/assets/8c067139-bd03-472f-afd8-60c9c987371e" />

