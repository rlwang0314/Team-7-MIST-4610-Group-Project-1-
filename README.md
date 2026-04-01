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


## Queries 

