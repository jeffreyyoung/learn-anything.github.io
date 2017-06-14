---
layout: post
title: "Mind Maps Design Guideline"
date: 2017-06-15 15:18:00
author: Team
---

The reason this guideline exists is because we want to make sure the mind maps are both of the highest quality in terms of resources but also so that they are not too overwhelming visually. All mind maps should feel familiar so that finding the resource you need is as effortless as possible.

Each mind map represents the most efficient path for learning a topic. Each topic that can be learned is a separate mind map and is located in a correct place in the knowledge graph as a child to some other topic. For example linear algebra is inside Mathematics because it is in direct relation to Mathematics.

All mind maps follow a very similar style. There is a main node at top which most often leads to a wiki article abut the topic. From this main node, there may be attached a ‘reddit subreddit’ or ’stack exchange community’ of this topic if such exists. If the main node is a project like React.js, a ’github link’ is attached to it.

Nearly all mind maps have a basics node which represents the most efficient step by step path for learning this topic. The resources are prefixed with a number like ‘1. ‘ which stands for the order in which the resources should ideally be taken in. If resources are of the same value (no direct prerequisite knowledge), they can be marked to have the same number.

Aside from the main node and basics node. There is very often a ‘help’ node which has links and resources that help with learning the topic. These resources may be documentation or a GitHub awesome list or a forum. Both help node and basics node are attached to the main node with the topic. A help node can be further split into ‘articles’, ‘talks’, ‘images’ or ‘tools’. All of them are attached to ‘help’ one after another. An example of this can be seen [here](https://learn-anything.xyz/web_development/javascript_libraries/react).

Together this makes a complete mind map. After this new topics can be created and they will go under ‘basics’ node. So for example in [linear algebra](https://learn-anything.xyz/mathematics/linear_algebra), after basics node, we can see ‘matrix factorisation’ diverge from it, where matrix factorisation is a mind map of its own. In some complex cases there is more freedom in how you can layout this branching out like for example here for learning [swift language](https://learn-anything.xyz/programming/programming_languages/swift). But the idea stays the same. You learn the topic with ‘basics’ and ’help’ nodes and then you can branch out into new topics. If the topic is large enough, it is created as a new mind map, if not, then a link is provided to either a wiki or a project link if it is a project.

Some mind maps can be more creative like [DevOps](https://learn-anything.xyz/programming/software_development/devops) but the idea is still very similar. There is a mind node and then it branches out to new topics where everything is connected in a meaningful way.

Knowing this, you can improve both the structure and content of these mind maps. Content wise, we have a set of rules we like to follow before adding the resource or link.

For basics node, the resource being added has to ideally be the best one for learning the topic as well, preferably being free. There is no limit to what can be added, the only requirement is that the content is really good and ideally is free.

For help node, the same applies but there is more freedom to what can be added. Same for articles and talks. The material has to be good and relevant to the topic, otherwise it won’t be added.

Knowing all of this. If you want to help improve these mind maps, you can do it by either changing the structure of the mind maps from our live editor or you can directly change and add new content to the JSON that lives on the [GitHub page](https://github.com/nikitavoloboev/learn-anything).