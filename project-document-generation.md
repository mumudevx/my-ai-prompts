# Prompt
```
I want to make a flip card memory game. Here are some features of the game:

- There will be a menu at the game opening, for now there will be a start game button.
- When the game starts, all cards will be open for 5 seconds. Then all cards will be closed.
- The player will be given 60 seconds to match the cards.
- If the player can match the cards in 60 seconds, you will win a screen.
- If the player can match the cards in 60 seconds, you will lose a screen.
- There will be two discount code lists (string lists). One is for the winners to download and select their coupons, the other is for the losers.
- Create the coolest card design possible.
- Read a variable for the back of the card, use this as card-back-image.
- Create an image list (string list) for the fronts of the card. If there are 4 images in this list, you will generate 8 cards from 4x2. The images of the fronts of the cards will be drawn from this list.

Considering all the features above, can you produce the following for me?

- Project requirement document
- Details within and outside the scope of the project.
- Project planning document
```

# Output Example

# Flip Card Memory Game - Project Requirements Document

## 1. Project Overview
The Flip Card Memory Game is a web-based game where players match pairs of flipped cards within a time limit. The game includes a reward system that provides discount codes based on the player's success.

## 2. Functional Requirements
### 2.1 Game Flow
- The game starts with a menu screen displaying a **Start Game** button.
- Upon clicking **Start Game**, all cards are revealed for **5 seconds**.
- After 5 seconds, all cards are flipped back.
- The player is given **60 seconds** to match all cards.
- If the player successfully matches all pairs within 60 seconds, they win.
- If the player fails to match all pairs in 60 seconds, they lose.

### 2.2 Game Mechanics
- The game board consists of **pairs of cards** with random placements.
- The number of cards depends on the image list: for **N images, there will be 2N cards**.
- Clicking on two cards reveals them; if they match, they remain open, otherwise, they flip back.
- A countdown timer is displayed.
- The game ends when all pairs are matched or the timer reaches zero.

### 2.3 Reward System
- Two lists of discount codes will be maintained:
  - One for winners.
  - One for losers.
- After the game ends, users receive a screen to claim their respective discount codes.

### 2.4 Visuals & UI/UX
- The **card-back** design is customizable and taken from a predefined variable.
- The **card-front** images come from a predefined list.
- The design should be aesthetically pleasing with animations for flipping effects.

## 3. Non-Functional Requirements
- The game should be responsive and playable on both desktop and mobile.
- It should have smooth animations and an engaging user experience.
- Game state should be maintained during a session but resets after completion.

---

# Scope of the Project

## 1. In-Scope
- **Game UI Development** (Menu, Game Board, Win/Lose Screens)
- **Game Mechanics** (Flipping logic, matching logic, time constraints)
- **Basic Reward System** (Static list of discount codes for winners/losers)
- **Dynamic Card Generation** (Based on image list input)
- **Customizable Card-Back Image**

## 2. Out-of-Scope (For Now)
- **Multiplayer Mode**
- **Saving User Progress / Leaderboards**
- **User Authentication & Profile Management**
- **Discount Code Management System** (Only static lists will be used)
- **Advanced Animations & Special Effects** (Beyond basic flipping effects)

---

# Project Planning Document

## 1. Milestones & Timeline
### Phase 1: Planning & Design (Week 1)
- Define UI components and overall aesthetics.
- Plan the game logic structure.
- Finalize technology stack.

### Phase 2: Core Development (Week 2-3)
- Implement menu and start-game transition.
- Develop card flipping and matching logic.
- Integrate timer and win/lose conditions.
- Implement reward system logic.

### Phase 3: UI Enhancements & Testing (Week 4)
- Enhance animations and transitions.
- Test on different screen sizes and browsers.
- Debugging and performance optimization.

### Phase 4: Deployment & Final Testing (Week 5)
- Final round of testing.
- Deploy to a live environment.
- Collect feedback for future improvements.

## 2. Technologies to Use
- **Frontend:** React.js or Vanilla JavaScript with CSS animations
- **Backend (if needed):** Node.js / Firebase for managing discount codes
- **Storage:** LocalStorage (for storing discount codes if needed)

## 3. Risks & Mitigation
| Risk | Mitigation Strategy |
|------|---------------------|
| Game lag on mobile | Optimize animations, test performance |
| Users exploiting discount codes | Limit code access per session |
| UI/UX not engaging | Conduct user testing and iterate on feedback |

## 4. Success Metrics
- **Smooth and responsive gameplay** across devices.
- **Engaging design** and animations.
- **Proper functionality** of card flipping, timer, and reward system.
- **Bug-free experience** with minimal glitches.
