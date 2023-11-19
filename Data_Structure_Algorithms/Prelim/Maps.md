- A `map` is a *set of ordered pairs* where *elements* are known as *keys* `(identifiers)` and *values* `(content)`.
	- A `map` *cannot contain* duplicate `keys`
	- Each `key` can `map` to only *one* `1` *value*
- `Example` *(A map of first names)*

| `Key` | `Value` |
| --- | --- |
| `N` | **Nika** |
| `K` | **Kae** |
| `M1` | **Mark** |
| `M2` | **Mairo** |

##### Java

- There are *three* `3` general-purpose `map` *implementations* in `Java:` `HashMap`, `TreeMap`, `LinkedHashMap`.
- To *create* an `empty map`:
```java
Map <String, String> nameMap = new HashMap<>();
```

- To *insert* a `mapping`:
```java
nameMap.put("M1", "Mark");
nameMap.put("M2", "Mairo");
```

- To *delete* the `mapping` for a `key`:
```java
nameMap.remove("M2");
```

- To *replace* a `key's value`:
```java
nameMap.replace("M2", "Marco");
```

- To *retrieve* the `value` based on the `key`:
```java
System.out.println(nameMap.get("M1"));
```

- To *check* whether a map *contains* a `mapping` for the *specified* `key` or `value`:
```java
System.out.println(nameMap.containsKey("M2"));
System.out.println(nameMap.containsValue("Mark"));
```

- To *retrieve* all the `keys` and `values` of a `map`:
```java
System.out.println(nameMap.keySet());
System.out.println(nameMap.values());
```

- To *display* entries in separate lines:
```java
for (Map.Entry e: nameMap.entrySet()) {
	System.out.println(e.getKey()+": "+e.getValue());
}
// Map.Entry is an interface to  retrieve entries
```

##### Python
- `Maps` in `Python` are known as *dictionaries*. To *create* `dictionary`, use the colon symbol `:` for *key-value pairs* within the `curly braces`.

- To *create* an `empty dictionary`:
```python
name_map = { }
```

- To *initialize* a `dictionary`:
```python
name_map = {"M1": "Mark", "M2": "Mairo"}
```

- To *insert* a `mapping`:
```python
name_map["N"] = "Nika"
```

- To *delete* the `mapping` for a `key`:
```python
del name_map["M2"]
```

- To *replace* a `key's value`:
```python
name_map["M2"] = "Marco"
```

- To *retrieve* the `value` based on the `key`:
```python
print(name_map["M1"])
```

- To *check* whether a `dictionary` contains a `mapping` for the `specified key`:
```python
print("M2" in name_map)
```

- To *retrieve* all the `keys` and `values` of a `dictionary`:
```python
print(list(name_map))
print(list(name_map.value()))
```

- To *display* entries in separate lines:
```python
for x, y in name_map.items():
	print(x, y)
```