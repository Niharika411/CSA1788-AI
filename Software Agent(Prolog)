% Define software agent properties
agent(Name, Purpose, Capabilities).

% Sample software agent
agent("Agent1", "Data Processing", ["Data Collection", "Data Analysis", "Data Visualization"]).

% Rule to list all software agents
list_agents :-
  agent(Name, Purpose, Capabilities),
  write("Name: "), write(Name), nl,
  write("Purpose: "), write(Purpose), nl,
  write("Capabilities: "), write(Capabilities), nl,
  nl,
  fail.
