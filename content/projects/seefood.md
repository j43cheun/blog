---
title: "SeeFood"
description: "A very simple iOS app for identifying food."
date: "2020-12-26T03:09:48-08:00"
slug: "seefood"
github: "https://github.com/j43cheun/SeeFood.git"
tags: [ "iOS", "Swift", "SwiftUI", "Core ML", "Vision" ]
---

SeeFood is a very simple iOS app that I wrote for identifying food. Given an
image, SeeFood will try to determine whether the subject is a **hot dog** or
**not a hot dog**. SeeFood is a fork of
[Garbage Vision](/projects/garbage-vision) with the Garbage Net Core ML model
replaced with the Hot Dog Net Core ML model. Classification is handled
exceedingly well by the Hot Dog Net Core ML model, which I created using
Apple's Create ML app and trained using the
[Hot Dog - Not Hot Dog](https://www.kaggle.com/dansbecker/hot-dog-not-hot-dog)
dataset from Kaggle by DanB. In practice, I've noticed that classification has
been mostly accurate, with the only minor quirk being an issue in
differentiating between hot dog and hamburger, which imo are basically the
same 🤣.

SeeFood takes inspiration from Jian-Yang's "SeeFood" app in HBO's Silicon
Valley TV series, which can only classify foods as **hot dog** or
**not hot dog**. I wrote this app as a joke after showing Garbage Vision to my
friends a day earlier.

<div class="columns mt-5">
  <div class="column">
    <img src="/projects/seefood/img/main-screen.PNG">
  </div>
  <div class="column">
    <img src="/projects/seefood/img/hot-dog-classification.PNG">
  </div>
  <div class="column">
    <img src="/projects/seefood/img/hot-dog-confidence-scores.PNG">
  </div>
  <div class="column">
    <img src="/projects/seefood/img/not-a-hot-dog-classification.PNG">
  </div>
  <div class="column">
    <img src="/projects/seefood/img/not-a-hot-dog-confidence-scores.PNG">
  </div>
</div>