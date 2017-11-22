# HackeNewsCloneDoc 

Requirements Analysis Document
1. Introduction
       1. Purpose of the system
       Social news website where people can share news, connected to computer science and entrepreneurship

       2. Scope of the system
       The system is ought to act as a clone of the existing website Hacker News. Hacker News is a website that present news written by it’s users. The website’s content is described as "anything that gratifies one's intellectual curiosity"[1] by its founder Paul Graham. On the website each content can be up or down voted and can be commented on by other users. Everybody can become a member of the website, but to downvote a content one must have accumulated 500 karma points. Karma points are given to users as the sum of up and down votes on their content.

       3. Objectives and success criteria of the project 
       The website displays content, signs up and signs in users. The system has an API that can receive content directly in JSON format, should return system status and latest post. The website is deployed to a publicly visible server. After going live, the system must have an uptime > 95%. The system shouldn’t 'loose' any content, sent to it from the simulator program. There should be a mechanism buffering incoming content, to be published to the system when it is operational again.
      
       4. Definitions, acronyms, and abbreviations 
- Hacker News Clone (HNC) – name of the system to be developed
- The words system and website refer to Hacker News Clone. 
- News, news article content and post refer to website’s content 
- API - Application programming interface
- front-end of a system – textual or graphical user interface
- back-end of a system - process information in response to front-end system requests and operations
- karma – points equal to the sum of upvotes-downvotes on a user’s own content-

5. References
[1] Hacker News website: https://news.ycombinator.com/
[2] Graham, Paul. "Hacker News Guidelines". Retrieved 2009-04-29.

       6. Overview
       HNC can present news articles. Guests can view articles, sign up and sign in to the website. After signed in they can create new articles, leave comments and vote on articles.
       HNC API component can give system status, show latest post and receive content.
       
2. Current system
HNC will be developed as a new stand-alone system.

3. Proposed system
        1. Overview
The system consists of a database operated by a the back-end. With front-end for the website and an API component.

        2. Functional requirements

- HNC can store text content in a database, the time it was posted, its up-votes, down-votes, and comments. 

- HNC can present that content in a user interface. 

- HNC can register new users in the system by creating a new user profile with user name and password.

- Users can log into the website by providing their user name and password.

- Users can post new content.

- Users can write comments on a specific content.

- Users can vote up or down for a specific content

- Simulator can retrieve the status of the system.

- Simulator can retrieve the latest post from the system.

- Simulator can submit content to the system. The content is kept by the system.


        3. Nonfunctional requirements
          1. Usability
- The website is deployed to a publicly visible server.
- The front page of the website should display content so it’s more convenient for user to view news.

          2. Reliability 
- After going live, the system must have an uptime > 95%. 
- The system shouldn’t 'loose' any content, sent to it from the simulator program. 

          3. Performance 
-The system 

          4. Supportability 

          5. Implementation 

          6. Interface

          7. Packaging

          8. Legal

        4. System models
          1. Scenarios
Actors:
Guest – A guest of the system can view posts but cannot comment or vote on them. A guest can create an account in the system or login if has an existing account.

User – An existing user of the system can view, upvote, downvote and comment on posts. A user can add new posts. Log out of the system. 

Simulator – A program that can get the status of the system, can see latest digested post and can accept new posts.

Scenarios: 
- Scenario name: View news
Participating actor instances: Joe as Guest
Flow of events:
1. Joe is interested in hacker news.
2. He goes on HNC website. 
3. Joe is presented with HNC front page, that contains hacker news.

- Scenario name: Share news article
Participating actor instances: Bob as User
Flow of events:
1. Bob wants to leave a comment on a hacker news article. 
2. He goes on HNC website and views the front page. 
3. He clicks the button on top named “New post” ad is presented with “New post” page.
4. Bob enters the post’s title and text. 
5. He clicks a button called “Post”. 
6. Bob is presented with page containing his new post.

- Scenario name: Up-vote a news article
Participating actor instances: Bob as User
Flow of events:
1. Bob goes on HNC website and views the front page.
2. He browses news.
3. Bob clicks on an article and gets redirected to a separate page containing this article.
4. Bob clicks “up” button to vote up for an article.

- Scenario name: Down-vote on a news article
Participating actor instances: Bob as User
Flow of events:
5. Bob goes on HNC website and views the front page.
6. He browses news.
7. Bob clicks on an article and gets redirected to a separate page containing this article.
8. Bob clicks “down” button to vote down for an article.

- Scenario name: Comment on a news article
Participating actor instances: Bob as User
Flow of events:
1. Bob goes on HNC website and views the front page.
2. He browses news.
3. Bob clicks on an article and is presented with a separate page containing this article.
4. Bob enters comment in text input field called “Comment”.
5. Bob clicks “Comment” button.


- Scenario name: Sign up 
Participating actor instances: Joe as Guest
Flow of events:
1. Joe wants to sign up on HNC website.
2. He goes on HNC website and views the front page.
3. Joe clicks on “Sign up” button on top and gets redirected to “Sign up” page.
4. Joe enters his desired username and password and clicks “Sign up”.

- Scenario name: Sign in 
Participating actor instances: Bob as User
Flow of events:
1. Bob wants to sign in to HNC website.
2. Bob goes on HNC website and views the front page.
3. Bob clicks on “Sign in” button on top and gets redirected to “Sign in” page.
4. Bob enters his username and password.
5. Bob clicks “Sign in” and gets redirected to front page.


- Scenario name: View system status
Participating actor instances: iBob as Simulator
Flow of events:
1. iBob wants to view the status of the website. 
2. iBob goes on the website’s url + “/status”.
3. iBob views the website status: Alive, Update, or Down.

- Scenario name: Post news article
Participating actor instances: iBob as Simulator
Flow of events:
1. iBob wants to POST a story to the website’s API. 
2. iBob goes on HNC website’s URL + “/post”.
3. iBob sends a news article in JSON format to that URL. 
4. The website saves the article.


- Scenario name: View latest post
Participating actor instances: iBob as Simulator
Flow of events:
1. iBob wants to view latest post. 
2. iBob goes to HNC website’s URL + “/latest”.
3. iBob receives latest article. 

          2. Use case model

Use case name: View news
Participating actors: Guest
Flow of events:
       Guest: visits HNC website
       HNC: returns front page, that contains a list of hacker news.
Entry conditions:
Exit conditions: Guest views hacker news.
Quality requirements:

Use case name: Sign up
Participating actors: Guest
Flow of events:
       Guest: clicks on “Sign up” button from the navigation bar.
HNC: returns “Sign up” page.
Guest: enters username and password and clicks “Sign up” button.
HNC: Registers a new user profile for Guest in the database and returns home page.
Entry conditions: Guest is on HNC front page 
Exit conditions: Guest has been registered on the system.
Quality requirements:

Use case name: Share news
Participating actors: User
Flow of events:
User: clicks “New post” button from navigation bar on top.
HNC: returns “new post” page.
User: enters the post’s title and text and clicks “Post” button. 
HNC: returns “Post” page, containing the post. The post is saved in HNC database.
Entry conditions User is logged in. User is on HNC front page.
Exit conditions: HNC has saved user’s post to the database
Quality requirements:

Use case name: Vote on an article
Participating actors: User
Flow of events:
User: clicks either “up” or “down” buttons to vote up or down for an article. 
Entry conditions User is logged in. User is viewing “Post” page.
Exit conditions: The up or down votes for that post change.
Quality requirements:

Use case name: Comment on an article
Participating actors: User
Flow of events:
User: enters comment in text input field called “Comment” and clicks “Comment” button.
HNC:  updates “Post” page with user’s comment and saves the comment to the HNC database.
Entry conditions User is logged in. User is viewing “Post” page.
Exit conditions: User’s comment is present in HNC database.
Quality requirements:

Use case name: Sign in
Participating actors: User
Flow of events:
       User: clicks on “Sign in” button on top.
       HNC: returns “Sign in” page.
       User: enters his username and password and clicks “Sign in” button
       HNC: returns front page and saves the current user as logged in.
Entry conditions: User is not logged in. User is on HNC front page.
Exit conditions: User is logged in.
Quality requirements:

Use case name: View system status
Participating actors: Simulator
Flow of events: 
Simulator: visits website’s URL + “/status”.
HNC: returns the website’s status: Alive, Update, or Down.
Entry conditions: 
Exit conditions: Simulator is aware of the HNC current state.
Quality requirements:

Use case name: Post article
Participating actors: Simulator
Flow of events:
Simulator: sends a news article in JSON format to website’s URL + “/post”.
HNC: Saves post in database. 
The website saves the article.
Entry conditions: Simulator knows JSON format of post class.
Exit conditions: System has saved the post in HNC database
Quality requirements:

Use case name: View latest article
Participating actors: Simulator
Flow of events:
Simulator: visits website’s URL + “/latest”.
HNC: returns latest article from database. 
Entry conditions: 
Exit conditions: Simulator receives the latest article from database
Quality requirements:


       4. Glossary


