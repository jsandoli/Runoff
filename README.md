# Runoff
(Harvard CS50 project) Runoff algorithm to fairly determine the winner of an election based on ranked votings.
*Code's structure provided by the course, functions built by me as an assignment.

How does the algorithm work?

The whole code revolves around the struct "candidate", which stores string name, int votes, and the bool eliminated, to account for the candidates in this runoff election.

MAIN Function:
  Receiving inputs via command line with "argv", the main function assures that these inputs will be transferred to the array candidates, of type "candidate". Then, the program will prompt the user for numver of voters in this election, and then query each vote for each voter, divided by ranks, all of which is done through for loops.
  Then, the runoff section begins, where they are held until a winner is declared.

My Implementation:

As the core code in the main function were previously provided by CS50's staff, I was tasked with the development of the other functions in the program.

bool vote(int voter, int rank, string name):
  This function is responsible for verifying the authenticity of votes, via the functrion strcmp, matching the name typed in the current vote with the array of candidates. If everything goes right, the number of votes will be updated.

  void tabulate(void):
    Tabulates votes for non eliminated cnadidates, veryfing through the bool "eliminated" cointained in the struct candidate.

  bool print_winner(void):
    When called, this function is responsible for finding the winner, if there is one, again through a for loop iterating through all the candidates and checking votes.

  int find_min(void):
    Returns the minimum number of votes any remaining candidate has.
    
  bool is_tie(int min):
    Returns true if the election is tied between all candidates.

  void eliminate(int min):
    Eliminates teh candidate (or candidates) in the last place.
  
    
    

  

