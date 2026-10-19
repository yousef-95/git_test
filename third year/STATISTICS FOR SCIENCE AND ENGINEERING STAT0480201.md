
## Conditional Probability :
conditional probability asks: "What is the chance of X happening, **given** that Y has already happened?"

Definition If A and B are any two events in a sample space S and P(A) ̸= 0, the conditional probability of B given A is P(B|A) = P(A ∩ B) P(A)

Theorem If A and B are any two events in a sample space S and P(A) ̸= 0, then: P(A ∩ B) = P(A) · P(B|A)

Alternatively, if P(B) ̸= 0, we have: P(A ∩ B) = P(B) · P(A|B)

Note: The multiplication rule can be derived by interchanging A and B and using the fact that A ∩ B = B ∩ A.

### 2. Step 1: The First Pick

When you reach into the shipment for the first time, the math is straightforward:  

```
Probability (1st is defective)=Number of DefectivesTotal / number of TVs = 15 / 240​
```

### 3. Step 2: The Second Pick (The Conditional Part)

This is the most important part of the slide. The slide specifies **"sampling without replacement."** This means once you take the first TV out, you do **not** put it back.

Because the first TV was defective, the "universe" has changed for the second pick:

- **The Total count drops:** There are now only **239** TVs left in the shipment.
    
- **The Defective count drops:** Since you already took one defective TV, there are now only **14** defectives left.
    

So, the probability of the second one being defective, **given** the first one was defective, is:  

```
P(2nd defective∣1st defective) = 14 / 239​
```

### 4. Step 3: The Final Calculation (The Multiplication Rule)

To find the probability of two events happening in a row (Event A AND Event B), you multiply the probability of the first event by the conditional probability of the second.

**The Formula:**  

```
P(Both Defective) = P(1st Defective) × P(2nd Defective∣1st Defective)
```

**The Math:**  

```
(15 / 240) × (14 / 239) = 210 / 57,360​
```

When you simplify that fraction, you get the final answer on the slide:  

```
7 / 1912
```

---

### 💡 Key Takeaway: Why this matters

If the problem had said **"with replacement"** (meaning you put the first TV back before picking the second), the numbers would not have changed. The calculation would have simply been:  

```
(15 / 240) × (15 / 240)
```

**Whenever you see "without replacement" or "succession," always remember to subtract 1 from both the numerator and the denominator for the second pick!**

### 1. What does "Independent" actually mean?

In plain English, two events are independent if **the occurrence of one does not change the probability of the other.**

Imagine you flip a coin and roll a die at the same time.

- Does getting a "Head" on the coin make it more likely that you'll roll a "6" on the die? **No.**
    
- Does rolling a "1" on the die change the odds of the coin being "Tails"? **No.**
    

Because the outcome of the coin does not affect the outcome of the die, these two events are **independent**.

---

### 2. The Mathematical Definition (The Formula)

The slide provides the "test" used to prove independence mathematically:

```
P(A∩B)=P(A)⋅P(B)
```

**How to use this formula:**  
If you are given three probabilities—the probability of A , the probability of B , and the probability of them both happening ( A∩B )—you can check for independence like this:

1. Multiply P(A) by P(B).
    
2. Compare that result to the actual P(A∩B).
    
3. **If they are equal**, the events are **Independent**.
    
4. **If they are NOT equal**, the events are **Dependent**.
    

---

### 3. Independence vs. Conditional Probability

To really understand this slide, you have to connect it to the "Conditional Probability" you learned in slides 36–37.

Recall the formula: P(B∣A)=P(A∩B)P(A)​ .  
If events are **independent**, then P(B∣A) is simply P(B) . In other words: "The probability of B, given that A happened, is still just the probability of B."

**Example comparison:**

- **Dependent:** Picking two defective TVs without replacement (Slide 40). The first pick changes the odds for the second pick. ( P(2nd)≠P(2nd∣1st)P(2nd) ).
    
- **Independent:** Picking two defective TVs **with replacement**. You put the first TV back, so the odds for the second pick stay exactly the same. ( P(2nd)=P(2nd∣1st) ).

### Summary Table:

|                 |                                     |                        |
| --------------- | ----------------------------------- | ---------------------- |
| Relationship    | Meaning                             | Math Test              |
| **Independent** | ```A``` doesn't care about ```B```  | ```P(A∩B)=P(A)×P(B)``` |
| **Dependent**   | ```A``` affects the odds of ```B``` | ```P(A∩B)≠P(A)×P(B)``` |

###  Summary for your Exam:

Whenever you see a problem with a **balanced coin**, a **balanced die**, or **"sampling with replacement,"** follow these steps:

1. **Find the probability of one single event** (e.g., 1/2 for a coin, 1/6​ for a die).
    
2. **Identify how many times** that event needs to happen.
    
3. **Multiply** the probabilities together for every step of the sequence.
    

**Common Mistake to Avoid:** Do not add the probabilities! Adding is for "OR" (Union); Multiplying is for "AND" (Intersection/Sequences).

###  Summary Cheat Sheet for "Total Probability" Problems:

When you see a problem that says "The probability of X is [this] if Y happens, and [that] if Y doesn't happen," follow these steps:

1. **Identify the "Conditions"** (e.g., Strike vs. No Strike).
    
2. **Find the probability of each condition** (e.g., 0.60 and 0.40).
    
3. **Find the conditional probability for each** (e.g., 0.35 and 0.85).
    
4. **Multiply** across each path, then **Add** the results together.


### Slide 53: The Illustration (The "Visual")

This slide turns the scary math from Slide 52 into a simple picture.

- **The Big Rectangle (** **`S`** **):** This is the entire Sample Space (the whole "cake").
    
- **The Vertical Colored Strips (** **`B1,B2…Bk​`** **):** These are the **Partition**. Notice they are side-by-side with no overlaps and no gaps. They represent your different scenarios (e.g., Rental Agency A, Agency B, Agency C).
    
- **The Blue Oval (**  **`A`** **):** This is the event you are trying to find the total probability for.
    
**The Logic of the Picture:**  
The blue oval A is made up of several smaller "slices."

- One slice is where A overlaps with B1.
    
- One slice is where A overlaps with B2.
    
- ...and so on.
    
To find the **Total Area of** **`A`** , you simply add up all those little slices. This is exactly what the ∑ (summation) symbol in the formula is doing.

---

### 💡 Summary: How to use this in an exam

When you see a problem with **multiple categories** (like the rental car agencies in Slide 54), don't let the formula scare you. Just follow the "Slices" logic:

1. **Identify the "Slices" (The Partition):** What are the different scenarios? (e.g., Agency A, B, and C).
    
2. **Find the weight of each slice:** What is the probability of each scenario? (P(B1),P(B2),…)
    
3. **Find the "Hit Rate" for each slice:** What is the probability of the event A happening inside that specific slice? (P(A∣B1),P(A∣B2),…)
    
4. **Multiply and Add:** (Weight × Hit Rate) for each slice, then add them all together.


### 1. The "Local" vs. "Global" Problem

- **`P(O∣A)=0.09P(O∣A)=0.09`**
    
    is a **local** probability. It only tells you what happens inside Agency A. It doesn't care about the rest of the world.
    
- **`P(A∩O)=P(A)⋅P(O∣A)P(A∩O)=P(A)⋅P(O∣A)`**
    
    is a **global** probability. It tells you the chance that a car is both from Agency A AND needs an oil change, relative to the **entire fleet of cars**.
    

**Analogy:**  
Imagine two classrooms:

- **Class A (100 students):** 10% are wearing red hats → (10 students)
    
- **Class B (10 students):** 90% are wearing red hats → (9 students)
    
If you just sum the percentages: 10%+90%=100%. Does that mean everyone in the whole school is wearing a red hat? **No.**  
You have to weight the percentages by the size of the class : **(100/110×0.10)+(10/110×0.90)=Total % of red hats in school.**

---

### 2. The "Impossible Total" (Logical Proof)

If we just summed conditional probabilities, the math would break the most basic rule of probability (Rule 1 from slide 23: (P(A)≤1).

Imagine you have 10 different rental agencies, and each one has a **20%** oil change rate.  
If you just summed them:  **0.20+0.20+0.20+0.20+0.20+0.20+0.20+0.20+0.20+0.20=2.0 (or 200%)**

**It is impossible for the probability of an oil change to be 200%.** The total probability must be between 0 and 1. By multiplying by P(A),P(B) , etc., you ensure the final answer stays within the logical limit of 100%.

---

### 3. What is actually happening in the math?

When you do P(A)⋅P(O∣A) , you are finding the **Intersection** (The "AND").

- **Agency A's contribution:** 0.60×0.09=0.054.
    
    - This means: "There is a 5.4% chance that a randomly picked car is from Agency A AND needs an oil change."
        
- **Agency B's contribution:** 0.30×0.20=0.060.
    
    - This means: "There is a 6% chance that a randomly picked car is from Agency B AND needs an oil change."
        
- **Agency C's contribution:** 0.10×0.06=0.006.
    
    - This means: "There is a 0.6% chance that a randomly picked car is from Agency C AND needs an oil change."
        

**Now that these are all "global" percentages, you can safely add them together:**  0.054+0.060+0.006=0.12

### Summary Table

|               |                                |            |                                                    |
| ------------- | ------------------------------ | ---------- | -------------------------------------------------- |
| Method        | Calculation                    | Result     | Meaning                                            |
| **Wrong Way** | ```∑P(O∣Agency)```             | ```0.35``` | Adding "local" rates (makes no sense).             |
| **Right Way** | ```∑[P(Agency)⋅P(O∣Agency)]``` | ```0.12``` | Adding "global" contributions (Total Probability). |


### **1. Set Operations (Foundations for Probability)**

- **Union ($A \cup B$):** All elements that are in set A, set B, or both.
    
      
    
- **Intersection ($A \cap B$):** Elements common to both set A and set B.
    
      
    
- **Complement ($A^c$):** All elements in the sample space $S$ that are not in set A.
    
      
    
- **Mutually Exclusive Events:** Two events are mutually exclusive if they have no elements in common:
    
      
    
    $$A \cap B = \emptyset$$
    

### **2. Basic Probability Rules**

- **Rule 1 (Range of Probability):** The probability of any event $A$ must be a non-negative real number less than or equal to 1.
    
      
    
    $$0 \le P(A) \le 1$$
    
- **Rule 2 (Probability of Sample Space):** The probability of the entire sample space is always 1.
    
      
    
    $$P(S) = 1$$
    
- **Rule 3 (Additivity):** If events $A_1, A_2, A_3, \dots$ are mutually exclusive, the probability of any one of them occurring is the sum of their individual probabilities:
    
      
    
    $$P(A_1 \cup A_2 \cup A_3 \cup \dots) = P(A_1) + P(A_2) + P(A_3) + \dots$$
    
- **Rule 4 (Complement Rule):** The probability that an event does not occur is 1 minus the probability that it does occur.
    
      
    
    $$P(A^c) = 1 - P(A)$$
    
- **Rule 5 (Subset Rule):** If event $A$ is a subset of event $B$ ($A \subseteq B$), then:
    
      
    
    $$P(A) \le P(B)$$
    
- **Rule 6 (General Addition Rule):** For any two events $A$ and $B$ in a sample space $S$:
    
      
    
    $$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$
    

### **3. Conditional Probability & Multiplication**

- **Conditional Probability Formula:** The probability of event $B$ occurring given that event $A$ has already occurred (where $P(A) \neq 0$):
    
      
    
    $$P(B\vert{}A) = \frac{P(A \cap B)}{P(A)}$$
    
- **Multiplication Rule (Theorem):** The probability that both $A$ and $B$ occur is the product of the probability of $A$ and the conditional probability of $B$ given $A$.
    
      
    
    $$P(A \cap B) = P(A) \cdot P(B\vert{}A)$$
    
    _(Alternatively, if $P(B) \neq 0$: $P(A \cap B) = P(B) \cdot P(A\vert{}B)$)_
    
      
    

### **4. Independence**

- **Definition of Independent Events:** Two events $A$ and $B$ are independent if and only if:
    
      
    
    $$P(A \cap B) = P(A) \cdot P(B)$$
    

### **5. Rule of Total Probability**

- **Simple Case (Binary Partition):**
    
      
    
    $$P(A) = P(B) \cdot P(A\vert{}B) + P(B') \cdot P(A\vert{}B')$$
    
- **General Theorem:** If events $B_1, B_2, \dots, B_k$ constitute a partition of the sample space $S$ and $P(B_i) \neq 0$:
    
      
    
    $$P(A) = \sum_{i=1}^{k} P(A \cap B_i) = \sum_{i=1}^{k} P(B_i) \cdot P(A\vert{}B_i)$$
    

### **6. Bayes' Theorem**

- **Theorem:** Used to find the "inverse" conditional probability. If $B_1, \dots, B_k$ is a partition of $S$ and $P(A) \neq 0$:
    
      
    
    $$P(B_r\vert{}A) = \frac{P(B_r \cap A)}{P(A)} = \frac{P(B_r) \cdot P(A\vert{}B_r)}{\sum_{i=1}^{k} P(B_i) \cdot P(A\vert{}B_i)}$$
    
    _(for $r = 1, 2, \dots, k$)_


### **1. Is $P(A \text{ AND } B) = P(B \text{ AND } A)$?**

- **Yes.** In mathematics, "AND" (the intersection $\cap$) is commutative. This means the order doesn't matter. Whether you say "the probability that it is raining AND cold" or "the probability that it is cold AND raining," you are describing the exact same event.
    
    $$P(A \cap B) = P(B \cap A)$$
    

### **2. Can we use either formula?**

- **Yes**, you can use either approach to find the answer. However, the notation in the original prompt had a slight error:
    
    - **Wrong:** $P(A) \times P(A\vert{}B)$ _(This doesn't make sense because you are multiplying the probability of $A$ by the probability of $A$ again)._
        
    - **Correct:** $P(B) \times P(A\vert{}B)$
        

The two correct ways to calculate the intersection are:

- **Option 1:** $P(A) \cdot P(B\vert{}A)$ $\rightarrow$ (Prob. of $A$ happening, then prob. of $B$ happening given $A$)
    
- **Option 2:** $P(B) \cdot P(A\vert{}B)$ $\rightarrow$ (Prob. of $B$ happening, then prob. of $A$ happening given $B$)
    

Because $P(A \cap B) = P(B \cap A)$, these two formulas will always give you the exact same result.

### **💡 Practical Example: Drawing Cards**

Imagine a standard deck of 52 cards:

- **Event A:** Drawing a King
    
- **Event B:** Drawing a Red card
    

We want to find the probability of drawing a card that is both a King AND Red.

- **Using Option 1 ($P(A) \cdot P(B\vert{}A)$):**
    
    - $P(A)$ [Prob. it's a King]: $\frac{4}{52}$
        
    - $P(B\vert{}A)$ [Prob. it's Red, given we know it's a King]: $\frac{2}{4}$ _(There are 4 kings, 2 are red)_
        
    - **Calculation:** $\frac{4}{52} \cdot \frac{2}{4} = \frac{8}{208} = \frac{1}{26}$
        
- **Using Option 2 ($P(B) \cdot P(A\vert{}B)$):**
    
    - $P(B)$ [Prob. it's Red]: $\frac{26}{52}$
        
    - $P(A\vert{}B)$ [Prob. it's a King, given we know it's Red]: $\frac{2}{26}$ _(There are 26 red cards, 2 are kings)_
        
    - **Calculation:** $\frac{26}{52} \cdot \frac{2}{26} = \frac{52}{1352} = \frac{1}{26}$
        

### **Summary: Which one should you use?**

In a test or a real-world problem, you choose based on what information you are given:

- If the problem tells you $P(A)$ and $P(B\vert{}A)$, use **Option 1**.
    
- If the problem tells you $P(B)$ and $P(A\vert{}B)$, use **Option 2**.