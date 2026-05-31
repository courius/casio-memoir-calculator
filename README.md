# casio-memoir-calculator
# 🧮 Custom Math Parser Calculator (A Digital Memoir)

A fully functional, responsive web-based calculator built from scratch using vanilla web technologies. Featuring a custom tokenized string parser that respects mathematical order of operations (PEMDAS), defensive boundary constraints, and dynamic CSS styling.

---

## 🌟 The Story Behind the Project
This project is a digital memoir. The design and texture are a recreation of a beloved physical Casio scientific calculator that my brother used for years before gifting it to me a long time ago. It still serves me faithfully to this day, but I built this application to preserve its memory and legacy in code just in case the physical hardware ever dies.

---

## 🚀 Core Features & Technical Engineering

* **Custom Abstract Math Parser:** Instead of taking traditional multi-input values or taking shortcuts like JavaScript's unsafe `eval()` function, this application captures a raw string expression (e.g., `2+4-5*2`), splits it using lookahead/lookbehind Regular Expressions (RegEx), and processes it via a multi-pass token evaluation system.
* **PEMDAS/Order of Operations Compliance:** The logic engine utilizes cascading array-collapsing loops that scan, solve, and splice high-priority operators (`*` and `/`) before executing lower-priority calculations (`+` and `-`).
* **Advanced Error Handling:** Implements defensive programming blocks to intercept illegal operator strings (like consecutive operators or floating signs), smoothly halting the parser to output custom context-aware `MATH ERROR` exceptions without crashing the script thread.
* **State Management Configuration:** Built-in custom boolean flags that elegantly separate the user input phase from the final calculation render phase, cleanly clearing or appending text depending on context (e.g., handling continuous operators natively).
* **Tactile Sliding Slide-Off Cover UI:** Fully immersive introduction animation built using CSS transformations and asynchronous `setTimeout` timers to coordinate a hardware-accelerated mechanical slide-off cover upon clicking.
* **Uniform CSS Grid Matrix:** The button layouts leverage native CSS Grid configurations optimized with `minmax(0, 1fr)` templates to guarantee perfectly uniform button sizing regardless of variations in text content length.

---

## 🛠️ Built With

* **HTML5** - Structured semantics and interactive DOM inputs.
* **CSS3** - Custom layouts (Grid & Flexbox), absolute overlay positioning, and fluid transitions.
* **JavaScript (ES6+)** - Custom string parsing algorithms, Regex tokenization, DOM manipulation methods, and asynchronous events.

---

## 📈 Future Roadmaps
* Implement support for parentheses tracking.
* Expand the RegEx map to intercept native multi-character math constants like $\pi$ or $e$.
