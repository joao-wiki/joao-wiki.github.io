---
layout: post
title:  "Taxonomy of Recommenders"
date:   2016-01-07
categories: mooc rec-sys open
---
tags: @reference @mooc @rec-sys

Sources:

* [Taxonomy 1](https://www.coursera.org/learn/recommender-systems/lecture/Bc5F3/taxonomy-of-recommender-systems)
* [Taxonomy 2](https://www.coursera.org/learn/recommender-systems/lecture/jUyr2/taxonomy-of-recommender-systems-continued)

## 1.Domain

What's being recommended (products, bundles, people, music playlists, etc.)? A particularly interesting property is the way in which we treat items that have already been experienced. Some focus on new items, others on re-recommend old ones.

## 2.Purpose

In many cases, the recommendation is an end in itself (buy, listen, watch). In other times can be education, or building a community. An example of an educational recommender would be one that teaches more efficient programming commands or better ways of use a given software.

## 3.Context

What is the user doing at the time of the recommendation and how does that constraint the recommender? If you are listening to music, you may not want to be annoyed by pop-ups and interruptions. 

## 4.Whose opinions

Whose opinion is the recommender based on? Experts? Ordinary folk? Similar people (relative neighbours)?

## 5.Personalisation level

At the most basic level the recommender may be generic, or **non-personalised**, and everyone receives the same recommendations.

From there, you have many ways to get to personalisation. We can attach a recommendation to a **demographic**; the recommendation can be **ephemeral** and be attached to the user's current activity; and a persistent recommended will try to match long-term interest and preferences.

## 6.Privacy and trustworthiness

Who knows what about me, for me to use this recommender? How much personal information do I have to give it? Does it have to know who I am? Can I use anonymously? There is a way I can deny any of those preferences?

Also answers to the question: is the recommendation honest? What are the biases and business rules and do they fell legit to the user (Fandango!)? Is the recommender vulnerable to external manipulation (hacks)? Is it transparent? Does it have a good rep? 

## 7.Interfaces

Different styles of output and interfaces. Is it presenting as an agent, as a dialog, or is it acting more like a search engine or a tool? Does it make predictions, recommendations, filtering, etc., and is it more organic or more explicit?

How does it gather input? Explicitly? Implicit user actions?

## 8.Algorithms

Basic model of how a recommender works, three fundamental components:

* Users: people who have preferences for items, may be a source of data as well
* Items: things that we are choosing to recommend
* Ratings: a way of expressing opinions in our systems, or where users meets items.

Users and items form a community, a space where all this opinions make sense.

### Non-personalised summary statistics

These involve summary statistics and in some cases product associations. They use external data (best-seller, most popular, trending hot, etc.) or a summary of community ratings to perform general recommendations to users.

The simplest example of summary stats is the averaging user submitting rankings to display a number of stars or quality score (TripAdvisor, Booking.com, etc.).

### Content-based filtering

Users rate items, and from that we build a model of user preferences against the item attributes. When we rate movies, a recommender will eventually figure out what genres (or any other of the items' features) we like best, by comparing our ratings with the characteristics of the item.

An alternative, are knowledge-based systems. These systems use the item attributes to form a model where the user navigates interactively, and that doesn't depend on what other people have to say because they are explicitly taught the properties the user cares about and likes (news feed, music libraries are examples).

### Collaborative filtering

Uses the opinion of other people, instead of attribute data.

In user-user collaborative filtering you select a neighbourhood of people with similar taste and use their options. A variant of this is trust-based recommendations.

In item-item recommendation you pre-impute similarity among items via ratings, and use own ratings to triangulate for recommendations.

Dimensionality reduction is a technique that compress the matrix as a proxy for taste.

### Others

Examples are interactive recommenders (critique-based, dialog-bases), that ask questions, or collect input interactively, and hybrid recommenders.

## Plus: Evaluation

In order to decide which to use, we will need a way to evaluate them. There are different types of evaluation, from accuracy f predictions, usefulness of recommendations, are the recommendations obvious, computational performance, among others.