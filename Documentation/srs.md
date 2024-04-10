<div align="center"><h1>X CLONE</h1></div>
<div align="center"><h2>Requirements Specification</h2></div>
<div align="center"><p>COS 301 Mini Project - Group MP9</p></div>

[Link To Requirement Specification PDF](https://drive.google.com/file/d/1XdLuJ3q4FsKShKNaWJm6MnCjJn4FWvCR/view?usp=sharing)

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
   
  - [3.2 Subsystems and Use Case Diagrams](#32-subsystems-and-use-case-diagrams)
 
    - [3.2.1 Authentication and User Management Subsystem](#321-authentication-and-use-managemen-subsystem)
   
    - [3.2.2 Content Creation and Management Subsystem](322-content-creation-and-management-subsystem)
   
    - [3.2.3 Interaction and Display Subsystem](#323-interaction-and-display-subsystem)
   
    - [3.2.4 Notification Subsystem](#324-notification-subsystem)
   
    - [3.2.5 Reporting and Help Subsystem](#325-reporting-and-help-subsystem)
   
    - [3.2.6 Role Management Subsystem](#326-role-management-subsystem)

  - [3.3 Quality Requirements](#33-quality-requirements)
    
    - [3.3.1 Performance](#321-performance)

    - [3.3.2 Security](#332-security)

    - [3.3.3 Portability](#333-portability)

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
The main function of X Clone is to provide a platform on which users can interact and share content with one another. Users of the product will be able to register with and create accounts on the platform. They can then use their account to interact with the platform through tweeting, retweeting, liking, following, and commenting.  The product essentially provides an online environment in which its users can communicate and share content with one another through a variety of features.

## 2.2 User Characteristics
This subsection of the SRS should describe those general characteristics of the intended users of the product including educational level, experience, and technical expertise. It should not be used to state specific requirements, but rather should provide the reasons why certain specific requirements are later specified in Section 3 of the SRS. 

**1\. General Users:**
These users form the vast majority of the user base. They generally don’t have a large amount of technical expertise but are likely to have some form of familiarity with online social media platforms. A general user would interact with the X Clone platform by creating an account, editing their profile, and utilizing the various forms of engagement with other users provided by the product.

**2\. Premium Users:**
Premium users form a subsection of general users. These users would generally interact with the platform in the same manner as general users, but have access to certain “perks”, like an increased character limit for their tweets, which are only available to them. Premium users also have a specific icon which appears next to their username, which indicates their premium status. On the reference platform, general users can attain a premium status by purchasing it, but this project implements a system whereby general users can apply for a premium role, and administrative users can approve or deny the request. 

**3\. Administrative Users:** 
These users moderate the platform and interact with the administrative and role system. 

## 2.3 Constraints
There are a number of constraints by which the X Clone system must abide. The project’s constraints, as detailed below, have been set by both the project owner, and by the development team. 

- C1.  X Clone’s implementation must use Supabase. 
- C2.  X Clone and its contents need to be appropriate for a professional environment. 
- C3.  The frontend frameworks that may be used in the development of X Clone are limited to Angular, React, Vue, Svelte, or Flutter. X Clone uses React in particular. 
- C4.  The backend frameworks that may be used in the development of X Clone are limited to Vanilla JavaScript/Typescript/Python using the Supabase libraries with the option of additionally using NestJS/Express/Fastify/Python FAST API. X Clone uses JavaScript and TypeScript in particular. 
- C5.  The structure of X Clone must adhere to a client-server architecture. 
- C6.  X Clone’s design must be kept minimalistic and must exactly replicate that of the reference platform X. 
- C7.  The development of X Clone must make use of an existing component library.  This project uses the Material UI React component library. 
- C8.  X Clone’s deployment must take place through a CI/CD process.

<br>

# 3\. Specific Requirements

## 3.1 Functional Requirements

The following functional requirements are organized by user class.

### 3.1.1 General Users

The *X Clone* system shall: 

**R1**  Provide a secure user registration and authentication process to users.
- **R1.1**  Allow users to create an account. 
  - **R1.1.1**  Require users to provide a unique username, password, and email address.
- **R1.2**  Require users to verify their email address before they have full access to their account.
  - **R1.2.1**  Send a verification code to the email address provided by the user.
  - **R1.2.2**  Require the user to input this code.
  - **R1.2.3**  Verify that the user’s input matches with the emailed code. 
  - **R1.2.4**  Subsequently, give the user full access to their created account.
<br><br>

**R2**  Allow users to create and post content.
- **R2.1**  Allow users to compose tweets with text that is limited to 280 characters. 
- **R2.2**  Allow users to attach images and videos to their tweets.
- **R2.3**  Allow users to post their tweets to the platform.
- **R2.4**  Allow users to edit or delete their own posted tweets. 
- **R2.5**  Allow users to accept or reject an invite to partake in a collaborative post.
<br><br>

**R3**  Allow users to view posted content. 
- **R3.1**  Provide a homepage which displays posts in reverse chronological order.
  - **R3.1.1**  Provide a “Following” timeline which exclusively displays posts from accounts that the user follows. 
  - **R3.1.2**  Provide a “For you” timeline which displays recent tweets from all users on the platform. 
  - **R3.1.3**  Enable a user to refresh their current timeline in order to display new tweets that have been posted from when the timeline was last loaded.
<br><br>

**R4**  Allow users to interact with content. 
- **R4.1**  Allow users to like tweets. 
- **R4.2**  Allow users to retweet tweets. 
  - **R4.2.1**  Post the retweeted tweet to the user’s own profile and followers’ timelines.
- **R4.3**  Allow users to comment on tweets and can delete or edit their own comments.
  - **R4.3.1**  Allow users to edit or delete their own comments.
- **R4.4**  Track and display the timestamp, likes, comments, and retweets on each tweet.
<br><br>

**R5**  Allow users to view their own and other’s profiles. 
- **R5.1**  Display a user’s tweets, retweets, followers, and following list on their profile.
<br><br>

**R6**  Allow users to manage their profiles. 
- **R6.1**  Allow users to edit their profile picture, bio, display name, email address, and password. 
- **R6.2**  Allow users to manage the visibility of their profile. 
  - **R6.2.1**  Allow users to set their profile to public or private. 
  - **R6.2.2**  Adjust the profile’s visibility based on the user’s selection.
- **R6.3**  Allow users to deactivate or delete their accounts.
  - **R6.3.1**  Provide users with the option deactivate or delete an account.
  - **R6.3.2**  Confirm the user’s choice by requiring them to input their password. 
  - **R6.3.3**  Remove relevant data or adjust account visibility based on the user’s choice.
<br><br>

**R7**  Allow users to edit their application settings. 
- **R7.1**  Include a settings page where users can edit visual and accessibility preferences. 
- **R7.2**  Implement users’ preferences to their application.
<br><br>

**R8**  Allow users to receive and view notifications. 
- **R8.1**  Provide notification services to users for likes, comments, and new followers on their profile. 
- **R8.2**  Include a notifications page where users can view all their notifications.
- **R8.3**  Implement toast notifications to display system notifications. 
<br><br>

**R9**  Allow users to search for specific content and accounts.
- **R9.1**  Include a search page with a search bar and filters. 
- **R9.2**  Display users and posts which match the search criteria.
<br><br>

**R10** Allow users to report tweets and accounts that violate community guidelines.
<br><br>

**R11** Provide a help page with contact information for where users can request assistance.
<br><br>

**R12** Allow users to request their account be upgraded to a premium user role.
<br><br>

### 3.1.2 Premium Users

Requirements **R1** and **R3** - **R11** are applicable to premium users. Additional requirements for this group are detailed below. 

The *X Clone* system shall:

**R13** Allow users to create and post content.
- **R13.1** Allow users to compose tweets with text that is limited to 1000 characters.
- **R13.2** Allow users to attach images and videos to their tweets.
- **R13.3** Allow users to post their tweets to the platform.
- **R13.4** Allow users to edit or delete their own posted tweets. 
- **R13.5** Allow users to accept or reject an invite to partake in a collaborative post.
- **R13.6** Allow users to create collaborative posts.
  - **R13.6.1**  Allow users to create a tweet and invite other users to accept or reject a request to collaborate on the tweet. 
  - **R13.6.2**  Post the tweet to the profiles and follower timelines of the collaborators who accepted the request. 
<br><br>

**R14** Display a badge next to premium users’ usernames to indicate their role. 

### 3.1.3 Administrative Users

Requirements **R1** - **R12** are applicable to administrative users. Additional requirements for this group are detailed below. 

The *X Clone* system shall: 
**R15** Allow users to change other users’ roles to premium user. 
- **R15.1** Allow users to view premium user applications. 
- **R15.2** Allow users to accept or reject the request.
<br><br>

**R16** Allow users to invite other users to take on an administrative user role. 
<br><br>

**R17** Allow users to view and edit a list of reported tweets and user accounts. 
<br><br>

## 3.2 Subsystems and Use Cases
The following subsystems and associated use case diagrams have been identified from the functional
requirements provided in section 3.1:

### 3.2.1 Authentication and User Management Subsystem
This subsystem deals with account creation and authentication, profile and account management, and
application settings. It includes fulfils R1, R6, and R7 (including their sub-points).
<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1K1ukcUyH7KAQn_ESDUFPaHHPvoJV3F3S">
  <br>
  <em>Figure 1: Authentication and User Management Subsystem Use Case Diagram</em>
</p>
<br><br>

### 3.2.2 Content Creation and Management Subsystem
This subsystem handles the creation, posting, and subsequent editing and deleting of tweets and
collaborative posts. It fulfils requirements R2 and R13 (including their sub-points).
<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1Ollhylkr27LlIugiRuc-crYzDzQAzQNP">
  <br>
  <em>Figure 2: Content Creation and Management Subsystem</em>
</p>
<br><br>

### 3.2.3 Interaction and Display Subsystem
This subsystem deals with how users can view, search for, and interact with tweets and other accounts. It
fulfils requirements R3, R4, R5, and R9 (including their sub-points).
<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1314ew0DjF5w_e9yYZVRySt0ji-BPVgwN">
  <br>
  <em>Figure 3: Interaction and Display Subsystem</em>
</p>
<br><br>

### 3.2.4 Notification Subsystem
This subsystem is responsible for managing and displaying notifications related to user interactions and
system messages. It fulfils requirement R8 (including its sub-points).
<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1NLfBBKqZxXJNhlGvEeG-DyIJMEvaIoUR">
  <br>
  <em>Figure 4: Notification Subsystem</em>
</p>
<br><br>

### 3.2.5 Reporting and Help Subsystem
This subsystem involves the creation and management of user reports and providing help to users. It fulfils
requirements R10, R11, and R17 (including their sub-points).
<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1qfKdAUgYlTH4gPLdw0u7EJYLsXjBQHQ0">
  <br>
  <em>Figure 5: Reporting and Help Subsystem</em>
</p>
<br><br>

### 3.2.6 Role Management Subsystem
This subsystem manages users changing their role/user class, including changing from general to premium,
and from general/premium to administrative. It fulfils requirements R12, R14, R15, and R16 (including their
sub-points).
<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1Aosp9y_3AIu0pul29smsub9ccsXrX_AP">
  <br>
  <em>Figure 6: Role Management Subsystem</em>
</p>
<br><br>

## 3.3 Quality Requirements

### 3.3.1 Performance
- **Scalability:** The X Clone system should be able to handle a reasonable number of concurrent users without experiencing a significant reduction in performance. 
- **Response Time:** The response time for fundamental user operations like posting tweets and displaying a timeline should be minimal. Particularly, database queries should be optimized to maintain a high level of performance within the project’s limitations.
- **Error Management:** The system should have a high level of fault tolerance. 
<br><br>

### 3.3.2 Security
- **Authentication:** The user authentication process should be secure to prevent unauthorized access to user accounts. This is implemented using usernames, passwords, and email address authentication.
- **Authorization:** Authorization techniques should be implemented securely to ensure users only have access to data and actions they are permitted to. 
- **Data Storage:** Sensitive user and system data should be stored securely and encrypted where necessary to prevent data breaches and other security threats. 
- **Data Integrity**: Data loss and corruption should be prevented by maintaining data integrity.
<br><br>

### 3.3.3 Portability
- **Cross-Platform Support:**  The system will be accessible and compatible both on mobile and desktop devices. 
- **Interoperability:** The system interacts with other external systems and services. This includes utilizing Supabase, an API, and the MUI library. 

# 4\. Appendix
## 4.1 Acronyms, Abbreviations, and Definitions
- Tweet – A user’s post on X and X Clone’s platforms. 
- Retweet – The act of reposting a tweet from a different user.
- Bio – A short description of a user which can be viewed on their profile.

## 4.2 References
Reference Platform: https://twitter.com/ 

Model for layout of this document: IEEE Std 830-1998(R2009)




IEEE Std 830-1998(R2009) 



