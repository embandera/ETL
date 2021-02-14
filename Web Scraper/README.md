### Python Web Scraper using Selenium and XPath

##### Project Overview: What insights can educators leverage from an analysis of university course offerings this Fall? How can course offerings provide insight on the impact of COVID-19 to international students and universities? 

I attempt to explore these questions by scraping a university's course listings, building a SQL database and connecting the data to Tableau, with a goal of building an interactive visualization that can permit non-technical educators in the field of international education to

* find out what times international students abroad are logging on to attend courses scheduled in PST (or students not on PST time) 
    * assess the time differences and impact of unusual study times on student academic experience
* estimate the number of students who might be impacted / studying outside in non-PST time zones
* find out how many courses are being offered at certain PST times and how these translate to other time zones 
* plan for actionable recommendations that can be made to university advisors and educators 
    * such as, exploring the need for accomodations, recorded lectures, alternate test-taking times 

##### Background
Through my advising and participating in university events, I first learned that some international students were having difficulty with adjusting to taking courses scheduled in PST. Many international and domestic students have returned home to continue their studies during the pandemic, and are taking courses outside of the PST time zone. I had a feeling that this was important, and a topic I was eager to help find a solution for. But just how many students were being impacted by this? What was the magnitude of the problem? The questions around scope tend to come to mind first, as an educator working in a large university. The academic experiences of international students (and students in general during this time) are tougher than normal and issues abound. But I thought this particular issue might be impacting enough students to be of high concern. I wasn't exactly sure what the lanscape of courses/time zones looked like, and I suspected other educators might have felt limited in the same way. I thought that if educators could better understand the problem, they might be able to come up with solutions. 

I recently heard a TWIML podcast episode with [Sal Khan](https://www.youtube.com/watch?v=qjTKUZIPxLk) where Sal urges educators to look at education initiatives during the pandemic in the context of disaster relief. By thinking about the current state of education in the pandemic as a disaster, I was inspired to place an even greater level of concern for students and especially those who are being disproportinately impacted. One of the first populations that comes to mind, is international students and those who have returned home and are attending univrsity virtually. 

I had also recently been part of conversations around the questions first discussed in the project overview above: How were international students abroad adjusting to taking their PST-based courses? What challenges were they experiencing? 

I was eager to find out the details of this issue and provide a tool for other educators to assess the situation and apply their own experience towards finding solutions or making recommendations. 

##### Building the web scraper 
The other incentive I had for pursuing this project, was the opportunity to gain experience with building out a Python web scraper. I started by studying how to build a Python webscraper using Beautiful Soup but after a couple of hours, I realized that I would need to do some more research because the code I was writing wasn't working and wasn't locating the elements I needed like course times. I didn't have experience with other web scraping tools at that point, so I started to Google. I found a [student's project](https://nathansmith.io/posts/scraping-enrollment-data-from-the-ucla-registrar-part-one) sharing their own experience scraping the same course enrollment website. I saw that they also attempted to use Beautiful Soup and Python but moved on to other languages after discovering there was a lot more dynamic content than they expected and would need to use another tool or language. I thought that I might be able to retrace the student's steps, but I saw them jump to building the scraper using methods I was even less familiar with like writing code in Javascript and Go. 

I thought I would take a step back and stick with Python, and research other ways I could leverage Python to scrape the course enrollment website. In reading the student's article above, I also found another [cool project](https://stack.dailybruin.com/2018/11/08/how-long-are-lectures/) using information that was scraped and published as an analysis of lengths of lectures on the university's blog. The project had used a scraper built with Selenium. Seeing the second project gave me an extra boost of confidence that I could use Python and Selenium, and off I went, into the world of Youtube code tutorials. I wanted to learn how to leverage Selenium and sure enough, I found a couple of great tutorials like [this one](https://www.youtube.com/watch?v=zjo9yFHoUl8) and [this one](https://www.youtube.com/watch?v=Xjv1sY630Uc&t=605s). I learned that I could use XPath to locate the elements I needed and just enough about XPath to leverage it in this project so far. I did bookmark three or four lengthier tutorials on XPath that I plan to come back to. Definitely an interesting and powerful method of locating dynamic elements!  

##### Currently
I am building out the web scraper using Python, Selenium and XPath and focusing just on building a working web scraper for the courses offered in the Computer Science department. Once I am able to do this, I'll have the web scraper search through the rest of the course subject areas. I plan on passing the retrieved data to a csv and conducting a brief EDA before moving to pass the data to a database I build with PostgreSQL. I might decide to just connect the csv to Tableau but I think a database with the capacity to continuously store data that is being scraped might be a good idea.  

##### Next Steps 
* Brief Exploratory Data Analysis 
* Build SQL Database 
* Connect to Tableau and build an interactive dashboard 
