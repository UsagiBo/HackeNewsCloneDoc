# HackeNewsCloneDoc 

Use Case Model
Contents
Use Cases	1
Actors	3
Use Case Diagram	4
Definitions, acronyms, and abbreviations	5


Use Cases

Name: View news
Primary Actor: Guest
Brief description: Guest views news on website.
Main success scenario:
       Guest: visits HNC website
       HNC: returns front page, that contains a list of posts.
Precondition:
Success guarantees: Guest views hacker news.
Special Requirements

Name: View article
Primary Actor: Guest
Brief description: Guest views a news article website.
Main success scenario:
      Guest: visits HNC website
      HNC: returns front page, that contains a list of posts.
	Guest: clicks on article name
	HNC: returns “Post” page with post content.
Precondition:
Success guarantees: Guest views article.
Special Requirements


Name: Sign up
Primary Actor: Guest
Brief description: Guest creates new user profile. 
Main success scenario:
	Guest: clicks on “Sign up” button from the navigation bar.
	HNC: returns “Sign up” page.
	Guest: enters username and password and clicks “Sign up” button.
	HNC: Registers a new user profile for Guest in the database and returns home page.
Precondition: Guest is on HNC front page 
Success guarantees: Guest has been registered on the system.
Special Requirements

Name: Share article
Primary Actor: User
Brief description: User creates new post.
Main success scenario:
	User: clicks “New post” button from navigation bar on top.
	HNC: returns “new post” page.
	User: enters the post’s title and text and clicks “Post” button. 
	HNC: returns “Post” page, containing the post. The post is saved in HNC database.
Precondition: User is logged in. User is on HNC front page.
Success guarantees: HNC has saved user’s post to the database
Special Requirements

Name: Vote on an article
Primary Actor: User
Brief description: User votes for an article.
Main success scenario:
	User: clicks either “up” or “down” buttons to vote up or down for an article. 
Precondition: User is logged in. User is viewing “Post” page.
Success guarantees: The up or down votes for that post change.
Special Requirements

Name: Comment on an article
Primary Actor: User
Brief description: User comments on an article.
Main success scenario:
	User: enters comment in text input field called “Comment” and clicks “Comment” button.
	HNC:  updates “Post” page with user’s comment and saves the comment to the HNC database.
Precondition: User is logged in. User is viewing “Post” page.
Success guarantees: User’s comment is present in HNC database.
Special Requirements

Name: Sign in
Primary Actor: User
Brief description: User logs into the website.
Main success scenario:
       User: clicks on “Sign in” button on top.
       HNC: returns “Sign in” page.
       User: enters his username and password and clicks “Sign in” button
       HNC: returns front page and saves the current user as logged in.
Precondition: User is not logged in. User is on HNC front page.
Success guarantees: User is logged in.
Special Requirements

Name: View system status
Primary Actor: Simulator
Brief description: Simulator gets system status.
Main success scenario: 
	Simulator: visits website’s URL + “/status”.
	HNC: returns the website’s status: Alive, Update, or Down.
Precondition: 
Success guarantees: Simulator is aware of the HNC current state.
Special Requirements

Name: Post article
Primary Actor: Simulator
Brief description: Simulator posts an article.
Main success scenario:
	Simulator: sends a news article in JSON format to website’s URL + “/post”.
	HNC: Saves post in database. 
The website saves the article.
Precondition: Simulator knows JSON format of post class.
Success guarantees: System has saved the post in HNC database
Special Requirements

Name: View latest article
Primary Actor: Simulator
Brief description: Simulator gets latest article
Main success scenario:
	Simulator: visits website’s URL + “/latest”.
	HNC: returns latest article from database. 
Precondition: 
Success guarantees: Simulator receives the latest article from database
Special Requirements

Actors

Actors:
Guest – A guest of the system can view posts but cannot comment or vote on them. A guest can create an account in the system or login if has an existing account.

User – An existing user of the system can view, upvote, downvote and comment on posts. A user can add new posts. Log out of the system. 

Simulator – A program that can get the status of the system, can see latest digested post and can accept new posts.

Use Case Diagram

  

Definitions, acronyms, and abbreviations 
- Hacker News Clone (HNC) – name of the system to be developed
- The words system and website refer to Hacker News Clone. 
- News, news article content and post refer to website’s content 
- website’s URL – the address of HNC website, from where it will be accessible from

