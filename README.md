# Microsoft Codefundo++ 2018 (Team Sorcerers)

## Who are we

We are a group of three sophomore students. The team members are as follows:

1. Anuprava Chatterjee (@theartist007)
2. Navaneeth Suresh (@themousepotato)
3. Shivam Kumar Jha (@thealphadollar)

All three of us are from different regions and different backgrounds and have diverse understanding of the conditions of calamities in our region. This would, I believe help us in fabricating a better solution.

## What are we planning to build

We are planning to build a service to help save lives and prevent economic losses through mechanisms to predict, prevent, or manage the impact of natural disasters, as accurately as possible and feasible using the dataset procurable.
The service would :

1. Predict (show probability) the possibility of a natural disaster, in any given location, set by the user.

2. Show the user / refief providers the most appropriate area to set the camp in.

3. Guide the user to all the relief points such as government schools, hospitals and police stations located within a specified radius and also provide guided path to the nearest one of them.

4. Provide user with valuable precautions which can be implemented well in advance based on the geography and topograghy of the location the user resides in. These tips will be such as "build houses with x type of pillars to ensure sturdiness at times of earthquake".

5. A person would also be able to list the danger he is in, and accordingly a response team can be assigned to him (or can volunteer to help him). A distress receiver and responder will be made available.

6. Relief centres can list the type of services they can provide and the area they can cover and accordingly people can request and post about their needs on the forum. At times of ongoing disasters, a critical dynamic page will list all of these for each geographical area separately.

7. Show data of previous natural disasters of the area, and grossly present the damage done by them to property and life.

## How does it work

Each bullet point has been explained with accordance to it's order in the previous heading.

1. Using the global dataset available (which is, frankly, not up to the mark) we can form a pattern in the occurence of global disasters and combining it with the suspectibility of a disaster according to geography, we can come up with probability of various disasters occuring in near future.

2. Will be done by parsing an user's location (or manually taking it for relief centres) and then assessing the population density distribution of the area (in peace times) and also the impact of the disaster if any ongoing. Through testing multiple algorithms, a suitable weight will be chosen for the two.

3. In a similar manner as above, once an user's location is received we can show him the locations on a map and have a path set to the nearest station; both graphical and textual manner.

4. Dividing the area based on disaster data; such as earthquake prone, flood prone and then accordingly devising a set of precautions and instructions which can help lower the damage done to life, property and other assets.

5. A separate "specific" dashboard shall be created for users / relief providers to interact and list the items they need / provide and the list is curated in a database and will be used in sync to match the needy with the providers at the right places and quickly.

6. Same as above; just different dashboard for relief centres and multiple other options so they can mark what all they have, and if they are occupied at the moment in some relief operation.

7. This can be done easily using the available surveys and records, arranging them in a suitable JSON-like format so that template pages can be filled with them.

## How users can get started with the project

The project will be provided as a web application in order to pass the hurdle of platform limitation. A simple, elegant and intuitive user interface will be provided along with a simple "help" to get the users as well as relief providers get started with the platform. Since the application will be a webApp, in the future it'll be easier to create mobile apps for the same.

The user will get a map-view of the location he is in, upto a certain radius, which will show locations of relief centers and the  directions to the nearest of them. They can also get personlaised help options, and relief procedures based on their reponse in the forum. There will be multiple dynamic dashboards for different features such as maps, past data, relief calls etc.

An appealing feature of the website will be the implementation of the SMS (and telephonic, if time permits) endpoints. This will ensure that the people without internet can also gather information and send help calls to the website without having to go to the website. This will be done as any other automated SMS API endpoint works; a set of keywords to recognize the type of message and then providing all the services (for example providing textual directions to the nearest relief point) through SMS.

## What dataset(s) are we using

We are planning to build a web app based on the dataset of whole world (or anything close to it). We've been testing data from [gisresources](http://www.gisresources.com/natural-disasters/) or [emdat](https://www.emdat.be/) on various scenarios. Due to the vastness of the dataset, it is not viable to train the deep learning models on our systems, and hence Azure Cloud Resources will be utilized in the process of assessment of various datasets and gauging their accuracy.

We will be using multiple geographical data to decide the zones of disaster prone areas, and population density. We will also procure (or produce) data for predicting and providing precautions according to the divison of zones.

Specifically for the part of prediction, we need to look at the pattern of natural disasters for the past decades and draw a pattern and then deduce the possibility and effects of a disaster in an area. The estimate of future damage will be based upon past data and will be calculated using simple data analysis techniques.

## What technologies are we using

- Python 3.6.5 with Pipenv
- Javascript
- HTML5 + CSS3
- GitHub for hosting
- [Microsoft Azure Data Science Virtual Machine](https://azure.microsoft.com/en-in/services/virtual-machines/data-science-virtual-machines/) for training prediction models
- Microsoft Azure Cloud for deployment
- [Docker](https://www.docker.com/) to deploy as containers by handling microservices 
- [Flask](http://flask.pocoo.org/)
- [Elasticsearch](https://www.elastic.co/products/elasticsearch) as a distributed RESTful search engine
- [Twilio SMS API](https://www.twilio.com/docs/sms)
- Maps API (Opensource such as [ModestMaps](http://modestmaps.com/) or [Leaflet](https://leafletjs.com/))
- SQL Database as a service from [Azure](https://azure.microsoft.com/en-in/services/sql-database/).

## Final Notes

We will be trying to give equal resources and time to every field of the problem statement but our main object will be to create a system which can help at the times of disaster; and is even remotely accessible (by SMS for instance). A simple interactive platform between helpers and needy will go a long way in improving the scenario and dependency on various social media platforms. We also have the plan (a fat-fetched one) of embedding a system in the platform where people can add family members and then at times of disaster mark themselves safe (or in danger) and our system will do the hardwork of carrying their message to all. 

We will be testing the technologies (mentioned above) and assessing if they need to be improved (or changed) to achieve the optimum efficiency for the goal.