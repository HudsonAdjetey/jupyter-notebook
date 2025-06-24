
---

### 🧪 Step 1: Create a Simple DataFrame

```python
import pandas as pd

df = pd.DataFrame({
    'name': ['Alice', 'Bob', 'Charlie', 'David', 'Eve']
})
print("Original DataFrame:")
print(df)
```

---

### 📍 Example 1: Sample 2 Rows (Fixed, Reproducible)

```python
print("\nSample 2 rows (with random_state=42):")
print(df.sample(n=2, random_state=42))
```

✅ This will always return the **same 2 rows**.

---

### 📍 Example 2: Sample 2 Rows (Random Each Time)

```python
print("\nSample 2 rows (random, no random_state):")
print(df.sample(n=2))
```

🔄 This will give **different rows each time** you run it.

---

### 📍 Example 3: Sample 50% of the Data

```python

print("\nSample 50% of the DataFrame:")
print(df.sample(frac=0.5, random_state=1))
```

💡 `frac=0.5` means "take 50% of the rows".

---

### 📍 Example 4: Sample With Replacement (Bootstrapping-style)

```python
print("\nSample 3 rows with replacement:")
print(df.sample(n=3, replace=True, random_state=0))
```

🔁 `replace=True` allows **duplicate rows**, useful for bootstrapping.


