---
layout: post
title:  "A pragmatic solution"
date:   2017-05-17 15:18:00
categories: Internet tech
author: Eonist
---

The knowledge.map project needs to scale from 1 person curation to multi-person curation. In order to do this there needs to be a device that facilitates community curation. This device is github it self. Namely pull requests or PR for short. 

The data needs to be structured as simple as possible with out loosing detail. The most sensible format currently available is .json files. Simply explained this format is just a list where each item can in turn have other lists. 

Using this format is great. But we loose the meticulously crafted physical layout that Nikita has setup. 
To combine the beautiful layout and the pragmatic community data structure we need to compromise. 

<img width="800" alt="img" src="https://images.pexels.com/photos/7097/people-coffee-tea-meeting.jpg?w=1260&h=750&auto=compress&cs=tinysrgb">

#### This compromise consists of the following: 

First we scrape all the current mind maps and store them all in 1 folder. Each mindmap must unique file name which is the same as the title. We store the coordinates of each item in each mindmap like: `Philosophy {link:url,pt:{100,100}}` where pt is the relative coordinate and url is the permalink to the resource. 

#### The drawBack:
The drawback is that the community will only be able to add/remove/edit content but not the positioning of the item their adding. this still has to be done by Nikita or someone on the team. 

#### The future:
In the future we can deploy an algorithm that designs the mindmaps close to Nikitas current design. Some maps will then have a layout attribute like. layout:leaf which would have a more list like appearance like  [philosphy](https://my.mindnode.com/DaLRfu3ipMHEkhxuzqKTgbZPLmVGTmN7khBS3xqZ#-28.4,-144.3,2) . And layout:tree which would resemble  [devops](https://my.mindnode.com/4pT3AeEEywqSgdxTFBRgq3bmFpLs6s9YSaNMrxZY#150.3,-6.1,-1) 

The so called layout themes would be partly a custom spacing balancer positioning nodes downwards like a hierarchy. The algorithm would use geometrical math to calculate available space around it. sort of like a physics engine. This algorithm could be improved over time to reflect better design choices art directed by Nikita and the team. 

```
func distribute(tree:Tree, pt:Pt){/*recursive*/
	tree.children.map{
		/*align things here*/
		if !$0.children.isEmpty {distribute($0)}
	}
}
```

<img width="800" alt="img" src="https://images.pexels.com/photos/21661/pexels-photo.jpg?w=1260&h=750&auto=compress&cs=tinysrgb">

#### The present.
We wont design the spacing algorithm now. As we should focus on other things. The manual positioning is a middle ground for the time-resources we have available. 

<img width="800" alt="img" src="https://raw.githubusercontent.com/learn-anything/img/master/2017-05-19-150614_1153x895_scrot.png">

#### Easing the manual labour.
However if adding nodes to the mindmap website is to intensive we could export the json files to .svg that in turn could be edited in Illustrator or sketch. Svg would only by a tool to edit the layout. Svg can do all the things mindmap can do. And then export back to json with coordinates etc. 

#### Final note. 
There will be some interesting coding challenges ahead. Custom parsers, geometrical spacing algorithms, filtering search. optimizing for speed, managing an eco system of information. Because that is what this is. An eco system of freely available information. An together with the opensource community we think knowledge.map can really be something for everyone. 🌹	


