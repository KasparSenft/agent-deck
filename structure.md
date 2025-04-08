# Project Structure

```
agent-deck/    
├──  src/
│   ├── /games/                      
│   │   ├── base_game.py             # Abstract base class for all games
│   │   ├── tic_tac_toe.py           # Example game implementation
│   │   ├── chess.py                 # Another game implementation
│   │   └── game_logger.py           # Logs game events (actions, states, outcomes)
│   │
│   ├── /agent/                      
│   │   ├── base_agent.py            # Abstract Base Class for common agent methods
│   │   ├── llm_agent.py             # LLM-powered agent implementation
│   │   ├── strategy.py              # Handles long-term strategy and updates
│   │   ├── tactics.py               # Short-term tactical memory and reasoning
│   │   ├── memory.py                # Tracks past game states
│   │   ├── reasoning.py             # LLM-based reasoning module (Chain-of-Thought)
│   │   ├── formatter.py             # Formats inputs into structured prompts for the LLM
│   │   ├── agent_logger.py          # Logs agent's reasoning, actions, strategies, and tactics
│   │
│   ├── /game_engine/                
│   │   ├── game_state.py            # Tracks and updates the game state
│   │   ├── action_schema.py         # Defines valid action formats for the game
│   │   ├── validator.py             # Validates action legality based on rules
│   │   ├── executor.py              # Applies validated actions to the game state
│   │   ├── referee.py               # Generates summaries of game events in natural language
│   │
│   ├── /interfaces/                 
│   │   ├── game_interface.py        # Defines interaction API between the game and agent
│   │   ├── llm_interface.py         # Wraps LLM calls and API communication
│   │
│   ├── /utils/                      
│   │   ├── logger.py                # Custom logging utilities for research and debugging
│   │   └── config.py                # Handles configurations and settings for the system
│   │
│   ├── /logs/                       
│   │   ├── /game_logs/              # Stores logs specific to each game session
│   │   └── /agent_logs/             # Stores logs of the agent's reasoning and actions
│   │
│   └── /tests/                      
│       ├── test_game_logic.py       # Unit tests for game engine logic
│       ├── test_agent_behavior.py   # Unit tests for agent's reasoning and actions
│       └── test_logging.py          # Tests for the logging system
│
├── main.py                      # Main game loop and execution entry point
├── requirements.txt             # Python dependencies
└── README.md                    # Project overview, setup instructions, and usage  

```