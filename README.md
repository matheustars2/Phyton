#!/usr/bin/env python3
import random
import json
import os
from datetime import datetime

SCORES_FILE = "scores.json"

FORTUNES = [
    "Today is a great day to start something new.",
    "A pleasant surprise is coming your way.",
    "Trust your intuition.",
    "Small steps lead to big achievements.",
    "Someone appreciates your friendship.",
    "Time to practice patience.",
    "Enjoy the small victories.",
]

def load_scores():
    if not os.path.exists(SCORES_FILE):
        return []
    try:
        with open(SCORES_FILE, "r", encoding="utf-8") as f:
            return json.load(f)
    except Exception:
        return []

def save_score(name, score):
    scores = load_scores()
    scores.append({"name": name, "score": score, "date": datetime.utcnow().isoformat()})
    with open(SCORES_FILE, "w", encoding="utf-8") as f:
        json.dump(scores, f, ensure_ascii=False, indent=2)

def clear_screen():
    os.system("cls" if os.name == "nt" else "clear")

def play():
    clear_screen()
    print("=== Fortune Co

        inp = input("Pressione Enter para abrir um biscoito (ou 'q' para sair): ")
        if inp.strip().lower() == "q":
            break

        points = random.randint(1, 10)

