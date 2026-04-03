# Team 7 MIST 4610 Group Project 1

## Team Name: 
Sp26_71552_Group 7

## Team Members:
1. Nandini Chinthapanti [@nandinichr](https://github.com/nandinichr)
2. Sara Gebreyohannes [@saragebree](https://github.com/saragebree)
3. Rajan Malik [@RKMalik-1](https://github.com/RKMalik-1)
4. Landon Tabor [@lptabor63](https://github.com/lptabor63)
5. Reina Wang [@rlwang0314](https://github.com/rlwang0314)

## Problem Description

Our team's task is to model and build a relational database that organizes the E-Sports Tournament Events. The central entity throughout our database is the Tournaments entity which represents the individual E-Sport tournaments in the database. The tournament is operated in correlation to multiple components such as teams, sponsors, games, prize_pools, and matches. Every tournament hosts multiple teams which play matches of E-Sports games organized into different rounds. These tournaments are also supported financially by different sponsors and have multiple prize pools which define the rewards that the teams receive based on their placings. Overall, the structure of the project allows individuals to understand how the tournaments are structured while connected to the variety of other operational entities in the database.


## Data Model 
Explanation of data model: 

Our model represents the structure of an esports tournament management system. It shows the relationships between games, tournaments, teams, players, sponsors, and match activities. 

The Games_Genres table represents different categories of games, such as MOBA and FPS. Each genre can include many games, which is why there is a one-to-many relationship to Games. 

The Games table holds information about each game, like its name and platform. Each game can be in multiple tournaments, so there is a one-to-many relationship between Games and Tournaments. 

Tournaments is the central entity in the data model and stores information about the individual tournaments, such as the name, dates, status, and location. Each tournament can have multiple prize pools, matches, sponsors, and teams associated with it. 

The Prize_Pools table stores information about the monetary rewards for each tournament, including payout status, amount, and currency. Because each tournament can have multiple prize pools, there is a one-to-many relationship between Tournaments and Prize_Pools.

The Sponsors table contains details about each sponsor, such as company name, contact information, and sponsorship amount. Since a tournament can have many sponsors and a sponsor can support multiple tournaments, a many-to-many relationship ties the tables Tournament and Sponsors together. They are connected by the associative table Tournament_Sponsors.

Teams stores information about each team, like name, region, and manager. Each team can have a sponsor, hence the many-to-one relationship between Teams and Sponsors. 

Teams can participate in multiple tournaments, and tournaments must have multiple teams. This results in a many-to-many relationship between Tournaments and Teams, creating the associative table Tournament_Teams.

The Rounds table shows the different stages in a tournament, such as quarterfinals or finals. Each round can have multiple matches, which creates a one-to-many relationship between Rounds and Matches. 

Matches contains details of each match, including date, time, and status. Matches belong to a specific tournament and round, forming many-to-one relationships with both Tournaments and Rounds. 

Because matches involve multiple teams and teams can play in multiple matches, there is a many-to-many relationship between Matches and Teams, connected by the associative table Matches_Teams, which also stores the team position in the match. 

The Players table represents each individual player participating in the tournaments, including details like gamer tag, name, nationality, and role. Players can participate in multiple matches and matches must involve multiple players. This results in a many-to-many relationship between Players and Matches with Player_Stats as the associative table.  

<img width="915" height="759" alt="image" src="https://github.com/user-attachments/assets/dce0a080-a2e1-4103-b49d-1195d36365c4" />


## Data Dictionary 

<img width="725" height="731" alt="image" src="https://github.com/user-attachments/assets/f958a3ed-cb2a-40d3-83c6-175b004d2db4" />

<img width="743" height="667" alt="image" src="https://github.com/user-attachments/assets/bd3b59da-efc4-458a-ae79-cb15e03cdfba" />

<img width="741" height="496" alt="image" src="https://github.com/user-attachments/assets/1ba46ddd-75ef-4192-805b-e5e3247f2509" />

<img width="755" height="564" alt="image" src="https://github.com/user-attachments/assets/5b9ce7d0-8ec1-4109-a2d4-e3ab7c081586" />

<img width="757" height="639" alt="image" src="https://github.com/user-attachments/assets/8f54dde2-925d-4511-9066-07c8abf653fd" />

<img width="729" height="551" alt="image" src="https://github.com/user-attachments/assets/19b30c85-7364-4c8e-9611-0f4eb0a0a71f" />

<img width="735" height="455" alt="image" src="https://github.com/user-attachments/assets/aef141c1-36f3-4742-b88f-78fb27ce9c06" />

<img width="739" height="260" alt="image" src="https://github.com/user-attachments/assets/71c7a445-201d-4e0c-b73d-d86baf6b34f1" />

<img width="752" height="493" alt="image" src="https://github.com/user-attachments/assets/1f68342a-15e8-4159-a99a-c7de53fc9794" />

<img width="1015" height="412" alt="image" src="https://github.com/user-attachments/assets/d46a49e4-64f1-4735-9256-8de2350f2b25" />

<img width="1025" height="400" alt="image" src="https://github.com/user-attachments/assets/3f8952ce-8391-4a49-8c45-3edd5cde87ba" />


## Queries 
<img width="879" height="761" alt="image" src="https://github.com/user-attachments/assets/90b65fe3-8f2f-4920-b46a-23950a17c3fb" />


1. Query 1 shows all the teams from North America.

Natural language question: Which teams are located in the North America region?

<img width="722" height="698" alt="image" src="https://github.com/user-attachments/assets/872f8ca2-86b2-43e8-800a-b2fc972de2d5" />

Query 1 helps management identify all teams operating in North America. This can help management evaluate how well North American teams perform compared to teams from other regions. Knowing which teams are in North America also allows for region-specific sponsorship deals and advertising campaigns. 


2. Query 2 shows sponsor names, the tournament they sponsor, and the donation amount for deals greater than $50,000.

Natural language question: Which sponsors contribute more than $50,000, and which tournaments are they sponsoring? 

<img width="685" height="697" alt="image" src="https://github.com/user-attachments/assets/a83f5c95-238c-4a87-ac79-618e0a0ae8de" />

Query 2 identifies sponsors who contribute high values and the tournaments they support. Management can use this information to determine which tournaments get major funding and which sponsor relationships to prioritize. Tournaments with higher sponsorships may also justify greater resources allocated to it, such as increased marketing and production quality.  


3. Query 3 shows all teams competing in NBA 2K Invitational.

Natural Language Question: Which teams are participating in the “NBA 2K Invitational” and what regions do they represent? 

<img width="567" height="572" alt="image" src="https://github.com/user-attachments/assets/f66ab627-bb2b-4c0c-91bd-e343a3c49366" />

Query 3 helps management identify the teams entered in a specific tournament and understand which region they are from. This can support regional marketing and tournament planning, showing whether a specific tournament has global appeal or if engagement is concentrated in a single region. This information would help match tournaments with sponsorshisp that target specific regions as well. 


4. Query 4 gives an overview of all matches in a tournament. 

Natural language question: What are the names, dates, locations, and statuses of all matches? 

<img width="662" height="655" alt="image" src="https://github.com/user-attachments/assets/dfee1a01-466b-4549-b3eb-069139f591c5" />

Query 4 provides information on all matches and their scheduling information, allowing managers to monitor tournament operations. Management can ensure that no match times overlap and create conflict that could disrupt the tournament. By reviewing match statuses, managers can track progress of each match as well and identify if there have been any delays or setbacks. Knowing the match schedules also helps allocate technical staff, streaming teams, and other operational resources. 


5. Query 5 finds tournaments with more than three teams.
   
Natural language question: Which tournaments with more than three teams?

<img width="617" height="634" alt="image" src="https://github.com/user-attachments/assets/608990f7-c45d-4de6-a6fa-86f827f3828c" />

Query 5 helps management identify tournaments with a larger number of participating teams. This can be useful to them because more teams usually means more resources being allocated to them and more coordination and staffing needed to run the events. Management can use this information to plan venue spaces and streaming staff. Larger tournaments are more likely to be higher-value, so they would need more marketing campaigns and focus on sponsors. 


6.  Query 6 shows tournaments that have more than one sponsor. 

Natural language question: Which tournament has more than one sponsor?

<img width="634" height="680" alt="image" src="https://github.com/user-attachments/assets/fc8cd525-e655-42e5-bf70-40b7ff6e7495" />

Query 6 helps management identify tournaments that attract multiple sponsors, which is an indicator of the value of the event and success. This provides information like where resources should be prioritized. High-sponsored tournaments could justify increased investment in marketing and operations. Market attractiveness can be determined as well. Managers can see which tournaments are more appealing to sponsors, which means more audience reach and stronger brand exposure. 


7. Query 7 shows sponsors whose sponsorship amount is greater than the average sponsorship amount.

Natural language question: Which sponsors contribute more than the average sponsorship amount? 

<img width="827" height="605" alt="image" src="https://github.com/user-attachments/assets/868b7383-d200-44ae-86ce-0fe1c702f4fc" />

Query 7 helps management identify sponsors who contribute above the average funding level, which is important in strategic decision-making. Knowing which sponsors are high value allows management to allocate more time and resources in maintaining that relationship. High-contributing sponsors may be offered exclusive benefits or long-term partnership opportunities. This also helps in revenue analysis, where it can help understand whether revenue is driven by a few major sponsors or many smaller ones. 


8. Query 8 finds the total prize money by game genre, but only for genres whose name starts with “R” or “N”.

Natural language question: For game genres starting with “R” or “N”, how many tournaments are there, what is the total prize money, and what is the average prize pool amount?

<img width="698" height="667" alt="image" src="https://github.com/user-attachments/assets/b181bb72-3977-4b28-a825-0dc9fa1eb1fe" />

Query 8 provides management with aggregated financial and participation information by game genre. This is valuable for market performance analysis, which helps identify which genres (Racing or RTS) are generating more tournaments and higher prize pools. By looking at total and average prize money, management can also determine which genres attract greater finance investment and allocate more time to those. 


9. Query 9 finds teams that have never participated in any tournament.

Natural language question: Which teams have never participated in any tournament? 

<img width="586" height="672" alt="image" src="https://github.com/user-attachments/assets/4a1e1aed-c9c1-4e07-a170-063dd82dab4b" />

Query 9 helps management identify teams that are currently not involved in any tournaments, which may indicate inefficiencies in scheduling. Management can also reach out to inactive teams to encourage participation or figure out what barriers are preventing their involvement. Different teams participating could lead to more revenue as well, so teams that are inactive are missed opportunities. 


10. Query 10 finds tournaments whose total prize pool is greater than the average total prize pool across all tournaments.

Natural language question: Which tournaments have a total price pool that is greater than the average total prize pool across all tournaments?

<img width="600" height="728" alt="image" src="https://github.com/user-attachments/assets/86a56cdf-e043-4c70-9507-558da57a202a" />

Query 10 helps management identify high-value tournaments based on prize pool size relative to the overall average. This is important to strategic decision-making because it highlights tournaments that exceed average prize funding, indicating premium events. Management can use this information to determine which tournaments should be allocated more marketing, production quality, and operational resources. The average prize pool gives a benchmark to evaluate whether tournaments are underperforming or exceeding expectations. Higher prize pool tournaments are also more attractive to sponsors, making them ideal for premium sponsorship deals.

## Database Information
Name of the database: ns_Sp26_71552_Group7

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();

