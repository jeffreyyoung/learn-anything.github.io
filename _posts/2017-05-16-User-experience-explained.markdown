---
layout: post
title:  "Interactive node map"
date:   2017-05-15 15:18:00
categories: Internet tech
author: Eonist
---

A walkthrough of how the interactive node map will work:

<img width="800" alt="img" src="https://d2lm6fxwu08ot6.cloudfront.net/img-thumbs/960w/YHIGXSND12.jpg">

#### Use case:
```
1. User types: Mindfulness -> Render mindfulness with subnodes in a circle around it. 6 subnodes 

2. User clicks [Up level button] -> Render Meditation with subnodes in a around it. 4 subnodes (mindfulness,yoga etc)

3. User searches for tensor flow -> render tensor flow with subnodes around it 16 leaf nodes (URL links)

4. User clicks [Up level button] x 4 times. Tensor flow -> ML -> Data science -> Big picture.  -> render full picture

5. User Is now in Big picture with 20 nodes around BigPicture in the middle. 

6. User clicks Crafts node -> arts -> fine art -> Pottery -> Pottery tutorial link. -> pottery URL opens in new tab

7. User Learns pottery and becomes happy. ❤️
```

#### Rationale:

For mobile we will do One 🌻 per level. On smaller screens you can only have so many nodes before you run out of space. This also eases the comprehension for the user. It's easier to reason about hierarchical structures. Diving in and out of branches is also fun. Brings out the Explorer in you. Since there there is more screen space on desktop computers we will render many 🌻🌻🌻🌻 on the same page. In short: Desktop has 2 levels per dive. Mobile has 1 level per dive. So you'll travel faster down the hierarchy on the desktop than on mobile. For MVP v1 we will design for desktop so Mobile will have to scroll around the "field" of sunflowers. But this will be mitigated in the near future.

<img width="800" alt="img" src="https://static.pexels.com/photos/297642/pexels-photo-297642.jpeg">

#### Something for the keyboardist

Another workflow is just using the keyboard. You type "tensor flow" and see that its parent is ML. You then start typing Machi... and the search engine auto suggest machine learning. You click enter and the node map transitions up an level. This also works diving into branches you see linear regression under ML and you just start typing linea.... and hit enter and it dives into the linear regression node. 
