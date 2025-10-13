# 🎮 GitHub Copilot Game Type-Along Session

**Build a Snake Game in 20 Minutes with GitHub Copilot**

A hands-on workshop for experienced developers new to GitHub Copilot. Learn to leverage Inline Suggestions, Chat, Edits, and Agent modes while building a fully functional game.

---

## 📋 Session Overview

**Duration:** 20 minutes  
**Audience:** Experienced developers new to GitHub Copilot  
**Goal:** Demonstrate Copilot's capabilities through practical game development  
**Tech Stack:** Vanilla JavaScript, HTML5 Canvas, CSS

### What You'll Learn
- ✅ **Inline Suggestions** - Fast code completion and pattern recognition
- ✅ **Copilot Chat** - Conversational coding assistance
- ✅ **Copilot Edits** - Multi-location refactoring
- ✅ **Copilot Agent** - Complex multi-file operations

---

## 🚀 Prerequisites

### Required
- GitHub Copilot subscription (Individual, Business, or Enterprise)
- VS Code with GitHub Copilot extension installed
- Basic knowledge of JavaScript and web development

### Setup Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/ykhadas/copilot-game-typealong.git
   cd copilot-game-typealong
   ```

2. Open in VS Code:
   ```bash
   code .
   ```

3. Verify Copilot is active (check status bar)

4. Open `game.js` and you're ready to start!

---

## ⏱️ 20-Minute Session Guide

### Minutes 0-2: Introduction
**What to cover:**
- "You know how to code—let's see how Copilot accelerates your workflow"
- Quick overview of 4 Copilot modes
- Set expectation: "Copilot is pair programming, not autopilot"

**Show:**
- Copilot icon in status bar
- Chat panel (Ctrl/Cmd + I)
- Edits mode vs Chat vs Inline

---

### Minutes 2-7: Core Game with Inline Suggestions

**Objective:** Build basic Snake game using comment-driven development

**🎯 Scenario 1: Game Setup**
```javascript
// Create a snake game with canvas 400x400
// Grid size 20x20, snake starts in center
// Snake moves with arrow keys
```

**Teaching Points:**
- Type the comment, pause, watch Copilot suggest entire function
- Press Tab to accept, or Ctrl+Enter for alternatives
- Point out: "Notice it understood canvas context, grid math, and game state"

**🎯 Scenario 2: Game State**
```javascript
// Game state object with snake position, direction, food, and score
```

**🎯 Scenario 3: Movement**
```javascript
// Update snake position based on current direction
// Add new head position, remove tail unless eating food
```

**Expected Result:** Working snake that moves and eats food

---

### Minutes 7-12: Features with Copilot Chat

**Objective:** Add features conversationally

**🎯 Scenario 1: Collision Detection**
Open Copilot Chat (Ctrl/Cmd + I):
```
Add collision detection for walls and self-collision. Show game over screen when collision occurs.
```

**Teaching Points:**
- Chat understands your existing code context
- Can insert code directly at cursor
- Explains what it's doing

**🎯 Scenario 2: Progressive Difficulty**
In Chat:
```
Increase game speed by 10% every time score reaches a multiple of 5
```

**🎯 Scenario 3: Use Slash Commands**
Select a complex function, then in Chat:
```
/explain how does this collision detection work?
```

Try other commands:
```
/doc add JSDoc comments to the game loop function
/tests create unit tests for collision detection
```

**Expected Result:** Feature-complete game with difficulty progression

---

### Minutes 12-17: Refactoring with Copilot Edits

**Objective:** Show multi-location changes with Edits mode

**🎯 Scenario 1: Convert to Class**
1. Open Copilot Edits (Ctrl/Cmd + Shift + I)
2. Add `game.js` to working set
3. Enter prompt:
```
Refactor this game into a SnakeGame class with proper encapsulation. Use constructor for initialization, and separate methods for update, render, and input handling.
```

**Teaching Points:**
- Edits mode changes multiple locations simultaneously
- Shows diff preview before applying
- Can work across multiple files in working set

**🎯 Scenario 2: Add Type Safety**
In Edits mode:
```
Add JSDoc type annotations throughout the code for better IDE support. Define types for GameState, Position, and Direction.
```

**🎯 Scenario 3: Error Handling**
```
Add comprehensive error handling for canvas operations and edge cases
```

**Expected Result:** Clean, well-structured class-based code

---

### Minutes 17-19: Advanced with Copilot Agent

**Objective:** Complex multi-file operations

**🎯 Scenario 1: Add Sound System**
Open Copilot Agent, describe the problem:
```
Add a sound system to the game:
- Create a new sounds.js file with a SoundManager class
- Add sound effects for eating food, game over, and movement
- Use Web Audio API
- Update index.html to include the new file
- Integrate sounds into game.js
```

**Teaching Points:**
- Agent mode handles multi-file creation and coordination
- Understands architecture and file relationships
- Can scaffold entire features

**🎯 Scenario 2: Configuration System** (if time permits)
```
Extract all game configuration (grid size, colors, speeds) into a separate config.js file. Update game.js to use this config.
```

**Expected Result:** Multi-file feature implementation

---

### Minutes 19-20: Wrap Up & Q&A

**Key Takeaways:**
1. **Inline Suggestions:** Best for autocomplete and known patterns
2. **Chat:** Best for questions, explanations, single features
3. **Edits:** Best for refactoring and multi-location changes
4. **Agent:** Best for multi-file features and architecture

**Next Steps:**
- Try the challenges in `exercises/CHALLENGES.md`
- Explore completed examples in `completed/`
- Read detailed scenarios in `SCENARIOS.md`

---

## 📁 Repository Structure

```
copilot-game-typealong/
├── README.md                    # This file - session guide
├── SCENARIOS.md                 # Detailed Copilot scenarios
├── FACILITATOR_GUIDE.md         # Tips for instructors
├── index.html                   # HTML boilerplate
├── style.css                    # Game styling
├── game.js                      # Starter file (minimal setup)
├── completed/
│   ├── game-final.js           # Reference implementation
│   └── game-enhanced.js        # Advanced features version
├── exercises/
│   └── CHALLENGES.md           # Practice exercises
└── .gitignore
```

---

## 🎯 Quick Reference: When to Use Each Mode

| Mode | Best For | Example |
|------|----------|---------|
| **Inline Suggestions** | Auto-completion, predictable patterns | Loop structures, common functions |
| **Chat** | Questions, single features, explanations | "How do I optimize this?", "Add error handling" |
| **Edits** | Refactoring, multi-location changes | Converting to classes, adding types |
| **Agent** | Multi-file features, architecture | "Add authentication system", "Create API layer" |

---

## 🔥 Pro Tips for Experienced Devs

1. **Context is King:** Meaningful variable/function names = better suggestions
2. **Comment First:** Write what you want in comments, let Copilot implement
3. **Review Everything:** Don't blindly accept—Copilot makes mistakes
4. **Use @ References:** In Chat/Edits, use `@workspace`, `#file`, `#selection`
5. **Iterate:** If first suggestion isn't perfect, ask for refinement
6. **Learn Patterns:** Notice what prompts work well, build your library

---

## 📚 Additional Resources

- [GitHub Copilot Documentation](https://docs.github.com/copilot)
- [Best Practices Guide](https://docs.github.com/copilot/using-github-copilot/best-practices)
- [Copilot CLI](https://docs.github.com/copilot/github-copilot-in-the-cli)
- [VS Code Copilot Extension](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)

---

## 🤝 Contributing

Found a better way to demonstrate Copilot? Have suggestions? PRs welcome!

---

## 📄 License

MIT License - feel free to use this for your own training sessions!

---

**Ready to start?** Open `game.js` and let's build! 🚀

For detailed step-by-step scenarios, see [SCENARIOS.md](SCENARIOS.md)  
For facilitator tips, see [FACILITATOR_GUIDE.md](FACILITATOR_GUIDE.md)