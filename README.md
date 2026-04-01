# Team 7 MIST 4610 Group Project 1

## Team Name: 
Sp26_71552_Group 7

## Team Members:
1. Nandini Chinthapanti
2. Sara Gebreyohannes [@saragebree](https://github.com/saragebree)
3. Rajan Malik
4. Landon Tabor
5. Reina Wang [@rlwang0314](https://github.com/rlwang0314)

## Problem Description

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





## Queries 

