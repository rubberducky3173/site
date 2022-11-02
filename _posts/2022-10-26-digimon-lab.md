


**Hello and welcome to Lab 1... the Digimon CSV lab.**

Here you’ll find my answers for the questions that the lab asked:
What is the average speed of all Digimon?
Write a function that can count the number of Digimon with a specific attribute. (“Type and “Vaccine” should return 70.)
The Digimon on your team are restricted by the total amount of Memory that they need. If your team only has 15 Memory, name a team of up to 3 Digimon that has at least 300 attack (Atk) in total.

**What is the average speed of all Digimon?**
Answer: 120.40160642570281 (or 120.4)

After doing the simple setup for reading a CSV file, I used sum() and len() to get the average. It was pretty simple, given that everything was in numbers already. 

![Speed](https://github.com/rubberducky3173/site/blob/master/assets/img/speed.JPG?raw=true)


**Write a function that can count the number of Digimon with a specific attribute.**
Answer:
![Counter](https://github.com/rubberducky3173/site/blob/master/assets/img/counter.JPG?raw=true)

At first I really had overcomplicated this for myself because I made my counter a list rather than an integer. (Don’t ask why I was thinking that way) But using the == operator in the loop for the reader, the counter was able to simply add 1 every time it found a matching attribute in the column.

If I change the inputs to Type and Vaccine, I do indeed get 70!
![Vaccine1](https://github.com/rubberducky3173/site/blob/master/assets/img/vaccine.JPG?raw=true)
![Vaccine2](https://github.com/rubberducky3173/site/blob/master/assets/img/vaccine2.JPG?raw=true)


**The Digimon on your team are restricted by the total amount of Memory that they need. If your team only has 15 Memory, name a team of up to 3 Digimon that has at least 300 attack (Atk) in total.**
Answer: Kuramon, Pabumon, Ogremon: Memory: 12 Atk: 310 (Just using the parameters of 15 and 300)

This question was extremely painful to answer because of the amount of checking needed.

First I checked the memory and attack of every Digimon. If the memory is less than the max specified memory AND the attack is greater than the specified attack (because we want to minimize memory and maximize attack) then we return and append the data.

![Team1](https://github.com/rubberducky3173/site/blob/master/assets/img/team1.JPG?raw=true)

Here’s a pile of if statements that goes through our already processed data, the stats list. For making a team of 3 (x, y, z) we have to check if a group of 3 found matches up with the input requirements. Also, because data points are unique, we have to use the =! operator to make sure this group doesn’t have duplicates.

![Team243](https://github.com/rubberducky3173/site/blob/master/assets/img/team243.JPG?raw=true)

If we have a match, print the team of 3 (names, memory, and attack)

In my case, when I used parameters of memory 15 and attack 300, I got  Kuramon, Pabumon, Ogremon with memory 12 and attack: 310.

Overall I did have some struggles where I overcomplicated code as well as trial and error for finding syntax that worked, troubleshooting, and looking for online resources. (The sources are credited and explained in my submitted Python file.) After some brainstorming I do eventually come up with what I think is the right idea, but implementing it in code is a bit harder and I find myself often looking for some extra help. The last question was quite hard and I spent the longest on it, given that sometimes even changing small things like brackets, parentheses, and single numbers can throw your entire program off. I had to check and check again and just guess sometimes to fix something. I think it’s a matter of practicing over and over again to be able to recognize the issues! I didn’t work with anyone else in this lab other than consulting the internet. (Thanks w3schools especially for refreshing my syntax!) I found myself looking at past exercises a lot too for syntax and code I had completely forgotten (penguins.csv and favoritecolors.csv). I’m wondering if there is a sleeker way to write my code for the team builder question because I had if-statements upon if-statements that turned out to be a little messy. 


But this lab was pretty awesome too. I continued to learn how to interpret data from a CSV file and seeing the code eventually work is like a breath of fresh air and made Python-noob (to an extent) pain worth it. It was quite the relief for the team builder function. I’m wondering if it would ever be possible to include images/sprites of the Digimon in some larger program to add some nice visuals.

Lastly, since Digimon is one of my childhood favorites, getting to see them again in schoolwork is a small but very enjoyable treat for me. 
(If you’re curious, my favorite Digimon is Omnimon. I know that Omnimon is absolutely overpowered but come on. That design is peak)
(This is my favorite Digimon song too: https://youtu.be/bjO_MIVLQcE)

![Omnimon](https://github.com/rubberducky3173/site/blob/master/assets/img/omnimon.png?raw=true)


Thanks for reading!
