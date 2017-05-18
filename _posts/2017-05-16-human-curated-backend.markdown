---
layout: post
title:  "Human curated backend"
date:   2017-05-15 15:18:00
categories: Internet tech
author: Eonist
---

The underlying data structure must be easy to edit by humans. A possible way this could be achieved is to store "tree-data" with "many-to-many" links in multiple .json files that link each other.

<img width="800" alt="img" src="https://raw.githubusercontent.com/ducksource/img/master/human_laptop.jpg">

**Data-Structure diagram:**

```
👷 WIP Feedback welcome 🚧
A.json {title:Politics}[
    1 {title:Math, node:B.json}
    2 {title:Computers, node:Q.json}
    3 {title:Astronomy, node:X.json}
]
B.json {title:Math}[
    1 {title:Algebra, node:R.json}
    2 {title:Nature,node:C.json}
        1. {title:Nano, node:C.json}
        2. {title:Tech, node:J.json}
    3 {title:Cosmos, node:Q.json}
]
```

In the beginning the search engine will use the same .json hierarchy as its backend. In the future one could employ a Graph like database that syncs the .json hierarchy to it self. A graph database would be better for performance on the webpage. 

#### Future:

Structuring the entire data set in separate .json files is great for user editing.  Here is the folder hierarchy on github:

```
Health
	Medicine
	Meditation	
		Mindfulness
		Yoga
	Psychology
tech
	Digital currency
		Etherium
	AI
		ML
			Linear-regression
		Heuristics
		Big-data
Handcraft
	Pottery
	pet-grooming
```

Under each folder there will be an topic.json file containing the links to other nodes. See data structure diagram.


#### Q&A

**Q:** This will get overwhelming Fast too many .json files all over the place it will be impossible to manage. 😵    
**A:** Github has a trick: type the letter `T` and you can search within the repo. This doesn't work on mobile. so then you have to dig into the folders your self.   

**Q:** On mobile it will be hard to edit .json files too many 😵  
**A:** Use the learn-anything search engine. find your node and right click it. Click: Show in knowledge.map. This will take you directly to the .json file in the knowledge.map repo on github 🎉  

**Q:** Ive added my awesome resource to the topic.json file. How do I make my addition show in the learn-anything search engine?  
**A:** Wow, thanks for your contribution ❤️ It's a really simple 2 steps and the Change is sent for review here is the instruction: [How to PR](https://help.github.com/articles/about-pull-requests/) After this is complete. A person on our team will confirm that its in line with the knowledge.map curation ethos and then it will go live. Usually within minutes. As we are global and someone is usually awake. 

#### knowledge.map curation ethos: 

1. Add resources that are highly regarded among peers. 
2. Avoid adding content that is similar to content that already exists. 
3. It's ok to delete resources if you find a better one. 
4. Arrange resources based on their impact. 
5. Learning should accessible by all. Always add free learning resources. 
6. Prefer unbiased knowledge. If its disputed in the general consensus remove it. Wikipedia is a good resource to clarify dispute. 
7. New resource can have higher sort order than older but more regarded resource. Aka give the new guy a chance. This is up to the human to decide. 
8. Your track-record of adding good content will impact the decision of adding a resource or not. I.e if you only add 👎 content then it will negatively impact future pull requests. So curated your additions with ❤️ And argue your case why it should be added/removed. 
9. Power corrupts. Our Mods will rotate on a regular basis. Pass the torch around so to speak. 
10. knowledge.map is curated by you. Thank you 🌹

#### Fast-lane:

In the future. If a contributor becomes a member of the knowledge map team. This person can alter links on their own. Provided this person has a good track-record for making positive un-biased changes. This vetting process will be a combination of past github history on open-source project and all around "gut feeling". There will be limits to how many alterations one can make in a small period of time so to avoid rouge agents. A CI bot will take care of this imposed limit. 
