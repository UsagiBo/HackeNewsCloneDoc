# HackeNewsCloneDoc 

- front-end of a system – textual or graphical user interface
- back-end of a system - process information in response to front-end 

Refined Use case model

Use case name: View news
Participating actors: Guest
Brief description: Guest views news on website.
Flow of events:
       Guest: visits HNC website
       HNC: returns front page, that contains a list of posts.
Entry conditions:
Exit conditions: Guest views hacker news.
Quality requirements:

Use case name: View article
Participating actors: Guest
Brief description: Guest views a news article website.
Flow of events:
      Guest: visits HNC website
      HNC: returns front page, that contains a list of posts.
	Guest: clicks on article name
	HNC: returns “Post” page with post content.
Entry conditions:
Exit conditions: Guest views article.
Quality requirements:


Use case name: Sign up
Participating actors: Guest
Brief description: Guest creates new user profile. 
Flow of events:
	Guest: clicks on “Sign up” button from the navigation bar.
	HNC: returns “Sign up” page.
	Guest: enters username and password and clicks “Sign up” button.
	HNC: Registers a new user profile for Guest in the database and returns home page.
Entry conditions: Guest is on HNC front page 
Exit conditions: Guest has been registered on the system.
Quality requirements:

Use case name: Share article
Participating actors: User
Brief description: User creates new post.
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
Brief description: User votes for an article.
Flow of events:
	User: clicks either “up” or “down” buttons to vote up or down for an article. 
Entry conditions User is logged in. User is viewing “Post” page.
Exit conditions: The up or down votes for that post change.
Quality requirements:

Use case name: Comment on an article
Participating actors: User
Brief description: User comments on an article.
Flow of events:
	User: enters comment in text input field called “Comment” and clicks “Comment” button.
	HNC:  updates “Post” page with user’s comment and saves the comment to the HNC database.
Entry conditions User is logged in. User is viewing “Post” page.
Exit conditions: User’s comment is present in HNC database.
Quality requirements:

Use case name: Sign in
Participating actors: User
Brief description: User logs into the website.
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
Brief description: Simulator gets system status.
Flow of events: 
	Simulator: visits website’s URL + “/status”.
	HNC: returns the website’s status: Alive, Update, or Down.
Entry conditions: 
Exit conditions: Simulator is aware of the HNC current state.
Quality requirements:

Use case name: Post article
Participating actors: Simulator
Brief description: Simulator posts an article.
Flow of events:
	Simulator: sends a news article in JSON format to website’s URL + “/post”.
	HNC: Saves post in database. 
The website saves the article.
Entry conditions: Simulator knows JSON format of post class.
Exit conditions: System has saved the post in HNC database
Quality requirements:

Use case name: View latest article
Participating actors: Simulator
Brief description: Simulator gets latest article
Flow of events:
	Simulator: visits website’s URL + “/latest”.
	HNC: returns latest article from database. 
Entry conditions: 
Exit conditions: Simulator receives the latest article from database
Quality requirements:



Actors:
Guest – A guest of the system can view posts but cannot comment or vote on them. A guest can create an account in the system or login if has an existing account.

User – An existing user of the system can view, upvote, downvote and comment on posts. A user can add new posts. Log out of the system. 

Simulator – A program that can get the status of the system, can see latest digested post and can accept new posts.


     


