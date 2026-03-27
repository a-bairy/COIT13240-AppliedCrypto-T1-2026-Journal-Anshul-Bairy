# Week 2: Classical Ciphers & Cryptanalysis
> "The attacker ALWAYS knows the algorithm. Stop trying to hide the math; hide the key."
[Return to contents](README.md)

**My General Overview while skimming through the content at first:**
This week is foundation for everything. If I don't understand *why* classical ciphers failed (e.g., small key space, frequency analysis), I won't understand *why* modern ciphers (AES) are designed the way they are. 

**Time Allocation**
- **Lecture**: 1.5 hours
- **Tutorial Execution (Python Caesar /Rail Fence):** 2 hours
- **Journaling:** 30 min
- **Review & Checklist:** 30 min

---

## 3. 🗺️ Concept Map

```mermaid
graph TD
    A[Classical Ciphers] --> B(Substitution Ciphers)
    A --> C(Transposition Ciphers)
    B --> D[Monoalphabetic]
    B --> E[Polyalphabetic]
    D --> F(Caesar Cipher)
    D --> G(Simple Substitution)
    E --> H(Playfair Cipher)
    E --> I(Vigenère Cipher)
    E --> J(One-Time Pad)
    C --> K(Rail Fence)
    F --> L((Brute Force Vulnerable))
    G --> M((Frequency Analysis Vulnerable))
    I --> N((Kasiski Method Vulnerable))
    J --> O((Unconditionally Secure))
```

![Week 2 Notes Part 1](images/02_week_260319_003440_1.jpg)
![Week 2 Notes Part 2](images/02_week_260319_003440_2.jpg)
![Week 2 Notes Part 3](images/02_week_260319_003440_3.jpg)
![Week 2 Notes Part 4](images/02_week_260319_003440_4.jpg)

Add your entry here.
