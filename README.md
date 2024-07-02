# Cricket Score Tracking System - Low Level Design

This project implements a simple cricket score tracking system using Java. It simulates a cricket match between two teams and tracks their scores, overs, wickets, and other statistics.

## Implementation Overview

The implementation consists of two main classes: `Main` and `ScoreCard`.

### Sample input:

```
Please Enter TotalNo of Players in each Team:
5
Please Enter totalNo of Overs in match:
2
Team1: 
over1: 1,1,1,1,1,2
over2: W,4,4,Wd,W,1,6
Team2: 
over1: 4,6,W,W,1,1
over2: 6,1,W,W

Team1 won by 1 wicket & 4 runs!
```

### Main Class

The `Main` class initializes the game by taking user input for the number of players per team and the total number of overs in the match. It then creates instances of the `ScoreCard` class for both Team 1 and Team 2 and manages the match flow by taking input for each ball/over and updating the scorecards accordingly.

### ScoreCard Class

The `ScoreCard` class represents the scorecard for each team. It maintains arrays to store individual player statistics (runs scored, 4s, 6s, balls faced) and overall team statistics (total runs, wickets, wides, overs remaining). It also manages player line-up and handles the logic for updating scores based on input balls.

## Features

- **Dynamic Input**: Allows input for each ball/over to update scores and statistics in real-time.
- **Score Calculation**: Calculates individual player scores, boundaries (4s and 6s), and maintains cumulative team scores.
- **Match Result**: Determines the match result based on total runs scored and wickets fallen.

## How to Run

To run the application:
1. Compile the Java files (`Main.java` and `ScoreCard.java`).
2. Execute the compiled `Main` class.
3. Follow the prompts to input the number of players, overs, and individual ball/over updates.

## Example Usage

Here's a brief example of how to use the application:

```java
// Sample usage in Main.java
public static void main(String[] args) {
    Scanner sc=new Scanner(System.in);
    System.out.println("Please Enter TotalNo of Players in each Team:");
    int totalPlayers=Integer.parseInt(sc.next());
    System.out.println("Please Enter totalNo of Overs in match:");
    int totalOvers=Integer.parseInt(sc.next());
    ScoreCard.initialize(totalOvers,totalPlayers);
    ScoreCard team1 = new ScoreCard(1);
    ScoreCard team2 = new ScoreCard(2);
    
    // Simulate batting for both teams
    // Code continues as per the logic in the provided Main class
}
