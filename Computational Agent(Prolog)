% Define the agent's actions
action(move_up).
action(move_down).
action(move_left).
action(move_right).

% Define the agent's rules for choosing actions
choose_action(Agent, Action) :-
    current_position(Agent, X, Y),
    (goal_reached(X, Y) -> Action = stop;
    (obstacle_ahead(Agent) -> choose_alternate_action(Agent, Action);
    Action = move_towards_goal(Agent))).

% Define the alternate actions for when there is an obstacle
choose_alternate_action(Agent, Action) :-
    (clear_path(Agent, move_left) -> Action = move_left;
    (clear_path(Agent, move_right) -> Action = move_right;
    (clear_path(Agent, move_up) -> Action = move_up;
    (clear_path(Agent, move_down) -> Action = move_down;
    Action = stop)))).

% Define the action to move towards the goal
move_towards_goal(Agent) :-
    current_position(Agent, X, Y),
    goal(GX, GY),
    (GX > X -> move_right;
    (GX < X -> move_left;
    (GY > Y -> move_up;
    move_down)))).
