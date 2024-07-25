I did not invent this, it says it on the official Offsec website and oh man, they are not kidding!

![oscp_1](/images/oscp1.png)

With that said the reason I decided to make this write-up is to share my experience during the preparation and exam for the OSCP or PEN-200 practical hacking certification and well to make that journey through hell a little more comfortable for you ;)

The course covers a wide range of topics, from information gathering and vulnerability scanning to exploit development and post-exploitation. It also includes a section on Active Directory attacks. As a good friend of mine told me: “The OSCP is a 100-meter-wide trench that is only 1 meter deep.” Try to keep this in mind as you will have to come back to this thought many times when things get fuzzy, believe me.

Honestly speaking the certification aims to prepare anyone with some decent networking knowledge to a beginner level penetration tester level. And as much as it hurts (I know, I’ve been there) it is a professional, yet still a beginner level certification. Why is that? Because there are no evasions needed. You only need to watch out for some firewall rules; however, this does not mean at all that this exam is a breeze to go through. Even people with some years of pentesting experience have failed miserably on the exam, so don’t take it lightly!

Also please keep in mind that the above task from the company’s perspective is not an easy one! There is so much an Offsec student must learn during the course and in a very limited time frame. This combination opens a lot of questions, so let’s talk about time management first because based on my conversations with other students I feel that this is where most people fail.

If you go through the course syllabus and realize that most of the topics are already familiar to you, then you will have an easier time for sure, however if that’s not the case, brace yourself because you will have to spend countless hours practicing the course material in the lab. If you know how to port forward, pivot in a Linux and a Windows machine as well, that will definitely help you a lot along this journey. Of course, the course will teach you how to do all that as well but once you start it, you are on the clock! Especially if you purchased the course with the 90 days lab access. So, to give a better structure to this write-up, let’s talk about the options and how to take full advantage of the practice lab and what other resources you may need while prepping for the exam.

## The good, the bad and the ugly
At the time of writing this article the 90 days lab access for the PEN-200 Course & Cert Exam Bundle goes for $1,599 USD, this includes one exam attempt as well. You could extend your lab access if you ran out of time and could also purchase another exam attempt if needed. Both of these options are somewhat pricey. Especially if we compare the price with other trainings and certs but Offsec definitely has a big name in the Cybersecurity industry and that is why they can charge what they ask for. Anyways, I’m not here to compare prices instead I would like to help you out with a couple of tips. I actually ran out  of the 90 days lab time, let me explain why. This has to do with the exam structure and scoring system. You see the exam is proctored and you have 24 hours to pass. You pass the exam if you complete any of the below scenarios:
* 40 pt AD + 3 local.txt flags
* 40 pt AD + 2 local.txt flags + 1 proof.txt flag
* 40 pt AD + 2 local.txt flags + bonus points
* 40 pt AD + 1 proof.txt + 1 local.txt + bonus points
* 3 fully completed non-AD machines + bonus points

Now the bonus points will take you time to earn them and once you started the course you also started your lab access, so please consider this: you have 90 days to go through the training material (learn as much as you can), complete the exercises required for the bonus points and also try to finish the practice lab machines. And before you say: “I don’t need the 10 bonus points.” Allow me to call your attention to a little detail that I’ve seen on the forums (Offsec gives you access to the forum where students can discuss topics about the lab, not the exam, and there is also a Discord channel.) where students are really sorry that they had not completed the required exercises because after a failed attempt they realized that they could’ve used those bonus points on the next exam. To pass the exam you need to get 70 points and if you take a look at the scoring system you will notice that without the bonus points you either complete the AD machines where you get no partial points, so you get to Domain Admin or you get 0 points, or you need to complete all 3 non-AD machines + bonus points or else you will fail the exam. If you don’t have your bonus points and cannot complete the AD set, no matter how many standalone machines you rooted you are done.

Of course you can just buy the 1 year subscription and do all this nice and comfy but that also comes with a hefty price tag of $1,999 USD. If you run out of lab time and need to buy an extension for another 30 days (yes, 30!) that will cost you another $359 USD.

![oscp_1](/images/oscp2.png)

Oh by the way if you take the exam (because why not, I might not need to do the rest of the lab machines anyways, I think I will pass…) but if you don’t, you will also need to buy another exam attempt for $249 USD. Sweet…

![oscp_1](/images/oscp3.png)

You see where I’m going with this? If you actually run out of your 90 days lab time, you would’ve been better off just by paying for the 1 year subscription. Most definitely if you don’t pass the exam you would’ve been better of just by signing up for the 1 year plan. And because I went through all those pitfalls let me give you some tips I learned on the hard way in hope that you can avoid falling into this rabbit hole. One more thing I would like to point out, this is not to hate on Offsec at all. I truly think that teaching people how to hack into systems on both Linux and Windows, Active Directory, finding exploits, fixing exploits (you may want to go through this section very carefully in the training material when you get there) and how to apply critical thinking is not an easy task for sure! This is for you to you understand their game plan and business model. We are hackers, we learn and adapt.

## The game plan
So you’ve decided to go for the glorious OSCP cert and looked up some reviews and eager to start, right? Well, not so fast! 

First off, think this through, please: the preparation for the OSCP is not a sprint, it’s a marathon. You will have to put some serious hours in for a long time, for months, for many months. Most of us have a day job or school and other responsibilities so I recommend calculating at least 3-4 days per week 3-4 hours per day to dedicate to your preparation. And that is why we will not start with the OSCP course. We don’t want to be on the clock right away.

## Phase one - pre-learning
If you are absolutely new or have little experience in hacking or even if you just want to be better prepared buy 2 courses from Udemy. Both courses are from Tib3rius and 1 more course from TCM Security the PEH (Practical Ethical Hacking) which I think was released for free on YouTube. Go through them and take some good notes! I’m not going to be talking about note taking as I advertised that very much in my CRTO article but I recommend using Notion. If you are already familiar with the topics in aforementioned courses move on to phase two.
* TCM Security on YouTube  (search for the PEH course) : FREE
* Udemy: Windows Privilege Escalation for OSCP & Beyond! : approx. $20 USD
* Udemy: Linux Privilege Escalation for OSCP & Beyond! : approx. $20 USD
* Total investment : approx. $40 USD
* Approx. time frame for completion: 3 months (dedicated)

## Phase two - HTB
Sign up for HackTheBox VIP. Yes, VIP membership. This is so you will have access to retired machines and guides. At this point I would like to mention that it is a good idea to create a HTB lab section in your notes because oh man, you will have a lots of notes and it will come handy later on when you can refer back to them. The following is a list of machines that are highly recommended to complete before the OSCP exam. There are many variations of this list out there, you can Google them if you want to but this is the one I did and even though the machines changed a little since I’ve taken the exam this is a good core-list of boxes that will teach you different techniques that will be useful during the exam. And I did the AD version of the OSCP exam, but we will talk about that later. The VIP membership at the time of writing this review is $14 USD a month and you will need probably 2 months before completing all the machines, but your time may vary. 
* Approx. time frame for completion: 2 months
* Total investment: approx. $28 USD

![oscp_1](/images/oscp4.png)
Credit goes for @TJ_Null on Twitter (now X).

There are several other lists, updated lists if you search for them however I think this one is still strong. I used Cherrytree (built into Kali) at the time of prepping, now I would just use Notion because the notes look good even in the mobile app and I could pull them up anytime I wanted to review something. (Like at 2 AM when you can’t sleep because you’re brainstorming on a machine you got stuck on, the struggle is real 😈 ) And look, I’m not kidding, here is a snapshot of my Cherrytree notes from back then.

![oscp_1](/images/oscp5.png)

What I also did was (I painted it out on the screenshot) that I make a small note next to the machines’ name with the description of the exploit so I could search back for it if I encountered a similar situation, like the zone transfer for example.

## Phase three - the OSCP lab
Here we go, finally arrived to the OSCP lab! If you did phase one and two then you are in this preparation for about 5 months now, congratulations! I told you it’s a marathon, not a sprint. If you were already familiar with above preparation phases then this section will still give you some very useful advices, keep reading 😎

Once you purchase the course, try to go through the training material as fast as you can and take notes, good notes! Honestly for the money of the PEN-200 course they could’ve done a better job at putting the training course together but if something is not clear right on the spot, just Google it or refer to back to the courses from phase one. It will help. This shouldn’t take longer than 2 weeks, 3 the most and you will have enough time to spend in the lab, don’t worry. You may not complete the whole lab but that is not an issue either, I will explain later why not.

Also if you decide to go for the exercises, (I think you will need to do write-ups on a number of machines from the lab, not sure how this works now days) put that plan away for a moment and head straight to the Active Directory machines! This is important because in most labs you will not be able to practice in an AD environment! Everything else you can practice anywhere but this is where the value of the lab access lies IMHO. First of course you need to find the AD sets but if you’ve gone through the training material and the courses that shouldn’t be a problem. Hunt them down, take notes and start exploiting them. If you really, really struggle don’t worry, keep it simple and get away from the keyboard from time to time because tunnel vision is real! (Also learned that the hard way.) Always remember: a trench that is 100-meters-wide but only 1 meter deep. (I wish I had come up with that 😬😎👌) If a tool doesn’t work, find a different tool, if an attack vector doesn’t work, find a different attack vector. Don’t try the same commands and tools over and over again if they don’t work. That is not what the Try Harder approach is about. Trying the same thing over and over again expecting a different result is not what the Try Harder mentality is all about, that is the definition of insanity.

![oscp_1](/images/oscp6.png)

Great, so we finally got to the lab and found our AD sets! Let’s enumerate and attack them, right…? No. ⚠️➡️ Revert the machines first. This is very important as (unfortunately) this is a shared environment. Meaning that multiple people are trying / or tried to exploit it or alter something in it if they can. This means that you need to revert the machine and start enumerating it in a pristine state. People who are already working in the lab will hate you for that and you will hate the newcomers as well when you are in a double pivot and someone reverts one of the machines but it is better to do it that way than just banging your head against the wall because someone changed the password for one of the users and now you can’t crack it and that would be your only attack vector to move forward. This is of course just and example but it literally happened to me in a different lab from a different company. I’m all about positive attitude and love but if there is one thing I really hate in this world is shared lab environments 😂. Just kidding, or maybe not…

This is what it is, and as I mentioned earlier you will need to adapt. Once you completed all your AD sets and took good notes, move on to the stand alone machines but be aware that some of them have dependencies (thanks Offsec) so you may get up to a point in your exploitation and get stuck because you need to exploit another machine before your can move on, or the same situation but you can’t even get a foothold on the machine for the same reason. Create a separate section in your notes for the credentials you gathered and try to pass them around in the network. Think of the lab as a network, not individual machines, do not try to exploit them in sequential order, it won’t work. The AD sandbox is really good to get some AD practice. But again, go back to the basics, you do not need to reinvent the wheel, it is just some basic AD hacking with limited number of hosts in the sets. Also Offsec provides detailed write-ups of two machines Alpha and Beta. These write-ups are insanely good to provide you with a guidance on methodology!

If you have troubles in the lab you can also ask the admins on the forum or on the Discord channel. My experience was that everybody from the Offsec staff was really kind. Even when I had issues where I had to email them, their response time was really fast.

With all that said prepare for a really hardcore hacking experience filled with some joy and happiness and countless hours of research, frustration and crying. Coolio was not wrong at all:

As I walk through the valley of the shadow of death

I take a look at my life and realize there's nothin' left

'Cause I've been blastin' and laughin' so long that

Even my momma thinks that my mind is gone…

## Phase four - lab time runs out

![oscp_1](/images/oscp7.png)

If you have completed all your lab machines before your time ran out skip this section. You are more than ready to take the OSCP exam. Of course if you did all that without pass-around write-ups which is of course unheard of…  I hope you didn’t do that as it will hurt you on the exam, this is something you’ve never experienced before and no copy-pasting will work no matter how many machine write-ups you stack up in your inventory. We do machines so we learn, polish our methodology to be able to break into machines and avoid rabbit wholes. I usually encountered two types of machines, the first ones with a lots of ports open and I knew I was in for a treat 🤣, the second one were the ones where only 2 or 3 ports are open and man, I went straight for my helmet to put it on because I knew I will be banging my head against the wall for hours. 

Anyways so not “if” but **when** your lab time runs out, do not extend your lab. Don’t worry I did that one for you too :) What you wanna do is head straight to the Offsec - Proving Grounds lab. Not the free one (PG Play) because those machines are way easier than what you will encounter on the exam. You want to sign up for the PG Practice lab for a month. That lab is going around $19 USD / month. Sign up and do all the Windows machines (not many of them but they are good) and then finish up your remaining time with the Linux machines. There are several reasons for that. The most important is that the “style” of these machines are more Offsec exam-kind-of-like. You want to pick the machines by author and pick the ones that were made by Offsec. The other reason is that these are not shared machines, you get to fiddle around with your own dedicated instance, and third, there are hints and walkthroughs available for each one of them. When you sign up for the PG Practice lab that is a good time to schedule your exam. A month ahead. Don’t worry you can always reschedule but if you went through all the different phases you should encounter no issues with attempting and passing the exam.

## Phase five - the exam
Up until now if you followed the game plan you have completed the following timeframe and spent around $87 USD on top of the course price:
* pre-learning courses / 3 months / $40 USD approx.
* HTB practice machines / 2 months / $28 USD approx.
* PG Practice lab / 1 month / $19 USD approx.
* Offsec PEN-200 lab / 3 months / included in course price

After 9 months of practicing day and night the time for the truth has finally arrived! Your exam time is scheduled, your notes are in order (they better be) and you are ready to take on the beast! 

The proctors are (according to my experience) very nice, so please treat them well. They are just doing their job. They will need to make sure that all the screens you have are shared during the exam, that your webcam is working accordingly and that your phone is away from you while working on the exam. You can take breaks but you need to let them know when you want to go on a break and when you come back you also need to give them a heads up and when they say please proceed then and just then you go back to be working on the exam. I say proctors because you may have one proctor when you start the exam and during your 24 hours timeframe their shift may end and you will get another proctor. Talking to the proctor is via a chat and you won’t even see when one leaves and another one joins in. Get a good night sleep before the exam and make sure you have food and water prepared the day before and a lot of coffee, and I mean A LOT!

Oh by the way, do not hack the day before, rest!  You need to be mentally ready and rested when you start the exam. Think about it, you are attempting to hack into an AD set of 3 machines and 3 standalone machines in a matter of 24 hours. Do the math :) 

Four very important things that I would like to point out before wrapping up this long review.
1. Read the exam guide and understand it. Offsec will provide you with a link to it. They take it really seriously.
2. Take really good screenshots and make sure everything is on it as they ask you to do. It would be a shame loosing points because of a bad screenshot.
3. When you submit a flag in your exam dashboard it will not indicate if the flag is correct or not. Make sure that you copied the entire flag. I would copy it into my notes, make sure that it is correct and then submit it on the dashboard.
4. Take very good notes of the steps you use to exploit the machines and once you get up to 70 points stop if you can, and review all your evidence. If necessary go back and take new screenshots, just to be sure it is all there. This will take some time so don’t try to do this in the last 5 minutes of your exam because as soon as your time runs out it’s over.

## After the exam - report writing
At this point I hope you could get enough points to pass the exam. You still have one more task to do, write a professional report. Offsec offers a template for it and I suggest you use it, it will make your life easier. If I were you I would not write that report up right after the exam, I would just go through my notes one more time to make sure that everything is there. If I used a command that worked I would copy and paste that command from the exam into my notes, do not manually copy the commands into your notes. You will be under a lots of stress and you will be tired as hell. It is easy to make a mistake in that state. If the Offsec staff can not reproduce what you did during the exam they will likely disqualify that machine and will not give you points for it. You see the exam is not just about getting the flags, it is also about documenting everything the correct way. I’ve seen people who underestimated the importance of this and failed their exam. 

Once you reviewed everything go get some well deserved sleep. The next day put the report together and be careful that it will take some time. A considerable amount of time. Select your best screenshots, and describe every step you took to exploit the given machine, then read the email from Offsec on how to upload the report and go, get some more sleep :)

In my experience they evaluate the exam really fast so don’t worry, they will let your know your results the fastest they can.

## If you don’t pass the exam on your first try
Well, that s*cks for sure but at this point you will have two options. The first one (and I don’t recommend it) take a break and get back to it later. This is really hard because you’ve been grinding for the OSCP for many months now and if you let your feelings get you down and put it away for a month or two it will be much harder to pick it up again. A marathon, remember…? The second options is that you take a couple of days off from practicing, like a cool down period and then get back into the saddle and grind out another month or two in the PG Practice lab, review all your machines, notes, try to exploit them again without looking into your notes and try to pinpoint what went wrong. Some people are way more stressed when they go for their first attempt than when they try to pass for the second time. I will not write about my own experience because that is not the point of this write-up, you can find plenty of those blogs out there but I gotta tell you that when I first tried to pass it about 3 or four hours into my exam I felt like I hit a brick wall with the speed of a 100 miles per hour. Do not get discouraged, just put some more hours in and you will be fine. It really comes down to how much you want it! I’m sure if you are eager enough to earn your OSCP certification you will find the time, effort, courage to complete it.

## Aftermath
I passed my OSCP exam in February 2024 and I feel the benefit of going through all that pain, suffering and frustration. I refer back to my notes quite often and find those techniques I learned during the preparation phase very useful in my everyday work. To me it was not just a hacking certification but a personality test as well. I also wanted to say thank you for everybody who was supporting me during this insane incredible journey through hell… to heaven :) 

### ps:
Please don’t reach out to me for the solution of the lab or exam machines. Thank you!
