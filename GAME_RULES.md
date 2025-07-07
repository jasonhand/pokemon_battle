# 📋 Detailed Game Rules & Mechanics

## 🎯 Game Structure

### **Game Session**
- **Duration**: 8 rounds per game
- **Players**: 1 human player + 2 AI opponents
- **Time per Round**: 30 seconds decision time
- **Objective**: Achieve the highest total score

### **Round Structure**
1. **Card Distribution**: All players receive random Pokémon cards
2. **Decision Phase**: 30-second timer to choose action
3. **AI Decision**: Opponents make their choices
4. **Resolution**: Scores are calculated and displayed
5. **Transition**: 3-second pause before next round

## 🎴 Pokémon Card System

### **Card Properties**
Each Pokémon card contains:
- **Name**: Pokémon species name
- **Emoji**: Visual representation
- **Types**: 1-2 elemental types (Fire, Water, Electric, etc.)
- **Base Points**: 10-106 points (with ±10% random variance)
- **Color Theme**: Type-appropriate gradient background

### **Pokémon Database**
The game includes 50+ Pokémon from the original series:
- **Legendary**: Mewtwo, Mew, Articuno, Zapdos, Moltres
- **Starter Evolution**: Charizard, Blastoise, Venusaur
- **Popular**: Pikachu, Gengar, Dragonite, Snorlax
- **And many more** with balanced point distributions

### **Type System**
Pokémon types affect visual styling but not gameplay mechanics:
- **Fire**: Red/orange themes
- **Water**: Blue themes  
- **Electric**: Yellow themes
- **Grass**: Green themes
- **Psychic**: Pink themes
- **And 13 other types** with unique color schemes

## ⚔️ Decision Mechanics

### **Player Actions**
Each round, you must choose one of two actions:

#### **🤝 Cooperate**
- **Description**: Work together with other players
- **Strategy**: Build trust and mutual benefit
- **Risk**: Vulnerable to betrayal

#### **⚔️ Defect** 
- **Description**: Betray other players for personal gain
- **Strategy**: Exploit cooperative opponents
- **Risk**: Penalties when everyone defects

### **AI Decision Logic**

#### **Trusty AI (70% base cooperation)**
- **Adaptive Behavior**: Cooperation rate increases based on player's cooperation history
- **Formula**: `0.7 + (player_cooperation_rate * 0.2)`
- **Personality**: Trust-building, relationship-focused
- **Thought Process**: "Trust builds stronger bonds!"

#### **Risky AI (40% base cooperation)**
- **Progressive Risk**: Gets riskier as game progresses
- **Formula**: `0.4 - (current_round / 20)`
- **Personality**: Calculated risk-taker, opportunistic
- **Thought Process**: "Fortune favors the bold!"

## 🏆 Scoring System

### **Cooperation Matrix**

The scoring system is based on the number of players who cooperate in each round:

| Cooperators | Defectors | Result | Points Formula |
|-------------|-----------|---------|----------------|
| 3 | 0 | **Perfect Cooperation** | Base Points × 1.5 (+50%) |
| 2 | 1 | **Mixed Strategy** | Cooperators: Base Points<br>Defectors: Base Points × 1.25 (+25%) |
| 1 | 2 | **Mixed Strategy** | Cooperators: Base Points<br>Defectors: Base Points × 1.25 (+25%) |
| 0 | 3 | **Total Defection** | Base Points × 0.75 (-25%) |

### **Score Calculation Example**

**Scenario**: All players have 100-point Pokémon

**Round 1**: All Cooperate
- Everyone gets: 100 × 1.5 = **150 points**

**Round 2**: 2 Cooperate, 1 Defects  
- Cooperators get: 100 points each
- Defector gets: 100 × 1.25 = **125 points**

**Round 3**: All Defect
- Everyone gets: 100 × 0.75 = **75 points**

### **Cumulative Scoring**
- Scores accumulate across all 8 rounds
- No negative scores (minimum 0)
- Final ranking determines winner

## 🎮 Strategic Considerations

### **Short-term vs. Long-term Strategy**

#### **Immediate Benefits**
- **Defection**: +25% bonus in mixed scenarios
- **Cooperation**: Base points, but enables team bonuses

#### **Long-term Consequences**
- **Defection**: May trigger retaliation from AI
- **Cooperation**: Builds trust for future rounds

### **AI Adaptation Patterns**

#### **Trusty AI Learning**
- **Cooperation History**: Tracks your cooperation rate
- **Adaptation**: Becomes more cooperative if you cooperate
- **Strategy**: Builds mutual trust over time

#### **Risky AI Progression**
- **Risk Escalation**: Gets riskier each round
- **Timing**: Early rounds safer, later rounds more aggressive
- **Strategy**: Exploits predictable patterns

### **Optimal Strategies by Game Phase**

#### **Early Game (Rounds 1-3)**
- **Recommended**: Establish cooperation patterns
- **Reasoning**: Build trust with Trusty AI
- **Risk**: Risky AI is still relatively safe

#### **Mid Game (Rounds 4-6)**
- **Recommended**: Adapt based on opponent behavior
- **Reasoning**: AI patterns become clearer
- **Strategy**: Exploit predictable opponents

#### **Late Game (Rounds 7-8)**
- **Recommended**: Aggressive defection if leading
- **Reasoning**: Risky AI becomes very aggressive
- **Strategy**: Secure victory or catch up

## 🎯 Advanced Tactics

### **Pattern Recognition**
- **Trusty AI**: Look for cooperation trends
- **Risky AI**: Notice increasing aggression
- **Your History**: Consider how your past actions affect AI behavior

### **Risk Assessment**
- **High-Risk Scenarios**: When both AI might defect
- **Safe Scenarios**: When Trusty AI is likely to cooperate
- **Mixed Scenarios**: Calculate expected value of each choice

### **Psychological Warfare**
- **Trust Building**: Consistent cooperation with Trusty AI
- **Bluffing**: Occasional defection to keep opponents guessing
- **Retaliation**: Defect if consistently betrayed

## 🏅 Victory Conditions

### **Final Ranking**
1. **Winner**: Highest total score after 8 rounds
2. **Runner-up**: Second highest score
3. **Third Place**: Lowest score

### **Tie-Breaking**
- **Cooperation Rate**: Higher cooperation rate wins ties
- **Final Round Performance**: Better final round performance wins
- **Random**: Coin flip for identical performances

## 🎨 User Interface Features

### **Visual Feedback**
- **Progress Bar**: Shows game advancement
- **Timer**: 30-second countdown per round
- **Score Animations**: Visual score updates
- **Card Reveals**: Smooth Pokémon card animations

### **Information Display**
- **Round Results**: Detailed breakdown of decisions
- **Score History**: Running totals for all players
- **AI Thoughts**: Simulated AI decision-making process
- **Final Results**: Complete game summary

### **Accessibility**
- **Responsive Design**: Works on all screen sizes
- **Color Coding**: Visual distinction between actions
- **Clear Typography**: Easy-to-read text and numbers
- **Intuitive Controls**: Simple button-based interface

## 🔧 Technical Implementation

### **Game Engine**
- **Pure JavaScript**: No external dependencies
- **Object-Oriented Design**: Clean, maintainable code
- **Event-Driven**: Responsive user interactions
- **State Management**: Tracks game progress and history

### **Data Management**
- **Local Storage**: No server requirements
- **Pokémon Database**: 50+ entries with balanced stats
- **Game History**: Tracks all decisions and outcomes
- **Score Calculation**: Real-time point computation

### **Performance**
- **Fast Loading**: Minimal resource requirements
- **Smooth Animations**: 60fps visual effects
- **Responsive UI**: Immediate user feedback
- **Cross-Platform**: Works on all modern browsers

---

*This document provides comprehensive information for players who want to master the strategic depth of the Pokémon Game Theory Battle Arena! 🎮* 