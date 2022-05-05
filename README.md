# crawling_listof_followers_instagram
The Cinderella Project (Stalking in instagram 101): Downloading list of followers of a page in instagram
Story:
In a normal busy day, after inserting a lot of coffein in my blood, beside of doing my works, I wanted to find Id of a person I recently met and surpisingly I couldnt find her anywhere beside telegram. So I wanted to find her page Id with some knowledge of her like name and family name, telegram id, age and her major.
After some random searchings, I couldn't find any clue and I was کله کیری شدن.
At this rage, I started to do a more specificed search and began to search on pages related to our major and university or any uni related pages.
After this **revolutionary** decision, Wanted to search on following of near connected peaple but there wasnet 
Step 1:
Login to your instagram account on a browser.
Go to desired page.
Select on followers to see the list of followers.
As you can see it doesnt have any search option and if you scroll down the list, you can see the new data will be fetched from the server and you must scroll down until you reach end of the list.
Now we want to simulate this behavior and automate this method.

Step 2:
Open Inspect Element on the browser.
Each record has two fields: title and subtitle.
title is equal to id.
subtitle is equal to the name given by the user.
In this step we must find two tags matching these two fields.
As I am writing this readme file, these two classes are like blow:
< Pic 1: from class name of tag one >
<comment: >
< Pic 2: from class name of tag two >
<comment: >

Step 3:
Run these two codes and see the output you can see the numbers of already loaded pages.
< Pic 3: from output of two codes >
after one **complete** scrolling:
< Pic 4: from output >


Step 4:
In this step we want to automate scrolling to load all the follower/following pages into our browser cache.

pop_up_list = 
pop_up_list.scrollIntoView({block: "end"});

pages = followers/7;
(async () => {
    for (i = 0; i <= pages; i++) {
        await c.scrollIntoView({ block: "end" });
        await new Promise(resolve => setTimeout(resolve, 1000));
        await c.scrollIntoView({ block: "end" });
        await new Promise(resolve => setTimeout(resolve, 7000));
    }
})();

IDs = 
Names = 

(async () => {
    for(i=0; i<=1052; i++){
        Id = await IDs[i].textContent;
        Name = await Names[i].textContent;
        await new Promise(resolve => setTimeout(resolve, 3000));
        string = string + 
                "\n" + 
                Id + 
                " - " + 
                Name;
    }
})();

