---
title: "[Leetcode] Solving Fruit Into Baskets"
date: 2023-07-16 22:52
tags:
  - leetcode
social_image: /media/904-example_1.png
description: Let's solve Fruit Into Baskets
---
T﻿he problem given:\
\
<!--StartFragment-->

You are visiting a farm that has a single row of fruit trees arranged from left to right. The trees are represented by an integer array `fruits` where `fruits[i]` is the **type** of fruit the `ith` tree produces.

You want to collect as much fruit as possible. However, the owner has some strict rules that you must follow:

* You only have **two** baskets, and each basket can only hold a **single type** of fruit. There is no limit on the amount of fruit each basket can hold.
* Starting from any tree of your choice, you must pick **exactly one fruit** from **every** tree (including the start tree) while moving to the right. The picked fruits must fit in one of your baskets.
* Once you reach a tree with fruit that cannot fit in your baskets, you must stop.

Given the integer array `fruits`, return *the **maximum** number of fruits you can pick*.

<!--EndFragment-->

we're given only 2 baskets, and each basket can contain only 1 type of fruit, and fruits are marked as numbers, not with names. now we have to calculate the maximum numbers that we can collect, this line is important 

* Once you reach a tree with fruit that cannot fit in your baskets, you must stop.

s﻿o if the window contains more than 2 types of fruits, we must stop collecting them. 

t﻿he first solution is being brute force on the array

e﻿xample for this \[1,2,3,2,2,1,4]

**Solution 1: Brute Force**

<!--StartFragment-->

![How to Solve Two Sum in JavaScript | by Jordan Moore | Level Up Coding](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRf4djrvce5wI-XJ3djJHEsDO9crNXqUknzDw&usqp=CAU)

<!--EndFragment-->

w﻿e can set the starting index from 0, then sliding through each next indices to scan put each suitable 1 into the baskets, let's break it down with the solution above

1. s﻿tarting index is fruits\[0], which is fruit with number 1, then we move to the next index is number 2, these 2 have filled the 2 baskets already
2. M﻿ove to the next tree is fruit number 3, the fruit number 3 cannot fit into those 2 baskets cause now we only accept type 1 and 2, so the maximum of fruits we can collect in this window is 2.