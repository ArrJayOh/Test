<div align="center"><h1>X CLONE</h1></div>
<div align="center"><p>Requirements Specification<p></div>
<div align="center"><p>COS 301 Mini Project - Group MP9<p></div>



## Table of Contents

- [1\. Introduction](#1-introduction)

  - [1.1 Purpose of this Document](#11-purpose-of-this-document)

  - [1.2 Product Scope](#12-product-scope)

    - [1.2.1 What the System Will Implement](#121-what-the-system-will-implement)

    - [1.2.2 What the System Will Not Implement](#122-what-the-system-will-not-implement)

    - [1.2.3 Objectives](#123-objectives)

  - [1.3 SRS Overview](#13-srs-overview)

- [2\. General Description of Product](#2-general-description-of-product)

  - [2.1 Product Functions](#21-product-functions)

  - [2.2 User Characteristics](#22-user-characteristics)

  - [2.3 Constraints](#23-constraints)

- [3\. Specific Requirements](#3-specific-requirements)

  - [3.1 Functional Requirements](#31-functional-requirements)

    - [3.1.1 General Users](#311-general-users)

    - [3.1.2 Premium Users](#312-premium-users)

    - [3.1.3 Administrative Users](#313-administrative-users)

  - [3.2 Other Requirements](#32-other-requirements)

- [4\. Appendix](#4-appendix)

  - [4.1 Acronyms, Abbreviations, and Definitions](#41-acronyms-abbreviations-and-definitions)

  - [4.2 References](#42-references)

<br>

# 1\. Introduction

## 1.1 Purpose of this Document

This software requirement specification acts as a detailed overview of the functionalities, features, requirements, and constraints of the project. Its purpose is to provide a communication medium between the development team and the project owner.

## 1.2 Product Scope

The product, _X Clone_, is designed to be a simplified replica of the social media platform X (previously known as Twitter). The system will replicate a selection of functionalities and features of the reference platform, as detailed below.

### 1.2.1 What the System Will Implement

- The system allows for user account registration and authentication through the use of usernames, passwords, and verification codes.
- Account authorization is implemented with different user roles.
- The system includes account and settings management, whereby users can adjust their profile information and visibility, deactivate, or delete their profile, and adjust application settings.
- Content posting and social interaction are included in the form of tweets, retweets, comments, followers, and collaborative posts.

### 1.2.2 What the System Will Not Implement

- The system does not provide an implementation of direct messaging, whereby users can have private, one-on-one or group conversations which are separate from the main tweeting platform.
- The system will not implement X’s communities feature, which are exclusive groups where only specific users who are invited to the community may converse.
- The system will not implement an algorithm to determine what content should be displayed on a user’s timeline and will instead display posts in reverse chronological order.
- The system will not implement a bookmarks feature, whereby users can save tweets for later viewing.

### 1.2.3 Objectives

The primary goal of this project is to create a simple, deployed clone of the social network X.

The objectives of _X Clone_ are as follows:

- Facilitate online public discourse in a concise and interactive manner.
- Facilitate networking and collaboration between individuals with similar interests or professions.
- Facilitate information sharing and public visibility, particularly for businesses or organizations wanting to share news, updates, and other content with their audience.

## 1.3 SRS Overview

This document is laid out according to the IEEE SRS 830-1998 standard with structural alterations made with considerations to the project at hand.

The following information is in this document:

- Section 2: General description of product, providing a background for its specific requirements.
- Section 3: Specific requirements of the product with functional requirements organized by user class.
- Section 4: Appendix, including a glossary and references.

<br>

# 2\. General Description of Product

This section provides a background and context for the project by describing the factors that affect X Clone and its specific requirements, which are detailed in Section 3 of this document.

## 2.1 Product Functions

The main function of X Clone is to provide a platform on which users can interact and share content with one another. Users of the product will be able to register with and create accounts on the platform. They can then use their account to interact with the platform through tweeting, retweeting, liking, following, and commenting. The product essentially provides an online environment in which its users can communicate and share content with one another through a variety of features.

## 2.2 User Characteristics

This subsection of the SRS should describe those general characteristics of the intended users of the product including educational level, experience, and technical expertise. It should not be used to state specific requirements, but rather should provide the reasons why certain specific requirements are later specified in Section 3 of the SRS.

**1\. General Users:**
These users form the vast majority of the user base. They generally don’t have a large amount of technical expertise but are likely to have some form of familiarity with online social media platforms. A general user would interact with the X Clone platform by creating an account, editing their profile, and utilizing the various forms of engagement with other users provided by the product.

**2\. Premium Users:**
Premium users form a subsection of general users. These users would generally interact with the platform in the same manner as general users, but have access to certain “perks”, like an increased character limit for their tweets, which are only available to them. Premium users also have a specific icon which appears next to their username, which indicates their premium status. On the reference platform, general users can attain a premium status by purchasing it, but we will manually select premium users in our implementation.

**3\. Administrative Users:** 
These users interact with the administrative system and moderate the platform.

## 2.3 Constraints

There are a number of constraints by which the X Clone system must abide. The project’s constraints, as detailed below, have been set by both the project owner, and by the development team.

1. X Clone must be implemented using Supabase.
2. X Clone and its contents need to be appropriate for a professional environment.
3. The frontend frameworks that may be used in the development of X Clone are limited to Angular, React, Vue, Svelte, or Flutter.
4. The backend frameworks that may be used in the development of X Clone are limited to Vanilla JavaScript/Typescript/Python using the Supabase libraries with the option of additionally using NestJS/Express/Fastify/Python FAST API.
5. The structure of X Clone must adhere to a client-server architecture.
6. X Clone’s design must be kept minimalistic and must exactly replicate that of the reference platform X.
7. The development of X Clone must make use of an existing component library.
8. X Clone’s deployment must take place through a CI/CD process.

<br>

# 3\. Specific Requirements

## 3.1 Functional Requirements

The following functional requirements are organized by user class.

### 3.1.1 General Users

The _X Clone_ system shall:

- R1 Provide a secure user registration and authentication process to users.
  - R1.1 Allow users to create an account.
    - R1.1.1 Require users to provide a unique username, password, and email address.
  - R1.2 Require users to verify their email address before they have full access to their account.
    - R1.2.1 Send a verification code to the email address provided by the user.
    - R1.2.2 Require the user to input this code.
    - R1.2.3 Verify that the user’s input matches with the emailed code.
    - R1.2.4 Subsequently, give the user full access to their created account.
<br><br>
- R2 Allow users to create and post content.
  - R2.1 Allow users to compose tweets with text that is limited to 280 characters.
  - R2.2 Allow users to attach images and videos to their tweets.
  - R2.3 Allow users to post their tweets to the platform.
  - R2.4 Allow users to edit or delete their own posted tweets.
<br><br>
- R3 Allow users to view posted content.
  - R3.1 Provide a homepage which displays posts in reverse chronological order.
    - R3.1.1 Provide a “Following” timeline which exclusively displays posts from accounts that the user follows.
    - R3.1.2 Provide a “For you” timeline which displays recent tweets from all users on the platform.
    - R3.1 4 Enable a user to refresh their current timeline in order to display new tweets that have been posted from when the timeline was last loaded.
<br><br>
- R4 Allow users to interact with content.
  - R4.1 Allow users to like tweets.
  - R4.2 Allow users to retweet tweets.
    - R4.2.1 Post the retweeted tweet to the user’s own profile and followers’ timelines.
  - R4.3 Allow users to comment on tweets and can delete or edit their own comments.
    - R4.3.1 Allow users to edit or delete their own comments.
  - R4.4 Track and display the timestamp, likes, comments, and retweets on each tweet.
<br><br>
- R5 Allow users to view their own and other’s profiles.
  - R5.1 Display a user’s tweets, retweets, followers, and following list on their profile.
<br><br>
- R6 Allow users to manage their profiles.
  - R6.1 Allow users to edit their profile picture, bio, display name, email address, and password.
  - R6.2 Allow users to manage the visibility of their profile.
    - R6.2.1 Allow users to set their profile to public or private.
    - R6.2.2 Adjust the profile’s visibility based on the user’s selection.
  - R6.3 Allow users to deactivate or delete their accounts.
    - R6.3.1 Provide users with the option deactivate or delete an account.
    - R6.3.2 Confirm the user’s choice by requiring them to input their password.
    - R6.3.3 Remove relevant data or adjust account visibility based on the user’s choice.
<br><br>
- R7 Allow users to edit their application settings.
  - R7.1 Include a settings page where users can edit visual and accessibility preferences.
  - R7.2 Implement users’ preferences to their application.
<br><br>
- R8 Allow users to receive and view notifications.
  - R8.1 Provide notification services to users for likes, comments, and new followers on their profile.
  - R8.2 Include a notifications page where users can view all their notifications.
  - R8.3 Implement toast notifications to display system notifications.
<br><br>
- R9 Allow users to search for specific content and accounts.
  - R9.1 Include a search page with a search bar and filters.
  - R9.2 Display users and posts which match the search criteria.
<br><br>
- R10 Provide a help page with contact information for where users can request assistance.

### 3.1.2 Premium Users

Requirements **R1** and **R3** - **R10** are applicable to premium users. Additional requirements for this group are listed below.

The _X Clone_ system shall:

- R11 Allow users to create and post content.
  - R11.1 Allow users to compose tweets with text that is limited to 1000 characters.
  - R11.2 Allow users to attach images and videos to their tweets.
  - R11.3 Allow users to post their tweets to the platform.
  - R11.4 Allow users to edit or delete their own posted tweets.
  - R11.5 Allow users to create collaborative posts.
    - R11.5.1 Allow users to create a tweet and invite other users to collaborate on the tweet before it is posted.
    - R11.5.2 Send the invite to the other users and allow them to accept or reject the request.
    - R11.5.3 Post the tweet to the profiles and follower timelines of the collaborators who accepted the request.

### 3.1.3 Administrative Users

Requirements for admin.

## 3.2 Other Requirements

<br>

# 4\. Appendix

## 4.1 Acronyms, Abbreviations, and Definitions

- Tweet – A user’s post on X and X Clone’s platforms.
- Retweet – The act of reposting a tweet from a different user.
- Bio – A short description of a user which can be viewed on their profile.

## 4.2 References

Reference Platform: <https://twitter.com/>

Model for layout of this document: IEEE Std 830-1998(R2009)
