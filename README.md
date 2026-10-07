# Theory of Computation — JFLAP Web Edition
### Developed by **Gururaj Surampalli**

An interactive, browser-based pedagogical studio for teaching, learning, and experimenting with **Formal Languages and Automata Theory**. Designed as a modern, Java-free web alternative to JFLAP.

---

## 🌟 Key Features & Supported Models

### 1. Finite Automata (DFA / NFA / ε-NFA)
- **Interactive Visual Canvas**: Drag and drop states, draw directed transitions, curvature controls, and self-loops.
- **State Properties**: Mark Initial states ($\to$), Final/Accept states ($\mathcal{F}$, rendered with double ring $\odot$).
- **Step-by-Step Visual Simulation**: Step forward, step backward, or auto-run with adjustable simulation speeds.
- **Non-Deterministic Branching**: Visualizes multi-state active sets $\{q_0, q_1\}$ simultaneously during NFA execution.
- **Batch String Tester**: Test multiple strings in parallel with instant PASS / FAIL checkmarks.
- **Transition Table**: Auto-generates $\delta(q, a)$ matrix with initial and final state indicators.

### 2. Conversions & Algorithms
- **NFA $\to$ DFA Subset Construction**:
  - Full powerset subset construction with $\epsilon$-closure.
  - Step-by-step transition table with dead state handling.
  - One-click **"Load DFA onto Canvas"** to simulate the resulting DFA.
- **DFA Minimization**:
  - Removes unreachable states.
  - Myhill-Nerode & Hopcroft Table-Filling algorithm with interactive distinguishable pairs staircase table ($X$ vs $\equiv$).
  - One-click **"Load Minimized DFA onto Canvas"**.
- **Finite Automata $\to$ Regular Expression**:
  - State elimination method (Generalized NFA / Arden's theorem).
  - Iterative step-by-step state removal log and final formula generator.
- **Regular Expression $\to$ $\epsilon$-NFA**:
  - Thompson's Construction algorithm supporting union (`|`), concatenation, Kleene star (`*`), positive closure (`+`), and parentheses `()`.
- **Regular Grammar $\leftrightarrow$ Finite Automata**:
  - Bidirectional conversion between Right-Linear Grammars ($A \to aB \mid b$) and NFA/DFA models.

### 3. Transducers (Mealy & Moore Machines)
- **Mealy Machine**: Outputs produced on transitions ($a/y$).
- **Moore Machine**: Outputs produced on states ($q_i/y$).
- **Simulation**: Real-time visualization of Input Stream, State Traversal Sequence, and Output Stream.
- **Mealy $\leftrightarrow$ Moore Converter**: Automatic bidirectional machine translation.

### 4. Pushdown Automata (PDA)
- **Animated Pushdown Stack**: Vertical stack visualization showing push and pop animations in real time.
- **Acceptance Modes**: Final State, Empty Stack, or Both.
- **Instantaneous Description (ID) Trace**: $(q, w, \gamma) \vdash (q', w', \gamma')$.
- **CFG $\to$ PDA Generator**: Top-down / LL parser PDA synthesis.

### 5. Context-Free Grammars (CFG) & Parsing
- **FIRST & FOLLOW Sets**: Fixed-point iterative calculation with $\epsilon$ propagation and end-marker (`$`).
- **LL(1) Parser**:
  - $M[A, a]$ parsing table generator.
  - Conflict detection (Is LL(1)? Yes/No with explanation).
  - Interactive stack parsing simulation trace ($Stack \mid Input \mid Action$).
- **SLR(1) Parsing**:
  - Canonical collection of $LR(0)$ items (Closures & Gotos).
  - SLR(1) ACTION & GOTO parsing tables with Shift/Reduce conflict detector.
- **Chomsky Normal Form (CNF) 5-Step Pipeline**:
  - 1. Start symbol simplification ($S_0 \to S$)
  - 2. $\epsilon$-productions elimination
  - 3. Unit productions elimination ($A \to B$)
  - 4. Terminal substitution
  - 5. Binarization of long productions

### 6. Turing Machines (Single-Tape & Multi-Tape)
- **Visual Endless Tape Ribbon**: Animated horizontal ribbon with head cursor pointer.
- **Multi-Tape Support**: 2-Tape Turing machine support with synchronized head movements.
- **Transition Semantics**: $\text{read} \to \text{write}, \text{Move } (L, R, S)$.
- **Classic Presets**: Binary Incrementer, Palindrome Decider ($w w^R$), $a^n b^n c^n$ decider.

### 7. Pumping Lemma Interactive Lab
- **Adversarial Game**:
  - Step 1: Select language to disprove (e.g. $0^n 1^n$, $w w^R$, $0^{n^2}$, $0^p$, $a^n b^n c^n$).
  - Step 2: Adversary picks pumping length $p$.
  - Step 3: Player chooses string $s \in L$ with $|s| \ge p$.
  - Step 4: Adversary generates all valid decompositions ($s = xyz$ or $s = uvwxy$).
  - Step 5: Player selects pump exponent $i \ge 0$ to construct contradiction $x y^i z \notin L$.

### 8. L-Systems (Lindenmayer Systems)
- Parallel string replacement engine.
- 2D Turtle Graphics renderer with automatic viewport centering and scaling.
- Presets: Koch Snowflake, Sierpinski Triangle, Dragon Curve, Barnsley Fern, Fractal Tree.

---

## 🚀 How to Run

Because this application is built purely with standard modern HTML5, CSS3, and JavaScript, **no installation, build steps, or external dependencies are required**:

1. Simply double-click `index.html` to open it in any modern browser (Chrome, Edge, Firefox, Safari).
2. Alternatively, run a local static server:
   ```bash
   python -m http.server 8000
   ```
   and visit `http://localhost:8000`.

---

## 👨‍💻 Author & Attribution
- **Developer**: Gururaj Surampalli
- **Course / Topic**: Formal Languages and Automata Theory (Theory of Computation)
