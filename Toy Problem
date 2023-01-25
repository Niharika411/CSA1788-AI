import itertools
def find_matches_fraction(max_players):
  team_a = range(1,max_players)
  team_b = range(1,max_players)
  team_c = range(1,max_players)
 
  matched_team = []
  for players in list(itertools.product(team_a,team_b,team_c)):
       largest_team = max(players)
       l_combinations = list(players)
       l_combinations.pop(l_combinations.index(max(l_combinations)))
       remaining_players = sum(l_combinations)
       if remaining_players == largest_team:
           matched_team.append(1)
       else:
           matched_team.append(0)
         
  fraction_success = sum(matched_team) / len(matched_team)
  return(fraction_success)
answer_express = find_matches_fraction(6)
print(answer_express)
