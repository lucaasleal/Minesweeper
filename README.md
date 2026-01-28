# Minesweeper

AI This project implements an AI to play Minesweeper using Python, following concepts from CS50’s Introduction to Artificial Intelligence. 
The AI can infer which cells are safe and which contain mines, making intelligent decisions without guessing whenever possible. 

## 🧠 **Project Idea** 
The goal is to build a knowledge-based agent that plays Minesweeper logically. The AI observes the number of neighboring mines for each revealed safe cell and updates its knowledge base, making inferences to identify mines and safe cells automatically. 

## 📊 **Data Representation** 
The board is represented as a 2D matrix (list of lists) in Python: 
- `True` represents a mine
- `False` represents a safe cell The AI maintains three main structures:
- `self.moves_made`: cells that have already been revealed
- `self.mines`: cells that the AI knows are mines
- `self.safes`: cells that the AI knows are safe Each logical sentence is represented as: ```python {A, B, C} = 2 ``` Meaning exactly 2 of the cells A, B, and C are mines. 

## ⚙️ **Technologies Used** 
- Python 3
- Pygame
- OOP
- Data structures: lists and sets
- Logical inference algorithms
- Knowledge-based reasoning 

## 🧩 **How the AI Works** 
1. When a safe cell is revealed, the AI receives the number of neighboring mines. 
2. A new **Sentence** is created with the unknown neighboring cells and the number of mines. 
3. The AI marks cells as safe or as mines whenever possible using: 
- If the number of unknown cells equals the remaining mine count, all are mines
- If the remaining mine count is 0, all unknown cells are safe 4.
- New sentences can be inferred from existing sentences using **subset inference**.
- This allows the AI to solve many situations without guessing. When no certainty exists, it makes a safe random move. 

## ▶️ **How to Run the Project** 
Clone the repository and install dependencies: 
```bash 
git clone https://github.com/lucaasleal/MinesweeperAI.git
cd MinesweeperAI
pip install pygame
```
Expected folder structure: 
``` 
├── minesweeper.py 
├── runner.py
├── requirements.txt
└── README.md
```

Run the game (or let the AI play): 
```bash 
python3 runner.py
```
## 🚀 **Possible Improvements** 
- Add a more interactive graphical interface
- Optimize inference with advanced heuristics
- Create difficulty levels to test the AI

## 📚 **Inspiration** 
Inspired by **CS50’s Introduction to Artificial Intelligence**, using concepts of **Knowledge Representation** and **Logical Inference**. 

## 👤 **Author** 
[@lucaasleal](https://github.com/lucaasleal)

