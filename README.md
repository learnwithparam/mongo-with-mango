# MongoDB for full stack developers

Creating a database for learning management system. (e.g., egghead, leveluptutorials, educative.io)

## What will you Learn

- NoSQL concepts
- MongoDB basics
- Data Modelling
- Embedding
- One way embedding
- Two way embedding
- References
- Schema designing best practices
- Aggregation framework
- Learn by doing: LMS (ecommerce) platform

## Features

LMS support a lot of features. Its a type of ecommnerce, infact a complex ecommerce. We will build the whole application database schema and queries in this book.

### Platform

- Platform support courses
- Platform support draft courses (upcoming courses)
- A course can have multiple lessons
- A lesson can have multiple topics
- A topic can be of type - Video (Youtube or Vimeo link), Text (markdown)
- A topic can be locked or unlocked (locked - Only loggedin user can view it, Unlocked - Anyone can view it)
- A topic will have a discussion page
- A discussion page can have multiple questions
- A discussion question can have multiple replies (two level)
- A discussion question can be upvoted / downvoted
- A discussion reply can be upvoted / downvoted
- A course can be either paid or free
- Multiple courses can be bundled together and offered for specific bundle price
- Coupon code supported for each course
- Coupon code supported for each bundle
- Coupon code support expire based on date
- Coupon code also support unlimited validity with window on max number of usage
- Referral token / link generated for each loggedin user

### Visitors

- Visitors can view all courses
- Visitors can view unlocked topics in a course
- Visitors can view the discussion pages
- Visitors can't view locked topics

### User

- Three types of user - Free plan, Pro plan and Enrolled users
- Free users are users who just register to the site and login to explore the platform
- Free users can enroll in free courses
- User can subscribe to pro plan for $16 per month
- User can subscribe for yearly plan for $160 per year
- All subscribed users are auto renewed
- If user opt out for auto renewal, then they will be downgraded to free plan
- User can enroll to individual courses / bundles (enrolled users)
- Pro user can view everything
- Enrolled user can view everything on the courses they enrolled. 
- For non enrolled courses, enrolled user get the same view as free user
- User can use coupons
- Referral link supoorted for each users
- Both referred user and refferal user gets 1 month free pro plan
- Topics will be marked as done once user finishes going through the topic
- Course percentage completion will be calculated
- User can take private notes on each topics
- User can provide feedback for each course (5 Star Rating + Feedback text)
- User can add their personal profile (Bio and Links - Social, Website)
- User can request for new courses through a form
- user can apply to become an author

### Author

- Author will be accepted based on the application
- Author can create a new course
- Author can edit content for their course
- Author can put a course for review (draft courses)
- Course will be published after review
- A course review process have multiple steps - Draft received, Editing, Good to Go, Published
- Author can add their personal profile (Bio and Links - Social, Website)
- Author can see dashboard of his courses
- Author can see the feedback from users
- Author can mark a discussion thread reply as highlighted
- Author can see how many users enrolled and what % they have completed in the course
- Author can see overview for weekly and monthly stats (new enrolls, how many completed their course during the period)
- Author will get revenue share based on how many users active on a course on given month
- Author can see the aggregated data of monthly revenue and active users on their courses
- An active user for the course on particular month should have taken atleast 2 topics in the course (marked as completed)

### Admin

- Admin can view the requested courses from users
- Admin can make a user as author
- Admin can review the draft courses and move to different steps
- Admin can moderate dicussion question and replies (mark as spam)
- Admin can view all authors
- Admin can view the revenue of each authors

### Folder structure

- Domain based folder structure. 
- Create a JSON file for model (model.json) 
- Create mongodb files for each queries and name the query files based on JS convention (ex., save a query file using studio 3T)
- Create seeds folder inside and create seeds JSON files for each models (May be create faker JS based data file if that makes sense and easy)

Example folder structure,

```
users 
courses
topics
coupons
payments
subscriptions
settings
referrals
```

Example for files inside a folder - `courses`

```
model.json
seeds / index.js
queries.js
create-courses.nosql
edit-courses.nosql
add-topics-to-courses.nosql
```

`queries.js` file will contains single line description of all the `.nosql` files.

_Note: The above are just examples, we can modify based on how the project goes_

