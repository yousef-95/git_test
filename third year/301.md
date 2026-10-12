## Big_Omega :
**Goal:** Find a "Floor." You need to prove that **f(n)≥c⋅g(n)**
#### 💡 Hint 1: The "Positive Term" Shortcut
If **f(n)** contains only **positive** terms (e.g., f(n)=5n2+3n+10), the function is already "pushed up."

- **The Trick:** Pick **c** to be the **leading coefficient** (the number in front of the fastest-growing term).
- **Example:** For **f(n)=5n2+3n+10**, pick **c=5**
- **Result:** **n0** will almost always be **1**.

#### 💡 Hint 2: The "Negative Term" Adjustment

If

```
f(n)f(n)
```

has a **negative** term (e.g.,

```
f(n)=5n2−10f(n)=5n2−10
```

), the function is being "pulled down." If you pick

```
c=5c=5
```

, the

```
−10−10
```

will make the inequality false.

- **The Trick:** Pick
    
    ```
    cc
    ```
    
    to be **slightly smaller** than the leading coefficient.
    
- **Example:** For
    
    ```
    f(n)=5n2−10f(n)=5n2−10
    ```
    
    , don't pick
    
    ```
    55
    ```
    
    . Pick**
    
    ```
    c=4c=4
    ```
    
    **or**
    
    ```
    c=1c=1
    ```
    
    **.
    
- **Result:** This "gives room" for the subtraction. You will then solve the algebra to find
    
    ```
    n0n0​
    ```
    
    .
    

#### 💡 Hint 3: The "Safe Bet"

If you are completely stuck and cannot find

```
cc
```

:

- **The Trick:** Pick a very small positive number, like
    
    **`c=1c=1`**
    
    or**
    
    ```
    c=110c=101​
    ```
    
    **.
    
- **Why?** A very small
    
    ```
    cc
    ```
    
    creates a very low floor. It is much easier for
    
    ```
    f(n)f(n)
    ```
    
    to stay above a tiny number than a large one.