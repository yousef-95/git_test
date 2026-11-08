
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


# CH1 :
## **Document 1: Formulas and R Code**

Here are **all formulas and R code** from the file.

  

> **Note:** The PDF OCR shows `teacher.dataS GPA` / `teacher.dataSScore`; in R you must use `$`, e.g., `teacher.data$GPA`.
> 
>   

## **1. Exercise 1 — Create teacher data frame**

R

```
t.name   <- c("Sara", "John", "Jane", "Stacy")
t.gender <- c("F", "M", "F", "F")
degree   <- c("PhD", "Bachelor", "Master", "Bachelor")
GPA      <- c(3.22, 3.54, 3.00, 2.87)
Exp.Y    <- c(3, 12, 6, 8)

teacher.data <- data.frame(t.name, t.gender, degree, GPA, Exp.Y)
teacher.data
```

## **2. Print the GPA column**

R

```
print(teacher.data$GPA)
print(teacher.data[["GPA"]])
print(teacher.data[, 4])
```

## **3. Add a new column `Score`**

R

```
teacher.data$Score <- c("95%", "93%", "97%", "90%")
print(teacher.data)
```

## **4. Remove the `Years of experience` / `Exp.Y` column**

R

```
teacher.data$Exp.Y <- NULL
print(teacher.data)
```

## **5. Statistical measurements — R commands**

The file lists these R commands for a numeric vector `x`:

  

R

```
summary(x)   # summary / can be used for mean
mean(x)      # mean
median(x)    # median
IQR(x)       # interquartile range
var(x)       # variance
sd(x)        # standard deviation
```

If you need the data vector implied by the summary table in the PDF:

  

R

```
x <- c(10, 16, 16, 19, 21, 24, 39, 46, 77,
       80, 86, 108, 144, 154, 157, 250, 408)
```

Then you can use:

  

R

```
summary(x)
mean(x)
median(x)
IQR(x)
var(x)
sd(x)
```

## **6. Formulas from the file**

### **Mean**

$$\bar{X}=\frac{\sum x_i}{n}$$

Given in the file:

  

$$\sum x_i = 1655,\qquad \sum x_i^2 = 335081$$

### **Median**

For sorted data, the median is the middle value. Standard formula:

  

$$\text{If } n \text{ is odd: } \text{Median}=x_{(n+1)/2}$$

$$\text{If } n \text{ is even: } \text{Median}=\frac{x_{n/2}+x_{n/2+1}}{2}$$

The file says: “The position of the median is …” but does not print the completed formula.

  

### **Interquartile Range**

$$\mathrm{IQR}=Q_3-Q_1$$

In R:

  

R

```
IQR(x)
```

### **Variance**

$$s^2=\frac{\sum X_i^2-n(\bar{X})^2}{n-1}$$

Equivalent standard form:

  

$$s^2=\frac{\sum (X_i-\bar{X})^2}{n-1}$$

In R:

  

R

```
var(x)
```

### **Standard Deviation**

$$s=\sqrt{s^2}$$

In R:

  

R

```
sd(x)
```

## **7. Histogram code from the file**

R

```
hist(x)
```

R

```
hist(x, main = "Histogram of x", xlab = "values", col = "blue")
```

## **8. Boxplot code from the file**

R

```
boxplot(x,
        main = "The actual number of unemployed",
        xlab = "Boxplot",
        ylab = "unemployed",
        col = "green")
```

The file also asks to find the five-number summary and investigate outliers, but does **not** print explicit R code for that. Common R commands are:

  

R

```
summary(x)
fivenum(x)
boxplot.stats(x)$out
```

These are not printed in the PDF, but they are the usual R commands for five-number summary and outlier detection.

  

##
**Document 2: Histogram and Boxplot — Important Features**

In a histogram and a boxplot, the **important things are what each plot tells you about the distribution of the data**.

  

## **Histogram — important features**

A histogram shows the **shape of the distribution**.

  

Look for:

  

1. **Shape**
    
      
    - Symmetric
        
          
        
    - Right-skewed / positively skewed
        
          
        
    - Left-skewed / negatively skewed
        
          
        
    - Uniform
        
          
        
    - Bell-shaped
        
          
        
2. **Modality**
    
      
    - One peak = unimodal
        
          
        
    - Two peaks = bimodal
        
          
        
    - More peaks = multimodal
        
          
        
3. **Center**
    
      
    - Where most of the data is concentrated
        
          
        
4. **Spread**
    
      
    - Narrow vs wide distribution
        
          
        
    - Range of values
        
          
        
5. **Gaps / unusual values**
    
      
    - Empty gaps
        
          
        
    - Isolated bars far from the rest
        
          
        
6. **Outliers**
    
      
    - Values far from the main body of data
        
          
        
7. **Bin width matters**
    
      
    - Different bin widths can make the same data look different.
        
          
        
    - Too few bins hides detail; too many bins makes noise.
        
          
        

In the tutorial, the histogram is used to answer:

  

**“What is the distribution of the data?”**

  

Typical R code:

  

R

```
hist(x, main = "Histogram of x", xlab = "values", col = "blue")
```

## **Boxplot — important features**

A boxplot shows the **five-number summary** and helps detect **outliers**.

  

The five-number summary is:

  

$$\text{Minimum},\ Q_1,\ \text{Median},\ Q_3,\ \text{Maximum}$$

Important parts:

  

1. **Median**
    
      
    - The line inside the box.
        
          
        
    - Shows the center.
        
          
        
2. **First quartile ($Q_1$)**
    
      
    - Lower edge of the box.
        
          
        
    - 25% of data below it.
        
          
        
3. **Third quartile ($Q_3$)**
    
      
    - Upper edge of the box.
        
          
        
    - 75% of data below it.
        
          
        
4. **Interquartile range**
    
      
    

$$\mathrm{IQR}=Q_3-Q_1$$

- The height of the box.
    
      
    
- Measures spread of the middle 50% of the data.
    
      
    

5. **Whiskers**
    
      
    - Usually extend to the most extreme values that are **not outliers**.
        
          
        
    - Common rule:
        
          
        

$$\text{Lower fence}=Q_1-1.5\,\mathrm{IQR}$$

$$\text{Upper fence}=Q_3+1.5\,\mathrm{IQR}$$

Values outside these fences are often flagged as outliers.

  

6. **Outliers**
    
      
    - Points plotted individually beyond the whiskers.
        
          
        
    - In the tutorial boxplot, the single circle near the top is an outlier.
        
          
        
7. **Skewness clue**
    
      
    - If the median is closer to $Q_1$, the data may be right-skewed.
        
          
        
    - If the median is closer to $Q_3$, the data may be left-skewed.
        
          
        

In the tutorial, the boxplot is used to:

  

- Find the **five-number summary**
    
      
    
- Investigate the **occurrence of outliers**
    
      
    

Typical R code:

  

R

```
boxplot(x,
        main = "The actual number of unemployed",
        xlab = "Boxplot",
        ylab = "unemployed",
        col = "green")
```

Useful R commands for boxplot interpretation:

  

R

```
summary(x)
fivenum(x)
boxplot.stats(x)$stats   # whiskers, quartiles, median
boxplot.stats(x)$out     # outliers
IQR(x)
```

## **Short comparison**

|**Histogram**|**Boxplot**|
|---|---|
|Shows overall shape|Shows five-number summary|
|Shows modality and gaps|Shows median and quartiles|
|Bin width affects appearance|Compact summary|
|Can show skewness|Can hint at skewness|
|Can show outliers as isolated bars|Explicitly flags outliers|
|Better for seeing the full distribution|Better for comparing groups and detecting outliers|

**Most important summary:**

  

- **Histogram:** look at **shape, center, spread, modality, gaps, and outliers**.
    
      
    
- **Boxplot:** look at **median, $Q_1$, $Q_3$, IQR, whiskers, and outliers**.
    
      
    
- A boxplot can hide **bimodality**; a histogram can reveal it. So they are often used together.


## **Slide 74 — Symmetry, Right Skew, Left Skew**

This slide defines the **shape** of a distribution:

- **Symmetric distribution**: The left and right sides of the histogram are mirror images around the center.
    
- **Right-skewed / positively skewed**: The longer “tail” is on the **right** side.
    
- **Left-skewed / negatively skewed**: The longer “tail” is on the **left** side.
    

So skewness is about **which side has the long tail**, not simply where most data are.

## **Slide 76 — Right-Skewed Distribution**

A **right-skewed distribution** has:

- A long tail extending to the **right**
    
- Most data concentrated on the left, with a few large values pulling the tail right
    
- Relationship usually stated as:
    

$$\text{Mean} > \text{Median} > \text{Mode}$$

**The slide’s explanation:** In right-skewed data, the right tail is longer, and the mean is greater than the median, which is greater than the mode.

**Intuition:** Large values on the right pull the mean upward more than they pull the median.

## **Slide 77 — Left-Skewed Distribution**

A **left-skewed distribution** has:

- A long tail extending to the **left**
    
- Most data concentrated on the right, with a few small values pulling the tail left
    
- Relationship usually stated as:
    

$$\text{Mean} < \text{Median} < \text{Mode}$$

**The slide’s explanation:** In left-skewed data, the left tail is longer, and the mean is less than the median, which is less than the mode.

**Intuition:** Small values on the left pull the mean downward more than they pull the median.

## **Slide 80 — Boxplot Components**

A **boxplot** summarizes a dataset using five summary statistics:

1. **Minimum**
    
2. **First quartile ($Q_1$)**
    
3. **Median ($Q_2$)**
    
4. **Third quartile ($Q_3$)**
    
5. **Maximum**
    

**Key parts:**

- **Box**: Represents the **interquartile range ($\mathrm{IQR}$)**, where the middle 50% of the data lie:
    

$$\mathrm{IQR} = Q_3 - Q_1$$

- **Vertical line inside the box**: The **median**.
    
- **Whiskers**: Extend from the box to the minimum and maximum values that are still within:
    

$$1.5 \times \mathrm{IQR}$$

from the quartiles.

- **Points beyond the whiskers**: Considered **outliers**.
    

So a boxplot shows spread, center, and possible outliers at a glance.

## **Slide 83 — Outliers in a Boxplot**

This slide explains how outliers appear on a boxplot:

- **Outliers** are points that fall outside the whiskers.
    
- They are unusually high or low compared with the rest of the data.
    
- In the example, values such as **5** and **10** are outliers, shown as individual points beyond the whiskers.
    

So if you see isolated dots beyond the whiskers in a boxplot, those are flagged as outliers.

## **Slide 85 — Comparing Three Boxplots**

This slide compares scores from three classes: **Class A, Class B, and Class C**.

**Interpretation from the slide:**

- **Class A**: Slightly wider spread of scores, with some higher values.
    
- **Class B**: More concentrated distribution; scores are clustered around the median.
    
- **Class C**: More variability, with a few lower scores and a wider range.
    

**In general, when comparing boxplots, look at:**

- **Median**: Typical value
    
- **Box height / $\mathrm{IQR}$**: Spread of middle 50%
    
- **Whiskers**: Overall range excluding outliers
    
- **Outlier points**: Unusual observations
    

## **Summary Table**

| **Slide** | **Main Idea**                                                                     |
| --------- | --------------------------------------------------------------------------------- |
| **74**    | Definitions of symmetric, right-skewed, and left-skewed distributions             |
| **76**    | Right skew: long right tail; $\text{Mean} > \text{Median} > \text{Mode}$          |
| **77**    | Left skew: long left tail; $\text{Mean} < \text{Median} < \text{Mode}$            |
| **80**    | Boxplot parts: min, $Q_1$, median, $Q_3$, max, $\mathrm{IQR}$, whiskers, outliers |
| **83**    | Outliers are points beyond whiskers; example shows 5 and 10 as outliers           |
| **85**    | Comparing boxplots across classes: spread, center, variability, and range         |

## **Slide 80 — Boxplot Components (Detailed View)**

A **boxplot** (also called a box-and-whisker plot) is constructed from the **five-number summary** of a dataset:

$$\text{Minimum},\quad Q_1,\quad \text{Median }(Q_2),\quad Q_3,\quad \text{Maximum}$$

### **1. The Five-Number Summary**

- **Minimum:** Smallest value (or smallest non-outlier value if outliers exist).
    
- **$Q_1$ (First Quartile / 25th Percentile):** About 25% of the data fall below it.
    
- **Median ($Q_2$ / 50th Percentile):** Splits the dataset into two equal halves.
    
- **$Q_3$ (Third Quartile / 75th Percentile):** About 75% of the data fall below it.
    
- **Maximum:** Largest value (or largest non-outlier value if outliers exist).
    

### **2. The Box**

The **box** spans from $Q_1$ to $Q_3$. Its height (or length) represents the **interquartile range ($\mathrm{IQR}$)**:

$$\mathrm{IQR} = Q_3 - Q_1$$

The $\mathrm{IQR}$ measures the dispersion of the **middle 50%** of the data:

- **Short box:** Indicates that the middle 50% of the data are tightly clustered.
    
- **Long box:** Indicates that the middle 50% of the data are more widely spread.
    

### **3. The Line Inside the Box**

The horizontal line inside the box marks the **median**:

- If the median is centered within the box, the middle half of the data is roughly symmetric.
    
- If the median is closer to $Q_1$ or $Q_3$, it hints at potential skewness.
    

### **4. The Whiskers**

The whiskers extend from the box boundaries toward the minimum and maximum values, controlled by standard fence criteria:

$$\text{Lower Fence} = Q_1 - 1.5 \times \mathrm{IQR}$$

$$\text{Upper Fence} = Q_3 + 1.5 \times \mathrm{IQR}$$

- The **lower whisker** extends to the smallest data point that is **$\ge$ Lower Fence**.
    
- The **upper whisker** extends to the largest data point that is **$\le$ Upper Fence**.
    
- Any data point lying beyond these fences is classified as a **potential outlier**.
    

**Whisker behavior:**

- **No outliers present:** Whiskers reach all the way to the absolute minimum and maximum values.
    
- **Outliers present:** Whiskers stop at the most extreme non-outlier values, and outliers are plotted individually as separate points.
    

### **5. Outliers**

Outliers are isolated data points that fall outside the whiskers. They represent unusually small or large observations compared to the rest of the dataset (e.g., extreme values such as **5** and **10** plotted as individual dots).

### **6. Insights Provided by a Boxplot**

A boxplot visualizes four core distributional traits:

- **Center:** Median position.
    
- **Spread:** $\mathrm{IQR}$ and overall range.
    
- **Skewness:** Median placement within the box and relative whisker lengths.
    
- **Outliers:** Isolated points beyond the fences.
    

### **7. Key Takeaway**

The boxplot does **not** display every individual data point; it compresses the dataset into quartiles and extremes. This summary property makes it ideal for rapidly comparing multiple distributions side-by-side.

# **Slide 85 — Comparing Three Boxplots (Class A, Class B, Class C)**

Slide 85 compares the examination score distributions of three distinct classes (**Class A**, **Class B**, and **Class C**).

Given datasets:

$$A = (65, 78, 85, 90, 45, 80, 72, 88, 93, 60, 70, 68, 95, 75)$$

$$B = (55, 82, 74, 66, 78, 88, 94, 71, 59, 85, 81, 73, 80, 90)$$

$$C = (40, 52, 67, 75, 89, 94, 61, 68, 72, 78, 81, 86, 95, 55)$$

### **Five-Number Summary Comparison Table**

|**Class**|**Minimum**|**Q1​**|**Median**|**Q3​**|**Maximum**|**IQR**|
|---|---|---|---|---|---|---|
|**Class A**|45|68.5|76.5|87.25|95|18.75|
|**Class B**|55|71.5|79.0|84.25|94|12.75|
|**Class C**|40|62.5|73.5|84.75|95|22.25|

### **Detailed Interpretation by Class**

#### **Class A**

- **Median:** $\approx 76.5$
    
- **$\mathrm{IQR}$:** $\approx 18.75$
    
- **Range:** $45 \text{ to } 95$
    
- **Characteristics:** Moderately wide middle 50% with high peak scores reaching 95.
    
- **Slide Notes:** _"Slightly wider spread of scores with some higher values."_
    

#### **Class B**

- **Median:** $\approx 79.0$ _(Highest median among all three classes)_
    
- **$\mathrm{IQR}$:** $\approx 12.75$ _(Smallest $\mathrm{IQR}$ / shortest box)_
    
- **Characteristics:** Highly consistent performance around the median value.
    
- **Slide Notes:** _"More concentrated distribution, with scores clustered around the median."_
    

#### **Class C**

- **Median:** $\approx 73.5$ _(Lowest median among all three classes)_
    
- **$\mathrm{IQR}$:** $\approx 22.25$ _(Largest $\mathrm{IQR}$ / tallest box)_
    
- **Range:** $40 \text{ to } 95$ _(Widest overall range)_
    
- **Characteristics:** Highest variability, containing several lower scores ($40, 52$).
    
- **Slide Notes:** _"More variability with a few lower scores and a wider range."_
    

### **Comparative Checklist for Boxplots**

1. **Medians (Center):**
    
    Class B has the highest typical performance ($\text{Median} = 79.0$), while Class C has the lowest ($\text{Median} = 73.5$).
    
2. **Box Height / $\mathrm{IQR}$ (Middle 50% Spread):**
    
    Class C exhibits the highest internal spread ($\mathrm{IQR} = 22.25$), whereas Class B is the most consistent ($\mathrm{IQR} = 12.75$).
    
3. **Overall Range:**
    
    Class C spans the widest range ($55$ points, from $40$ to $95$).
    
4. **Outlier Identification:**
    
    Applying the $1.5 \times \mathrm{IQR}$ rule reveals **no flagged outliers** across all three classes.
    
5. **Distribution Shape / Skewness:**
    
    Observed via median position relative to $Q_1$ and $Q_3$ alongside relative whisker extensions.
    

### **Conclusion**

- **Class B:** Most consistent group, highest central tendency.
    
- **Class A:** Moderate variability with strong high-end scores.
    
- **Class C:** Most variable group, lowest central tendency, and widest overall score dispersion.



A boxplot does **not** show the full shape of a distribution, so skewness from a boxplot is only a **visual clue**, not a definitive measure. However, you can often infer the likely direction of skewness by looking at:

1. **Where the median lies inside the box**
    
2. **The lengths of the two whiskers**
    
3. **Where outliers appear**
    
4. **A numerical check using quartiles** — Bowley skewness
    

## **1. Median Position Inside the Box**

The box runs from $Q_1$ to $Q_3$, and the median ($Q_2$) is the line inside:

- If the **median is closer to $Q_1$** and farther from $Q_3$, the data are likely **right-skewed**.
    
- If the **median is closer to $Q_3$** and farther from $Q_1$, the data are likely **left-skewed**.
    
- If the **median is roughly in the middle** of the box, the middle 50% of the data is fairly symmetric.
    

**Intuition:** In a right-skewed distribution, the bulk of the data is concentrated on the left, so the median tends to sit toward the lower quartile ($Q_1$). In a left-skewed distribution, the bulk is on the right, so the median tends to sit toward the upper quartile ($Q_3$).

## **2. Whisker Lengths**

Compare the distance from the box edges to the minimum and maximum non-outlier values:

- **Longer right whisker** $\rightarrow$ likely **right-skewed**
    
- **Longer left whisker** $\rightarrow$ likely **left-skewed**
    
- **Whiskers roughly equal** $\rightarrow$ likely **symmetric**
    

A longer whisker on one side indicates a longer tail on that side.

## **3. Outliers**

Outliers can also provide visual clues:

- Outliers mostly on the **right** $\rightarrow$ likely **right-skewed**
    
- Outliers mostly on the **left** $\rightarrow$ likely **left-skewed**
    
- Outliers on both sides or none $\rightarrow$ less conclusive
    

_Note:_ Outliers alone are not definitive; a single extreme value can create an outlier without the overall distribution being strongly skewed.

## **4. Numerical Check: Bowley Skewness**

You can compute a quartile-based skewness measure:

$$\text{Bowley Skewness} = \frac{(Q_3 - Q_2) - (Q_2 - Q_1)}{Q_3 - Q_1}$$

Equivalently:

$$\text{Bowley Skewness} = \frac{Q_3 + Q_1 - 2Q_2}{Q_3 - Q_1}$$

**Interpretation:**

- **Positive value ($> 0$)** $\rightarrow$ **Right-skewed**
    
- **Negative value ($< 0$)** $\rightarrow$ **Left-skewed**
    
- **Near zero ($\approx 0$)** $\rightarrow$ **Roughly symmetric**
    

This directly aligns with the visual clues: if the median is closer to $Q_1$, then $(Q_3 - Q_2) > (Q_2 - Q_1)$, producing a positive result.

## **Summary Table**

|**Boxplot Feature**|**Likely Skewness**|
|---|---|
|Median closer to $Q_1$; longer right whisker; right outliers|**Right-skewed**|
|Median closer to $Q_3$; longer left whisker; left outliers|**Left-skewed**|
|Median near center of box; whiskers of similar length|**Roughly symmetric**|

## **Important Caution**

A boxplot can suggest skewness, but it **cannot prove** it. Two completely different underlying distributions can share identical five-number summaries. For a complete and reliable assessment, always cross-examine with a **histogram** or **density plot**.

> **Practical Rule:** Combine **Median Position + Whisker Lengths + Outlier Direction** to hypothesize skewness, then confirm using a histogram or Bowley's coefficient.


# CH2:
إليك النص معدلاً ومصمماً بعناية فائقة، مع الحفاظ على كافة المحتويات الأكاديمية والرياضية (معادلات LaTeX والجداول) بالكامل دون أي نقص أو تلخيص، وتصحيح أي خطأ في التنسيق:

  

## **Document 1: Probability Formulas and Rules**

Below are **all probability formulas/rules**, with **when to use them**.

  

**Notation:** $S$ = sample space, $A, B$ = events, $A^c$ = complement of $A$, $B'$ = complement of $B$, $B_i$ = parts of a partition.

  

## **1. Basic probability rules**

|**Formula**|**When to use**|
|---|---|
|$$P(A)\ge 0$$|Probability cannot be negative. Use as a validity check.|
|$$P(S)=1$$|The probability that some outcome in the sample space occurs is 1.|
|$$0\le P(A)\le 1$$|Every event probability must lie between 0 and 1.|
|$$P(A^c)=1-P(A)$$|Use when you want the probability that $A$ does **not** occur, or “neither/nor” via complement of a union.|
|$$A\cap B=\varnothing$$|Two events are mutually exclusive if they cannot occur together.|
|If $A\cap B=\varnothing$, then<br><br>  <br><br>$$P(A\cup B)=P(A)+P(B)$$|Use for “A or B” when the events are mutually exclusive.|
|$$P(A_1\cup A_2\cup\cdots)=\sum_i P(A_i)$$|Use for a finite/infinite sequence of **mutually exclusive** events.|
|If $A\subseteq B$, then<br><br>  <br><br>$$P(A)\le P(B)$$|Use when one event is contained in another.|
|$$P(A\cup B)=P(A)+P(B)-P(A\cap B)$$|General addition rule: use for “A or B” when events may overlap.|
|$$P(A\cap B)=P(A)+P(B)-P(A\cup B)$$|Rearranged addition rule: use when you know $P(A)$, $P(B)$, $P(A\cup B)$ and need the intersection.|

## **2. Sample-space / equally likely outcomes**

Used in the file’s examples:

  

$$P(A)=\sum_{s\in A}P(\{s\})$$

Use when the sample space is finite and you can add the probabilities of the sample points inside $A$.

  

If outcomes are equally likely:

  

$$P(A)=\frac{\vert{}A\vert{}}{\vert{}S\vert{}}$$

Use for coins, dice, cards, etc., when all outcomes are equally likely.

  

Counting examples from the file:

  

$$\text{Two coins: } \vert{}S\vert{}=2^2=4$$

$$\text{Three dice: } \vert{}S\vert{}=6^3=216$$

## **3. Conditional probability**

$$P(B\mid A)=\frac{P(A\cap B)}{P(A)},\qquad P(A)\ne 0$$

Use when you know $A$ has occurred and want the probability of $B$ given $A$.

  

Equivalent form:

  

$$P(A\mid B)=\frac{P(A\cap B)}{P(B)},\qquad P(B)\ne 0$$

Use when the condition is $B$.

  

## **4. Multiplication rule**

$$P(A\cap B)=P(A)\,P(B\mid A)$$

Use for the probability that **both** $A$ and $B$ occur, especially in sequential experiments.

  

Equivalent form:

  

$$P(A\cap B)=P(B)\,P(A\mid B)$$

Use when the conditional probability is given in the other direction.

  

## **5. Independent events**

Two events $A$ and $B$ are independent iff:

  

$$P(A\cap B)=P(A)\,P(B)$$

Use to **test independence** or to multiply probabilities when independence is known.

  

For independent events:

  

$$P(A\cap B)=P(A)P(B)$$

Use for repeated independent trials, e.g. coin tosses or die rolls.

  

## **6. Rule of total probability**

Special two-case form:

  

$$P(A)=P(A\cap B)+P(A\cap B')$$

$$P(A)=P(B)P(A\mid B)+P(B')P(A\mid B')$$

Use when event $A$ can happen through two mutually exclusive cases: $B$ and $B'$.

  

General form: if $B_1,B_2,\ldots,B_k$ form a partition of $S$ and $P(B_i)\ne0$, then:

  

$$P(A)=\sum_{i=1}^{k}P(A\cap B_i)$$

$$P(A)=\sum_{i=1}^{k}P(B_i)\,P(A\mid B_i)$$

Use when $A$ can occur through several mutually exclusive scenarios $B_1,\ldots,B_k$.

  

## **7. Bayes’ theorem**

If $B_1,\ldots,B_k$ partition $S$, $P(B_i)\ne0$, and $P(A)\ne0$, then:

  

$$ P(B_r\mid A) = \frac{P(B_r\cap A)}{P(A)} = \frac{P(B_r),P(A\mid B_r)} {\sum_{i=1}^{k}P(B_i),P(A\mid B_i)} $$

  

Use when you want to **reverse a conditional probability**: given that $A$ happened, find the probability that it came from cause/scenario $B_r$.

  

In the file’s disease example, this is used as:

  

$$P(\overline D\mid p) = \frac{P(\overline D)P(p\mid \overline D)} {P(D)P(p\mid D)+P(\overline D)P(p\mid \overline D)}$$

where $\overline D=D^c$ means “does not have the disease” and $p$ means “tests positive.”

  

## **8. Set/event notation used with Venn diagrams**

|**Notation**|**Meaning**|**Use**|
|---|---|---|
|$A\cup B$|union: $A$ or $B$ or both|“either/or” events|
|$A\cap B$|intersection: both $A$ and $B$|“and” events|
|$A^c$|complement: not $A$|“does not occur”|
|$A\cap B=\varnothing$|mutually exclusive|events cannot happen together|

## **Quick summary: which formula to use**

- **“A or B” with overlap:**
    
      
    
    $$P(A\cup B)=P(A)+P(B)-P(A\cap B)$$
    
- **“A or B” mutually exclusive:**
    
      
    
    $$P(A\cup B)=P(A)+P(B)$$
    
- **“not A” / “neither”:**
    
      
    
    $$P(A^c)=1-P(A)$$
    
- **“A and B” sequential:**
    
      
    
    $$P(A\cap B)=P(A)P(B\mid A)$$
    
- **Given $A$, find $B$:**
    
      
    
    $$P(B\mid A)=\frac{P(A\cap B)}{P(A)}$$
    
- **Test independence:**
    
      
    
    $$P(A\cap B)=P(A)P(B)$$
    
- **$A$ happens through cases $B_i$:**
    
      
    
    $$P(A)=\sum_i P(B_i)P(A\mid B_i)$$
    
- **Given $A$, find which cause $B_r$:**
    
    $$P(B_r\mid A)=\frac{P(B_r)P(A\mid B_r)}{\sum_i P(B_i)P(A\mid B_i)}$$



# CH3:

Below are **all probability/random-variable formulas shown in CH03**, separated into **general formulas** and **example-specific formulas**.

The file has some garbled OCR pages; I include only formulas that are clearly shown or clearly used.

# **A. General formulas and when to use them**

## **1. Discrete random variable and probability distribution**

### **Probability distribution**

$$f(x)=P(X=x)$$

**When to use:** For a **discrete** random variable $X$, to give the probability that $X$ equals a specific value $x$.

### **Conditions for a valid discrete probability distribution**

$$f(x)\ge 0$$

for every $x$ in the domain, and

$$\sum_x f(x)=1$$

**When to use:** To check whether a given function $f(x)$ can be a probability distribution.

### **Discrete cumulative distribution function (CDF)**

$$F(x)=P(X\le x)=\sum_{t\le x} f(t)$$

**When to use:** To find the probability that a discrete random variable is **at most** $x$, or to build the cumulative distribution.

### **Properties of a CDF**

$$F(-\infty)=0,\qquad F(\infty)=1$$

and if $a<b$, then

$$F(a)\le F(b)$$

**When to use:** To check whether a function can be a valid CDF. A CDF must go from 0 to 1 and be nondecreasing.

### **Recovering $f(x)$ from $F(x)$**

If the values are $x_1<x_2<\cdots<x_n$, then

$$f(x_1)=F(x_1)$$

and

$$f(x_i)=F(x_i)-F(x_{i-1}),\qquad i=2,3,\dots,n$$

**When to use:** When you are given a discrete CDF $F(x)$ and need the probability distribution $f(x)$.

## **2. Continuous random variable and probability density function**

### **Probability from a density**

$$P(a\le X\le b)=\int_a^b f(x)\,dx$$

**When to use:** For a **continuous** random variable with density $f(x)$, to find the probability that $X$ lies between $a$ and $b$. This is the area under the density curve.

### **Conditions for a valid probability density function**

$$f(x)\ge 0$$

for all real $x$, and

$$\int_{-\infty}^{\infty} f(x)\,dx=1$$

**When to use:** To check whether a function is a valid p.d.f., or to find an unknown constant $k$ in a density.

### **Continuous CDF**

$$F(x)=P(X\le x)=\int_{-\infty}^{x} f(t)\,dt$$

**When to use:** To find the cumulative probability for a continuous random variable, or to construct its CDF from its density.

### **Probability using the CDF**

$$P(a\le X\le b)=F(b)-F(a)$$

**When to use:** When you already have the CDF and want the probability of an interval.

### **Density from the CDF**

$$f(x)=\frac{dF(x)}{dx}$$

**When to use:** When you have $F(x)$ and need the density $f(x)$, where the derivative exists.

## **3. Mathematical expectation**

### **Expected value of a discrete random variable**

$$E(X)=\sum_x x\,f(x)$$

**When to use:** To find the long-run average / theoretical mean of a discrete random variable.

### **Expected value of a continuous random variable**

$$E(X)=\int_{-\infty}^{\infty} x\,f(x)\,dx$$

**When to use:** To find the mean of a continuous random variable from its density.

### **Expected value of $X^2$**

For a discrete random variable:

$$E(X^2)=\sum_x x^2 f(x)$$

For a continuous random variable:

$$E(X^2)=\int_{-\infty}^{\infty} x^2 f(x)\,dx$$

**When to use:** Needed to compute the variance using

$$\sigma^2=E(X^2)-[E(X)]^2$$

The file uses these forms in the variance examples.

## **4. Variance and standard deviation**

### **Variance**

$$\sigma^2=E(X^2)-[E(X)]^2$$

Equivalently, variance is the expected squared deviation from the mean.

**When to use:** To measure the spread/dispersion of a random variable around its mean.

### **Standard deviation**

$$\sigma=\sqrt{\sigma^2}$$

**When to use:** To express spread in the same units as $X$.

# **B. Example-specific formulas from the file**

These are formulas that appear inside particular examples. They are not general rules, but you may need them for the tutorial.

## **1. Four tosses of a balanced coin**

The random variable is

$$X=\text{total number of heads in 4 tosses}.$$

The file gives:

$$P(X=2)=\frac{6}{16}$$

$$P(X\ge 3)=P(X=3)+P(X=4)=\frac{4}{16}+\frac{1}{16}=\frac{5}{16}$$

**When to use:** For the specific example of four fair coin tosses and counting heads.

## **2. Sum of two fair dice**

Let

$$X=\text{sum of the two dice}.$$

Then

$$f(x)=\frac{6-\vert{}x-7\vert{}}{36},\qquad x=2,3,\dots,12$$

Examples:

$$P(X=7)=f(7)=\frac{6-\vert{}7-7\vert{}}{36}=\frac{6}{36}$$

$$P(X\ge 10)=f(10)+f(11)+f(12) =\frac{3}{36}+\frac{2}{36}+\frac{1}{36} =\frac{6}{36}$$

**When to use:** For the specific experiment of rolling two fair dice and letting $X$ be their sum.

## **3. Checking a discrete distribution**

$$f(x)=\frac{x+2}{25},\qquad x=1,2,3,4,5$$

The file checks:

$$f(1)+f(2)+f(3)+f(4)+f(5) =\frac{3}{25}+\frac{4}{25}+\frac{5}{25}+\frac{6}{25}+\frac{7}{25} =1$$

**When to use:** As an example of verifying the two conditions for a discrete probability distribution.

## **4. Continuous example: $f(x)=2x$ on $[0,1]$**

$$f(x)= \begin{cases} 2x, & 0\le x\le 1,\\ 0, & \text{otherwise}. \end{cases}$$

**Probability:**

  

$$P(0.2 < X \le 0.7) = \int_{0.2}^{0.7} 2x \, dx = \left[ x^2 \right]_{0.2}^{0.7} = 0.49 - 0.04 = 0.45$$

**Expected Value:**

  

$$E(X) = \int_0^1 x(2x) \, dx = 2 \int_0^1 x^2 \, dx = \frac{2}{3}$$

**Second Moment:**

  

$$E(X^2) = \int_0^1 x^2(2x) \, dx = 2 \int_0^1 x^3 \, dx = \frac{1}{2}$$

**Variance:**

  

$$\sigma^2 = E(X^2) - [E(X)]^2 = \frac{1}{2} - \left(\frac{2}{3}\right)^2 = \frac{1}{18}$$

**Standard Deviation:**

  

$$\sigma = \sqrt{\frac{1}{18}} \approx 0.2357$$

**When to use:** For this specific density example, and as a model for how to compute probabilities, mean, variance, and standard deviation for a continuous random variable.

  

## **5. Continuous Example: $f(x)=\frac{3}{16}(4-x^2)$ on $[0,2]$**

$$f(x)= \begin{cases} \frac{3}{16}(4-x^2), & 0 \le x \le 2, \\ 0, & \text{otherwise}. \end{cases}$$

**Probability:**

  

$$P(0 \le X \le 1) = \int_0^1 \frac{3}{16}(4-x^2) \, dx = \frac{11}{16}$$

$$P(X \ge 1) = 1 - P(X \le 1) = 1 - \frac{11}{16} = \frac{5}{16}$$

**CDF:**

  

$$F(x)= \begin{cases} 0, & x < 0, \\ \frac{3}{16}\left(4x - \frac{x^3}{3}\right), & 0 \le x \le 2, \\ 1, & x > 2. \end{cases}$$

**Using the CDF:**

  

$$P(X < 1) = F(1) = \frac{11}{16}$$

$$P(X \ge 1) = 1 - F(1) = \frac{5}{16}$$

$$P(0.5 < X < 1.5) = F(1.5) - F(0.5) = 0.9140625 - 0.3671875 = 0.546875$$

**When to use:** For this specific continuous density example and for practicing CDF calculations.

  

## **6. Finding $k$ in a Density**

$$f(x)= \begin{cases} k(4-x^2), & 0 \le x \le 2, \\ 0, & \text{otherwise}. \end{cases}$$

Use:

  

$$\int_0^2 k(4-x^2) \, dx = 1$$

The file computes:

  

$$\int_0^2 (4-x^2) \, dx = \left[ 4x - \frac{x^3}{3} \right]_0^2 = 8 - \frac{8}{3} = \frac{16}{3}$$

So:

  

$$k \cdot \frac{16}{3} = 1 \quad \Rightarrow \quad k = \frac{3}{16}$$

**When to use:** To determine an unknown normalizing constant so that a density integrates to 1.

  

## **7. Uniform Density Example**

$$f(x)= \begin{cases} 1, & 0 \le x \le 1, \\ 0, & \text{otherwise}. \end{cases}$$

The file illustrates:

  

$$E(X) = 0.5$$

**When to use:** As the simple uniform example on $[0,1]$.

  

## **8. Continuous “Accident on Freeway” Motivation**

For a 200-km freeway:

  

$$P(\text{accident on length } d) = \frac{d}{200}$$

$$P(\text{accident on } d_1 \text{ or } d_2) = \frac{d_1 + d_2}{200}$$

$$P(\text{accident on } d_1, d_2, d_3, \dots) = \frac{d_1 + d_2 + d_3 + \dots}{200}$$

**When to use:** As motivation for continuous probability: probability is proportional to length/area, and single points have probability 0.

# **C. Quick Summary: Which Formula to Use**

|**Goal**|**Formula**|
|---|---|
|**Discrete probability at $x$**|$f(x)=P(X=x)$|
|**Check discrete distribution**|$f(x)\ge0, \quad \sum_x f(x)=1$|
|**Discrete CDF**|$F(x)=\sum_{t\le x}f(t)$|
|**Get $f(x)$ from discrete $F(x)$**|$f(x_i)=F(x_i)-F(x_{i-1})$|
|**Continuous probability on interval**|$P(a\le X\le b)=\int_a^b f(x)\,dx$|
|**Check continuous density**|$f(x)\ge0, \quad \int_{-\infty}^{\infty}f(x)\,dx=1$|
|**Continuous CDF**|$F(x)=\int_{-\infty}^{x}f(t)\,dt$|
|**Probability from continuous CDF**|$P(a\le X\le b)=F(b)-F(a)$|
|**Density from CDF**|$f(x)=F'(x)$|
|**Mean, discrete**|$E(X)=\sum_x x f(x)$|
|**Mean, continuous**|$E(X)=\int_{-\infty}^{\infty}x f(x)\,dx$|
|**Variance**|$\sigma^2=E(X^2)-[E(X)]^2$|
|**Standard deviation**|$\sigma=\sqrt{\sigma^2}$|