 📝 Sentence Analysis Algorithm

> *Read a sentence. Count everything that matters.*

---

 🔍 What It Does

Drop a sentence and this algorithm will instantly tell you:

| Metric | Description |
|--------|-------------|
| 📏 Length | Total number of characters |
| 📖 Words  | Total number of words      |
| 🔤 Vowels | Total number of vowels     |

---

 ⚙️ How It Works

- Reads the sentence **one character at a time**
- Detects words using a **boolean flag** instead of counting spaces
- Handles vowels with a **lowercase conversion** to keep checks minimal
- Stops reading when it hits a **period (.)**

---

 💡 Example

**Input:**
```
" i am looking for a city with a true foundation."
```

**Output:**
```
Length  : 48
Words   : 9
Vowels  : 18
```

---

 🧠 Key Concepts

- `inWord` flag detects the **moment we step into a new word**
- `LOWERCASE()` reduces vowel comparisons from **10 down to 5**
- The **period is never counted** in the length
- A **leading space** counts toward length but not word count

---

*Built as part of an Algorithm Checkpoint — pseudocode implementation.*
```
