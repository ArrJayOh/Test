<p style="font-size: 3em; text-align: center; font-weight: bold;">X CLONE</p>
<p style="font-size: 2em; text-align: center;">Requirements Specification</p>
<p style="font-size: 1em; text-align: center;">COS 301 Mini Project - Group MP9</p>


## Table of Contents

[1\. Introduction](#_Toc162881810)

[______1.1 Purpose of this Document](#1.1-Purpose-of-this-Document)

[______1.2 Product Scope](#_Toc162881812)

[____________1.2.1 What the System Will Implement](#_Toc162881813)

[____________1.2.2 What the System Will Not Implement](#_Toc162881814)

[____________1.2.3 Objectives](#_Toc162881815)

[______1.3 SRS Overview](#_Toc162881816)

[2\. General Description of Product](#_Toc162881817)

[______2.1 Product Functions](#_Toc162881818)

[______2.2 User Characteristics](#_Toc162881819)

[______2.3 Constraints](#_Toc162881820)

[3\. Specific Requirements](#_Toc162881821)

[______3.1 Functional Requirements](#_Toc162881822)

[____________3.1.1 General Users 3](#_Toc162881823)

[____________3.1.2 Premium Users](#_Toc162881824)

[____________3.1.3 Administrative Users](#_Toc162881825)

[______3.2 Other Requirements](#_Toc162881826)

[4\. Appendix](#_Toc162881827)

[______4.1 Acronyms, Abbreviations, and Definitions](#_Toc162881828)

[______4.2 References](#_Toc162881829)

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

# 2\. General Description of Product

This section provides a background and context for the project by describing the factors that affect X Clone and its specific requirements, which are detailed in Section 3 of this document.

## 2.1 Product Functions

The main function of X Clone is to provide a platform on which users can interact and share content with one another. Users of the product will be able to register with and create accounts on the platform. They can then use their account to interact with the platform through tweeting, retweeting, liking, following, and commenting. The product essentially provides an online environment in which its users can communicate and share content with one another through a variety of features.

## 2.2 User Characteristics

This subsection of the SRS should describe those general characteristics of the intended users of the product including educational level, experience, and technical expertise. It should not be used to state specific requirements, but rather should provide the reasons why certain specific requirements are later specified in Section 3 of the SRS.

**1\. General Users**

These users form the vast majority of the user base. They generally don’t have a large amount of technical expertise but are likely to have some form of familiarity with online social media platforms. A general user would interact with the X Clone platform by creating an account, editing their profile, and utilizing the various forms of engagement with other users provided by the product.

**2\. Premium Users**

Premium users form a subsection of general users. These users would generally interact with the platform in the same manner as general users, but have access to certain “perks”, like an increased character limit for their tweets, which are only available to them. Premium users also have a specific icon which appears next to their username, which indicates their premium status. On the reference platform, general users can attain a premium status by purchasing it, but we will manually select premium users in our implementation.

**3\. Administrative Users**

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

# 3\. Specific Requirements

## 3.1 Functional Requirements

The following functional requirements are organized by user class.

### 3.1.1 General Users

The _X Clone_ system shall:

1. Provide a secure user registration and authentication process to users.
    1. Allow users to create an account.
        1. Require users to provide a unique username, password, and email address.
    2. Require users to verify their email address before they have full access to their account.
        1. Send a verification code to the email address provided by the user.
        2. Require the user to input this code.
        3. Verify that the user’s input matches with the emailed code.
        4. Subsequently, give the user full access to their created account.
2. Allow users to create and post content.
    1. Allow users to compose tweets with text that is limited to 280 characters.
    2. Allow users to attach images and videos to their tweets.
    3. Allow users to post their tweets to the platform.
    4. Allow users to edit or delete their own posted tweets.
3. Allow users to view posted content.
    1. Provide a homepage which displays posts in reverse chronological order.
        1. Provide a “Following” timeline which exclusively displays posts from accounts that the user follows.
        2. Provide a “For you” timeline which displays recent tweets from all users on the platform.
        3. Enable a user to refresh their current timeline in order to display new tweets that have been posted from when the timeline was last loaded.
4. Allow users to interact with content.
    1. Allow users to like tweets.
    2. Allow users to retweet tweets.
        1. Post the retweeted tweet to the user’s own profile and followers’ timelines.
    3. Allow users to comment on tweets and can delete or edit their own comments.
        1. Allow users to edit or delete their own comments.
    4. Track and display the timestamp, likes, comments, and retweets on each tweet.
5. Allow users to view their own and other’s profiles.
    1. Display a user’s tweets, retweets, followers, and following list on their profile.
6. Allow users to manage their profiles.
    1. Allow users to edit their profile picture, bio, display name, email address, and password.
    2. Allow users to manage the visibility of their profile.
        1. Allow users to set their profile to public or private.
        2. Adjust the profile’s visibility based on the user’s selection.
    3. Allow users to deactivate or delete their accounts.
        1. Provide users with the option deactivate or delete an account.
        2. Confirm the user’s choice by requiring them to input their password.
        3. Remove relevant data or adjust account visibility based on the user’s choice.
7. Allow users to edit their application settings.
    1. Include a settings page where users can edit visual and accessibility preferences.
    2. Implement users’ preferences to their application.
8. Allow users to receive and view notifications.
    1. Provide notification services to users for likes, comments, and new followers on their profile.
    2. Include a notifications page where users can view all their notifications.
    3. Implement toast notifications to display system notifications.
9. Allow users to search for specific content and accounts.
    1. Include a search page with a search bar and filters.
    2. Display users and posts which match the search criteria.
10. Provide a help page with contact information for where users can request assistance.

### 3.1.2 Premium Users

Requirements **R1** and **R3** - **R10** are applicable to premium users. Additions for this group are listed below.

The _X Clone_ system shall:

1. Allow users to create and post content.
    1. Allow users to compose tweets with text that is limited to 1000 characters.
    2. Allow users to attach images and videos to their tweets.
    3. Allow users to post their tweets to the platform.
    4. Allow users to edit or delete their own posted tweets.
    5. Allow users to create collaborative posts.
        1. Allow users to create a tweet and invite other users to collaborate on the tweet before it is posted.
        2. Send the invite to the other users and allow them to accept or reject the request.
        3. Post the tweet to the profiles and follower timelines of the collaborators who accepted the request.

### 3.1.3 Administrative Users

Requirements for admin.

## 3.2 Other Requirements

# 4\. Appendix

## 4.1 Acronyms, Abbreviations, and Definitions

- Tweet – A user’s post on X and X Clone’s platforms.
- Retweet – The act of reposting a tweet from a different user.
- Bio – A short description of a user which can be viewed on their profile.

## 4.2 References

Reference Platform: <https://twitter.com/>

IEEE Std 830-1998(R2009)
