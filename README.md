# LEETCODE-Strings-2211
```
directions = "RLRSLL"
Index:        0 1 2 3 4 5
Characters:   R L R S L L
```

---

# ✅ **Step-by-Step Dry Run**

## **Initial Values**

```
n = 6
i = 0
j = 5
```

---

# **Step 1: Move `i` forward while directions[i] == 'L'**

The loop:

```java
while(i<n && directions.charAt(i)=='L')
```

Check each:

* i = 0 → char = 'R' → NOT 'L' → loop stops.

So:

```
i = 0
```

---

# **Step 2: Move `j` backward while directions[j] == 'R'**

The loop:

```java
while(j>=0 && directions.charAt(j)=='R')
```

Check each:

* j = 5 → char = 'L' → NOT 'R' → loop stops.

So:

```
j = 5
```

---

# **Step 3: Count collisions from i to j**

Logic:

```java
while(i <= j) {
    if(directions.charAt(i) != 'S')
        collisions++;
    i++;
}
```

We iterate from index **0 to 5**.

| i | char | char != 'S'? | collisions |
| - | ---- | ------------ | ---------- |
| 0 | R    | yes          | 1          |
| 1 | L    | yes          | 2          |
| 2 | R    | yes          | 3          |
| 3 | S    | no           | 3          |
| 4 | L    | yes          | 4          |
| 5 | L    | yes          | 5          |

Final:

```
i = 6 (> j)
```

Loop ends.

---

# ✅ **Final Answer**

```
collisions = 5
```

---
