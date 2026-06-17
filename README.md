# Soccer Attrition Model - Fatigue Simulation

A tactical simulation that models physical attrition in soccer, showing how specific passing patterns and defensive tactics can force opponents to expend energy while conserving your own.

## Features

### Attacking Patterns (12 strategies)
- Normal Play
- Target CB / FB / DM
- Switch of Play
- Double Switch
- Wing Overload
- Overload + Switch
- Through Balls
- Vertical Stretch
- Midfield Trap
- Press Bait

### Pass Mechanics
- **6 Pass Types**: Ground, Driven, Lobbed, Through, Long Ball, Curved
- **4 First Touch Options**: Forward, Backward, Lateral, Dummy
- **Pass Success Probability** based on distance, pressure, and fatigue
- **Curved Passes** with bezier trajectory (harder to execute)

### Defensive Tactics
- **Offside Trap**: Step up together to catch attackers offside
- **Rest Defense**: Maintain shape while defending
- **Drop Deep**: Nullify through balls
- **Force Wide**: Push attackers away from goal
- **Double Up**: Two defenders on dangerous runner
- **Block Lanes**: Position in passing lanes
- **Bait Run**: Show space then close it

### Game Events
- **Goal Scoring**: Close-range shots with probability model
- **Throw-ins**: Ball out of bounds triggers reset
- **Corner Kicks**: Attackers push forward, defenders pack the box
- **Goal Kicks**: Goalkeeper restarts
- **Possession Switching**: Automatic role change on interception

### Team Shape
- **Dynamic Formation**: Players maintain relational spacing
- **Shape Pull**: Players pulled toward home positions
- **Spacing Enforcement**: Minimum distance between teammates
- **Ball-relative Shift**: Formation shifts with ball position

### Analytics Dashboard
- **Expected Goals (xG)**: Probability model based on distance, angle, fatigue
- **Pass Maps**: Visual arrows showing pass patterns (last 50 passes)
- **Distance Tracking**: Total distance per player
- **Sprint Breakdown**: Sprint vs jog vs walk distance per player
- **Shot Statistics**: Shots, shots on target, corners, throw-ins
- **Possession Percentage**: Time-based possession tracking

### Fatigue Model
- Individual player fatigue tracking
- Sprint count and distance
- Wall warning at 80%+ fatigue
- Stamina bars above each player
- Substitution model (5 subs, 20% fatigue on entry)

### Visual Features
- **Ball Holder Highlight**: Pulsing yellow ring on player with ball
- **Pass Map Overlay**: Faded arrows showing pass patterns
- **Game State Overlay**: Shows goals, throw-ins, corners, goal kicks
- **Dynamic Offside Line**: Adjusts based on ball position
- Real-time pass visualization
- Dummies shown as blue dashed lines
- Offside line indicator
- Rest defense shape indicator
- Color-coded stamina bars
- Score display (goalsA - goalsB)

## How to Use

1. Open `index.html` in a browser
2. Select an attack pattern
3. Use speed controls (1x, 3x, 10x) or Pause
4. Watch fatigue build up on targeted players
5. Use Substitution buttons when players hit 60%+ fatigue

## Key Insights

- **Double Switch** forces entire defense to sprint 24x more than attackers
- Defenders hit WALL by 30th minute with aggressive targeting
- Substitutions only recover 17% of fatigue damage
- Offside trap saves 1.3 fatigue per sequence vs chasing
- Rest defense costs only 0.1 fatigue vs 1.5 for sprinting

## Tactical Recommendations

### First Half (0-45 min)
1. Double Switch or Overload + Switch
2. Force opponent to use 2-3 subs
3. Target fullbacks and defensive midfielders

### Second Half (45-90 min)
1. Vertical Stretch or Through Balls
2. Exploit tired center-backs
3. Use Press Bait to waste remaining energy

## License

MIT
