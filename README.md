# Netflix RS

## Bussiness Problem:
	1) Why we are buliding recommendation system?
		- The need to build robust movie recommendation systems is extremely important given the huge 
		  demand for personalized content of modern consumers.
		- Once at home, sitting in front of TV seems like a fruitless exercise with no control and no 
		  remembrance of content that we consumed. 
		  Netflix is an intelligent platform which understands our tastes and preferences and not just 
		  run on autopilot.
		- The main goal to build this recommendation system is to connecting people with movies that 
		  they love. To help customers find those movies, they developed world-class movie 
		  recommendation system: CinematchSM by NETFLIX.
		- Actually its job is to predict whether customer will enjoy a movie based on how much they 
		  liked or disliked the other movies.
		  By using that prediction netflix build personal RS for each customer based on their tastes. 

## Objetive and Constraints:
		1) Predicting ratings that would a customer give to a movie that he has not yet rated.
		2) Minimizes the difference between actual and predicted rating.(RMSE).

### Constarints:
		1) No low latency required.
		2) some form interpretability needed.
		
## Data Source
	- https://www.kaggle.com/netflix-inc/netflix-prize-data/data
	
## ML Problem:(TASK)
		For given movie and user we have to predict rating that would given by him/her to a movie.
		- Given problem is Recommendation problem.
		- It seems like regression problem

## Goal: 
	To recommend new movies(item I_j) to user u_i that most likely to watch.

## 3 Types of Alg. (Approaches):
	1) Popular Movies: 
		This algorithm handpicks trending content on the platform and recommends these movies 
		to all the users. 
		There is a major absence of personalization since every user would be shown same content. 
		It also implies prominence of clickbait content with eye-catching thumbnail. 
		This algorithm fails to showcase the vast repository of titles available on platform.
		
	2)User based Collaborative filtering (CF):
		Recommend movies/things on the basis of users history and other users past activity
		It shows what movies other users are watching and assumes that other would watch similar content. 
		It tries to create a personal/watchlist of every user before movie recommendations. 
		The major problem is cold-start problem when a new user arrives on platform and the engine 
		isn’t able to fire right reccos due to absence of user history. 
		It also assumes its users to be logical and their movie choices to be representative of their 
		true taste. 
		But there arises a situation where all the users are watching similar content based on 
		thumbnail and thus similar content is repeated for every user. 
		It is a vicious cycle with similar movies being repeated in loop and again the variety of 
		content never surfaces upfront.
		
	3)Item based filtering:
		First thing first, it does not need any user level data and the recco. engine can be up 
		and running even in an isolated home PC (No data privacy issue). 
		The algorithm relies on the basic assumption of why a user is watching a movie, is it 
		due to actor or director or war scene or revenge or based on novel? (Based on this each user's 
		profile is generated, which then used to make suggestion to each user.
		As user take more action on that recommendation then RS becomes more & more accurate for that user).
		This understanding of consumer mindset forms most important part in predicting what the user 
		would watch next?

## DATA:
	#movie  : 17K
	#Users  : 480K
	#ratings: 100M    
	
## Referred Sources:
	- https://www.kaggle.com/netflix-inc/netflix-prize-data
	- Blog: https://medium.com/netflix-techblog/netflix-recommendations-beyond-the-5-stars-part-1-55838468f429
	- surprise lib.: http://surpriselib.com/
	- surprise lib. doc: http://surprise.readthedocs.io/en/stable/getting_started.html (i use many models from this library)
	- Research paper: http://courses.ischool.berkeley.edu/i290-dm/s11/SECURE/a1-koren.pdf 

## Blog_link:
