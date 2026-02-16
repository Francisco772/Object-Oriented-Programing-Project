# Object-Oriented-Programing-Project
"Cars"-themed arcade racer developed for Computation III (NOVA IMS). Built with Python &amp; Pygame to demonstrate OOP mastery (Inheritance, Polymorphism). Features Single &amp; Local Multiplayer modes, polymorphic power-ups (Invincibility, Shrink), and a "Bomb Dodge" special mode. Includes UML architecture.

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Pygame](https://img.shields.io/badge/Library-Pygame-green?style=for-the-badge&logo=pygame)
![NOVA IMS](https://img.shields.io/badge/Course-Computation%20III-red?style=for-the-badge)

## 🎓 Academic Context
This project was developed as the final assessment for the **Computation III (2023/2024)** course at **NOVA IMS**. 

The objective was not simply to create a game, but to demonstrate mastery of **Object-Oriented Programming (OOP)**, **Software Design Patterns**, and **UML Modeling** using Python.

---

## 🏗️ Architectural Design & OOP Implementation

The codebase is structured to maximize modularity and code reuse, utilizing key OOP concepts:

### 1. Inheritance & Polymorphism
The project makes extensive use of inheritance to handle game entities efficiently.
* **Abstract Base Classes (ABC):** The `PowerUp` class (`powerups.py`) acts as an abstract contract.
* **Polymorphism:** Specific implementations (`InvincibilityPowerUp`, `DoublePowerUp`, etc.) override the `affect_player()` method. This allows the game loop to treat all power-ups uniformly without knowing their specific types.
* **Sprite Inheritance:** The `Car` and `Bomb` classes inherit from `pygame.sprite.Sprite`, allowing for optimized rendering and collision detection.

### 2. Encapsulation & Modularity
The application logic is decoupled into distinct modules to ensure maintainability:
* **`car.py`**: Encapsulates all vehicle logic (movement physics, state management for power-ups).
* **`gamemode.py` vs `game.py`**: Separates the logic for different game states (Standard Racing vs. Bomb Dodge Mode), preventing a monolithic "god object."
* **`interface.py`**: Handles UI/UX logic separately from the core game loop.

### 3. UML Modeling
The system was designed using the **Unified Modeling Language (UML)** prior to implementation to ensure a robust class structure.
![UML Class Diagram](./UML_Diagram.png)
*(Note: Ensure your UML image is in the root folder of the repo)*

---

## 📂 Repository Structure

```text
├── main.py            # Entry point (Orchestrator)
├── car.py             # Car class (State management, Physics)
├── powerups.py        # Abstract Base Class & Polymorphic implementations
├── game.py            # Single Player Game Loop logic
├── multiplayer.py     # Local Multiplayer logic (Two-instance management)
├── gamemode.py        # Special "Bomb" Game Mode logic
├── interface.py       # Menu System & Event Handling
└── images/            # Assets

## 👥 Team
* **Ashool Lakhani**
* **Francisco Oliveira**
* **Tara Kouros**
