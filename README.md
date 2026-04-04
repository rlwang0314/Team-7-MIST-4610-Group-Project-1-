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


1. Query 1

Natural language question: “Which players are registered and what is their current registration status?”

<img width="1080" height="574" alt="image" src="https://github.com/user-attachments/assets/9333609d-4411-48a3-a1c2-fd487d202b11" />

Query 1 — This query allows the tournament management system to view all registered players alongside their current registration status. This information can be used to quickly identify who is actively participating, pending approval, or inactive across all tournaments.



2. Query 2 shows sponsor names, the tournament they sponsor, and the donation amount for deals greater than $50,000.

Natural language question: “Which teams have a sponsor and how much is their sponsorship worth?”

<img width="540" height="378" alt="Screenshot 2026-04-03 at 10 38 45 PM" src="https://github.com/user-attachments/assets/a41e5ad5-3c9f-4b6e-954f-6219556dcd64" />

Query 2 — This query allows the tournament management system to identify which teams have sponsorships and how much each sponsorship is worth. This information can be used to recognize high-value sponsorship relationships and prioritize partnerships that bring the most financial support to teams.



3. Query 3 shows all teams competing in NBA 2K Invitational.

Natural Language Question: “What tournaments are upcoming and when and where are they being held?”

<img width="540" height="378" alt="Screenshot 2026-04-03 at 10 40 26 PM" src="https://github.com/user-attachments/assets/6e17c445-ce1d-491b-b971-f7a0939ce7af" />

Query 3 — This query allows the tournament management system to view all upcoming tournaments along with their scheduled dates and locations. This information can be used to plan logistics, inform teams and players of upcoming events, and ensure all necessary preparations are made ahead of time.




4. Query 4 gives an overview of all matches in a tournament. 

Natural language question: “Which prize pool placements have a payout greater than 50000?”

<img width="540" height="378" alt="Screenshot 2026-04-03 at 10 41 21 PM" src="https://github.com/user-attachments/assets/6d6d521c-4a67-4651-87e5-1f22fc368477" />

Query 4 — This query allows the tournament management system to identify which prize pool placements offer payouts greater than 50000. This information can be used to highlight high-value rewards to attract competitive teams and players to participate in tournaments.




5. Query 5 finds tournaments with more than three teams.
   
Natural language question: “Who was the highest scoring player in each tournament?”

<img width="540" height="282" alt="Screenshot 2026-04-03 at 10 42 10 PM" src="https://github.com/user-attachments/assets/f9d04b40-f294-409f-a08c-83821a43514a" />

Query 5 — This query allows the tournament management system to identify the highest scoring player in each tournament. This information can be used to recognize standout performers, create MVP awards, and promote top players to grow the tournament's audience and reputation.




6.  Query 6 shows tournaments that have more than one sponsor. 

Natural language question: “Which tournaments have more than 5 players registered and how many players do they have?”

<img width="540" height="354" alt="Screenshot 2026-04-03 at 10 43 04 PM" src="https://github.com/user-attachments/assets/96eec58f-38b2-45e2-bbb9-0f15d0329456" />

Query 6 — This query allows the tournament management system to determine which tournaments have the most players enrolled. This information can be used to assess tournament popularity, allocate resources appropriately, and identify which tournaments may need additional support or infrastructure.




7. Query 7 shows sponsors whose sponsorship amount is greater than the average sponsorship amount.

Natural language question: “Which matches were won by a team whose sponsor contributes above the average sponsorship amount?”

<img width="540" height="354" alt="Screenshot 2026-04-03 at 10 44 06 PM" src="https://github.com/user-attachments/assets/ee99156a-7987-4909-80d4-1c29b76f841f" />

Query 7 — This query allows the tournament management system to identify matches that were won by teams whose sponsors contribute above the average sponsorship amount. This information can be used to analyze whether higher sponsored teams tend to perform better, which could inform future sponsorship strategies and investment decisions.




8. Query 8 finds the total prize money by game genre, but only for genres whose name starts with “R” or “N”.

Natural language question: “Which sponsors are funding more than 3 tournaments and whose total contribution exceeds the average total contribution across all sponsors?”

<img width="540" height="324" alt="Screenshot 2026-04-03 at 10 44 52 PM" src="https://github.com/user-attachments/assets/0f9ea0a9-9e3e-402e-a6b6-e1ecad6245b1" />

Query 8 — This query allows the tournament management system to identify which sponsors are funding multiple tournaments and contributing above the average total contribution across all sponsors. This information can be used to recognize the most committed sponsors and prioritize maintaining those relationships through exclusive benefits or partnership opportunities.




9. Query 9 finds teams that have never participated in any tournament.

Natural language question: “Which players have scored above the overall average score in every single match they have played?”

<img width="540" height="166" alt="Screenshot 2026-04-03 at 10 45 34 PM" src="https://github.com/user-attachments/assets/8c35abb3-fdaa-49db-8ed8-53b3e1c69cb5" />

Query 9 — This query allows the tournament management system to identify players who have consistently performed above the overall average score in every match they have played. This information can be used to recognize elite players, create performance-based rankings, and identify candidates for invitational or high-tier tournaments.




10. Query 10 finds tournaments whose total prize pool is greater than the average total prize pool across all tournaments.

Natural language question: “What is each player’s performance level based on their score?”

<img width="540" height="357" alt="Screenshot 2026-04-03 at 10 46 13 PM" src="https://github.com/user-attachments/assets/29d01ce2-aa4d-406d-893d-74f8d143ea55" />

Query 10 — This query allows the tournament management system to categorize each player's performance as High, Medium, or Low based on their match scores. This information can be used to quickly assess the overall skill distribution across all players and identify those who may need development support or those ready to compete at a higher level.


## Database Information
Name of the database: ns_Sp26_71552_Group7

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();

