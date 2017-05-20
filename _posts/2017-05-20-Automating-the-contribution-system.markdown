---
layout: post
title:  "Automating the contribution system"
date:   2017-05-20 19:18:00
categories: Automation
author: Eonist
---

In order to scale we needed to add some automation. So we made an algorithm. The "Auto-spacer" And it isn't very intelligent at the moment. All it does is read hierarchical structured `.json` data from github and place each item in a waterfall like structure: 

<img width="800" alt="img" src="https://raw.githubusercontent.com/learn-anything/img/master/devops.png">

In the future we will iterate on the Auto-spacer algorithm and add nice little bells and whistles like horizontal/vertical balancers that intelligently makes room between groups of relates topics. Similar to Nikita meticulously designed mindmaps.

Adding automation to the project allows us to offer people an easy way to contribute their own resources and even new topics. None of us know much about the topic "Pet-grooming". But someone else might and this person can now add their favorite learning resources. Secret gems they as domain experts would only know about. To contribute some Book links all you have to do is insert some new fields in the document bellow: 

```
{
	"title":"pet grooming",
	"contributors":["Nikita","Angelo","PGG✌️"],
	"meta":["Pets","animals","nature"],
	"nodes":[
		{
			"title":"Tools",
			"nodes":[
				{"title":"clippers","url":"animals/clippers.json"},
				{"title":"Blades"},
				{"title":"Brushes"}
			]
		},
		{
			"title":"Workflows",
			"nodes":[
				{"title":"bathing"},
				{"title":"fur"},
				{"title":"claw"}
			]
		},
		{
			"title":"Tips",
			"nodes":[
				{"title":"Blogs"},
				{"title":"Books"}
			]
		}
	]
}
```

Now after the pet-groomer-domain-expert has inserted his ❤️ curated links all he has to do is [PR](https://help.github.com/articles/about-pull-requests/) it into the main repository knowledge.map and 💥 the topic is now added to the learn-anything search engine. If he made a mistake all he has to do is PR it again and correct his mistake. And if other people want to add their hand picked links to the pet grooming set. They do the same. [PR](https://help.github.com/articles/about-pull-requests/) and the world knows more about pet grooming. Here is an example of the auto created mind map after the last PR change:

<img width="800" alt="img" src="https://raw.githubusercontent.com/learn-anything/img/master/petgrooming.png">

## So how does it work?
`.json` files are stored in the knowledge.map github repository and the learn-anything.xyz website pulls these in and renders them.

#### Linking mind maps:
In each node there is a `url` attribute where you can insert a link to another mind map. The links looks like this:

```
/animals/mamals/cats/cat-grooming.json /*absolute url*/
./dog-grooming.json /*relative url*/
```

#### The present
So we will have a hybrid system of around 300 meticulously designed mindmaps that Nikita has designed and gathered resources for and the Pull-Request system where you as an individual can contribute directly to broaden the learn-anything.xyz eco system. 

#### The future:
In the future we will store json's on github/mymindnode server, and then parse these into a "graph db" on pr triggered events/interval events. and then the learn anything renderer pulls data from the graph db.
