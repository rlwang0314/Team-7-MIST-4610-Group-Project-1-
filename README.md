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

<img width="1097" height="766" alt="Screenshot 2026-04-03 at 11 24 01 PM" src="https://github.com/user-attachments/assets/901cd361-62d0-4603-98c2-e2a3dd77b146" />



## Data Dictionary 

<img width="530" height="528" alt="Screenshot 2026-04-03 at 10 48 23 PM" src="https://github.com/user-attachments/assets/f2c7b898-ad95-45d4-a3e4-ecd6d9243684" />

<img width="530" height="488" alt="Screenshot 2026-04-03 at 10 48 37 PM" src="https://github.com/user-attachments/assets/4e17a2be-1bd5-4087-af9b-9ba0bfad055d" />

<img width="530" height="340" alt="Screenshot 2026-04-03 at 10 48 57 PM" src="https://github.com/user-attachments/assets/79936937-6afe-40e7-8319-41d29dc408f3" />

<img width="530" height="390" alt="Screenshot 2026-04-03 at 10 49 13 PM" src="https://github.com/user-attachments/assets/06443c79-abda-401f-85f8-6895609c0b8d" />

<img width="524" height="448" alt="Screenshot 2026-04-03 at 10 49 30 PM" src="https://github.com/user-attachments/assets/8f11124f-ca74-4bba-9a3f-1b8e9d231f23" />

<img width="524" height="393" alt="Screenshot 2026-04-03 at 10 49 46 PM" src="https://github.com/user-attachments/assets/01be4556-00a7-4621-a224-862056d54cbf" />

<img width="524" height="326" alt="Screenshot 2026-04-03 at 10 49 59 PM" src="https://github.com/user-attachments/assets/846c2ae3-4f3b-4429-9782-2092f34fecd0" />

<img width="524" height="185" alt="Screenshot 2026-04-03 at 10 50 14 PM" src="https://github.com/user-attachments/assets/d5b3307c-1ac8-41fc-8379-37eac23fa940" />

<img width="524" height="343" alt="Screenshot 2026-04-03 at 10 50 28 PM" src="https://github.com/user-attachments/assets/7330fee8-70d2-408d-8b71-970e3250da5d" />

<img width="524" height="213" alt="Screenshot 2026-04-03 at 10 50 42 PM" src="https://github.com/user-attachments/assets/a5f90702-15bc-4357-adab-7f0becfc0498" />

<img width="524" height="320" alt="Screenshot 2026-04-03 at 10 50 57 PM" src="https://github.com/user-attachments/assets/1f802e53-995e-41f8-a7ca-7f3b3a7ffe1c" />

<img width="524" height="428" alt="Screenshot 2026-04-03 at 10 51 11 PM" src="https://github.com/user-attachments/assets/1aa85c39-4752-416a-ad6f-f929652931c3" />

<img width="524" height="297" alt="Screenshot 2026-04-03 at 10 51 26 PM" src="https://github.com/user-attachments/assets/9a21cf27-0ac4-47cc-85e6-cfa5642302b8" />

<img width="524" height="443" alt="Screenshot 2026-04-03 at 10 51 46 PM" src="https://github.com/user-attachments/assets/6e022da8-a257-4bf6-a974-1e89dbe25bdb" />


## Queries 

<img width="523" height="480" alt="Screenshot 2026-04-03 at 11 32 20 PM" src="https://github.com/user-attachments/assets/7bc3ea2c-ed46-4e21-a427-f143ff310fc4" />





Natural language question: “Which players are registered and what is their current registration status?”

<img width="1080" height="574" alt="image" src="https://github.com/user-attachments/assets/9333609d-4411-48a3-a1c2-fd487d202b11" />

Query 1 — This query allows the tournament management system to view all registered players alongside their current registration status. It retrieves a list of every player along with their registration status by joining together the Players and Registration table using the player_id. It merges the players personal information along with their registration records in which, if a player has more than one registration such as “Pending” or “Inactive”, it appears multiple times on the system. This information can be used to quickly identify who is actively participating, pending approval, or inactive across all tournaments. 




Natural language question: “Which teams have a sponsor and how much is their sponsorship worth?”

<img width="540" height="378" alt="Screenshot 2026-04-03 at 10 38 45 PM" src="https://github.com/user-attachments/assets/a41e5ad5-3c9f-4b6e-954f-6219556dcd64" />

Query 2 — This query allows the tournament management system to identify which teams have sponsorships and how much each sponsorship is worth. It retrieves information on the teams region, sponsor name, and sponsorship by joining the Teams and Sponsor table using sponsor_id. It includes teams that have matching sponsors and is organized in descending order by the sponsorship_amount. This information can be used to recognize high-value sponsorship relationships and prioritize partnerships that bring the most financial support to teams.





Natural Language Question: “What tournaments are upcoming and when and where are they being held?”

<img width="540" height="378" alt="Screenshot 2026-04-03 at 10 40 26 PM" src="https://github.com/user-attachments/assets/6e17c445-ce1d-491b-b971-f7a0939ce7af" />

Query 3 — This query allows the tournament management system to view all upcoming tournaments along with their scheduled dates and locations. It retrieves all the tournaments that are marked as “Upcoming” by filtering tournaments based on its status. The results are sorted by the start date in which the earliest events appear in the beginning. This information can be used to plan logistics, inform teams and players of upcoming events, and ensure all necessary preparations are made ahead of time.






Natural language question: “Which prize pool placements have a payout greater than 50000?”

<img width="540" height="378" alt="Screenshot 2026-04-03 at 10 41 21 PM" src="https://github.com/user-attachments/assets/6d6d521c-4a67-4651-87e5-1f22fc368477" />

Query 4 — This query allows the tournament management system to identify which prize pool placements offer payouts greater than 50000. This is done by filtering through the Prize_pools table and using the amount column. It shows the placement, amount, currency, and payout_status while sorting the results in descending order in which the highest amounts are displayed at the beginning. This information can be used to highlight high-value rewards to attract competitive teams and players to participate in tournaments.




   
Natural language question: “Who was the highest scoring player in each tournament?”

<img width="540" height="282" alt="Screenshot 2026-04-03 at 10 42 10 PM" src="https://github.com/user-attachments/assets/f9d04b40-f294-409f-a08c-83821a43514a" />

Query 5 — This query allows the tournament management system to identify the highest scoring player in each tournament. The players, scores, and tournament information is connected by joining the Players, Player_Stats, Matches, and Tournaments tables. In addition, a subquery is used in order to find the maximum score in each tournament and filters the results to include players whose score match the maximum. This information can be used to recognize standout performers, create MVP awards, and promote top players to grow the tournament's audience and reputation.





Natural language question: “Which tournaments have more than 5 players registered and how many players do they have?”

<img width="540" height="354" alt="Screenshot 2026-04-03 at 10 43 04 PM" src="https://github.com/user-attachments/assets/96eec58f-38b2-45e2-bbb9-0f15d0329456" />

Query 6 — This query allows the tournament management system to determine which tournaments have the most players enrolled. This information can be used to assess tournament popularity, allocate resources appropriately, and identify which tournaments may need additional support or infrastructure. High-participation tournaments require more resources such as more staff and larger venues. They can also be prioritized for marketing campaigns and sponsorships due to the amount of audience engagement. Comparing participation can also help identify underperforming events. Management can investigate and determine where the issues come from and find solutions to support them. 



Natural language question: “Which matches were won by a team whose sponsor contributes above the average sponsorship amount?”

<img width="540" height="354" alt="Screenshot 2026-04-03 at 10 44 06 PM" src="https://github.com/user-attachments/assets/ee99156a-7987-4909-80d4-1c29b76f841f" />

Query 7 — This query allows the tournament management system to identify matches that were won by teams whose sponsors contribute above the average sponsorship amount. This information can be used to analyze whether higher sponsored teams tend to perform better, which could inform future sponsorship strategies and investment decisions. If higher-funded teams consistently outperform others, it indicates that increased finances used to pay for coaching or equipment results in more success. This can influence how sponsors allocate funds and which teams they choose to support. 





Natural language question: “Which sponsors are funding more than 3 tournaments and whose total contribution exceeds the average total contribution across all sponsors?”

<img width="540" height="324" alt="Screenshot 2026-04-03 at 10 44 52 PM" src="https://github.com/user-attachments/assets/0f9ea0a9-9e3e-402e-a6b6-e1ecad6245b1" />

Query 8 — This query allows the tournament management system to identify which sponsors are funding multiple tournaments and contributing above the average total contribution across all sponsors. This information can be used to recognize the most committed sponsors and prioritize maintaining those relationships through exclusive benefits or partnership opportunities. It can also be used to plan for long-term finances. Sponsors with consistent above-average contributions can be considered essential partners for future tournaments, which reduces financial uncertainty. It helps managers determine sponsorship risk as well. If too much funding depends on a small number of sponsors, diversification may be needed to ensure there is enough funding for all tournaments. 




Natural language question: “Which players have scored above the overall average score in every single match they have played?”

<img width="540" height="166" alt="Screenshot 2026-04-03 at 10 45 34 PM" src="https://github.com/user-attachments/assets/8c35abb3-fdaa-49db-8ed8-53b3e1c69cb5" />

Query 9 — This query allows the tournament management system to identify players who have consistently performed above the overall average score in every match they have played. This information can be used to recognize elite players, create performance-based rankings, and identify candidates for invitational or high-tier tournaments. Management can use this for talent identification and player evaluation. Players who consistently outperform make them strong candidates for sponsorship deals or more exclusive tournaments. These players can also be featured in promotions and marketing campaigns to create more audience engagement and viewership. 




Natural language question: “What is each player’s performance level based on their score?”

<img width="540" height="357" alt="Screenshot 2026-04-03 at 10 46 13 PM" src="https://github.com/user-attachments/assets/29d01ce2-aa4d-406d-893d-74f8d143ea55" />

Query 10 — This query allows the tournament management system to categorize each player's performance as High, Medium, or Low based on their match scores. This information can be used to quickly assess the overall skill distribution across all players and identify those who may need development support or those ready to compete at a higher level.


## Database Information
Name of the database: ns_Sp26_71552_Group7

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();

