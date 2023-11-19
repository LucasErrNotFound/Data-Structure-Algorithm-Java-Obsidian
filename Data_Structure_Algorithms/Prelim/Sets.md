- A `set` is a *collection of elements* where each element is *unique*.
	- **Union** - The *union of two sets* `(A ∪ B)` is the set that *contains all the elements* in either set.
		- `{1, 3, 5, 7} U {2, 3, 4, 5} = {1, 2, 3, 4, 5, 7}`
	- **Intersection** = The *intersection of two sets* `(A ∩ B)` is the set that *contains only the elements common* to both sets.
		- `{1, 3, 5, 7} ∩ {2, 3, 4, 5} = {3, 5}`
	- **Difference** - The *difference of sets A and B* `(A - B)` is the set that *contains the elements* that are in `A` but not in `B`.
		- `{1, 3, 5, 7} - {2, 3, 4, 5} = {1, 7}`
	- **Subset** - *set* `A` is a subset of *set* `B` `(A ⊂ B)` if *every element of set* `A` is also an element of *set* `B`.
		- `{1, 3, 5, 7} ⊆ {1, 2, 3, 4, 5, 7} = true` **subset**
		- `{1, 3, 5, 7} ⊂ {1, 2, 3, 4, 5, 7} = true` **proper/strict subset**
		- This have multiple answer btw...
- `Java` contains *three* `3` general-purpose set implementations.
	- `HashSet` - This *stores its elements* in a *hash table* without a guaranteed order upon iteration. This is the *best-performing implementation*.
	- `TreeSet` - This *stores its elements* in a *special type of tree* where *elements are sorted* `(natural or custom)` during iteration.
	- `LinkedHashSet` - This *stores its elements* in a *hash table with a linked list* running through it. The order of the elements during iteration *is the same as the order they were inserted* into the set.
- To create an *empty set*:
```java
Set A = new HashSet();
Set A = new TreeSet();
Set C = new LinkedHashSet();
```

- To *add* items to the `set`:
```java
Collections.addAll(a, "Mark", "Nika", "Mairo", "Kae");
// Equivalent to multiple use of add()
```

- To *determine* the `union`, `intersection`, and `difference`:
```java
Set A = new HashSet();
Set A = new TreeSet();

Collections.addAll(A, "Mark", "Nika", "Mairo", "Kae");
Collections.addAll(B, "John", "Marco", "Mark");

Set union = new HashSet(A);
Set intersection = new HashSet(A);
Set difference = new HashSet(A);

union.addAll(B);
intersection.retainAll(B);
difference.removeAll(B);

System.out.println("Union: "+union);
System.out.println("Intersection: "+intersection);
System.out.println("Difference: "+difference);
```

- To *determine* whether a `set` is a `subset` of another `set`:
```java
System.out.println(A.containsAll(B));
```

- `Curly Braces` or the `set()` *function* can be used to *implement* `sets` in `Python`.
- To *create* an `empty set`:
```python
A = set()
```

- To *initialize* a `set`:
```python
A = set(["Mark", "Nika", "Mairo", "Kae"])
B = {"John", "Marco", "Mark"}
# Equivalent to multiple use of add()
```

- To *determine* the `union`, `intersection`, and `difference`:
```python
A = set(["Mark", "Nika", "Mairo", "Kae"])
B = {"John", "Marco", "Mark"}

print("Union: "+str(A | B))
print("Intersection: "+str(A & B))
print("Difference: "+str(A - B))
```

- To *determine* whether a `set` is a `subset` of another `set`:
```python
print(A.issubset(B))
```