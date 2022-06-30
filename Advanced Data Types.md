### Sequences (Lists)
`!!seq` here means sequence.

```
student: !!seq
 - marks
 - name
 - rol_no
```

We can also do something like

```
cities: [new delhi, mumbai, amritsar, gurdaspur]
```

We can also keep some of the keys of the *Seqeuence* **empty**. This is known as *Sparse Sequence* . 

```
- hey
- how
- 
- hello
- 

```

### Nested Sequence
```
- 
 - cool 
 - awesome
 - sexy
- 
 - bad
 - ugly
 - rugged
```

The `-`   with no value, specifies start of a new object.

### Maps i.e key: value pairs
we can use `!!map` data type

We can also define **Nested Mappings**. Map within a map.

```
name: Kunal Kushwaha
role:
 age: 22
 job: student
```

We can also do something like
```
name: Kunal Kushwaha
role: {age: 22, job: student}

```

### Pairs 
In `pairs`, keys may have duplicate values. 
`!!pairs` to declare this data type. 

```
pairExample: !!pairs
  - job: student
  - job: teacher
  
# This can also be seen as an array of hash tables
pairExamples: !!pairs [job: student, job: teacher]

```

### Sets
`Set` in YAML can be seen as an data structure containing unique keys only. 

```
names: !!set
 ? Kunal
 ? Apoorv
 ? Rahul
```

### Dictionary
`Dictionary` is used when you want to represent entire sequence as a *value*. This is represented by `!!omap`
```
people: !!omap
 - Kunal:
	 name: Kunal Kushwaha
	 age: 22 
 - Rahul: 
	 name: Rahul Sharma 
	 age: 23
```

## Anchors
When their some repeated properties over multiple declarations you can declare them in a single data structure and use them in your other declarations. 

So, basically which property / declaration you want to copy and where do you want to copy it. 

```
likings: &likes
	fav: mango
	notFav: grapes

person1: 
 name: Shubh
 <<: *likes	

```
`<<: *anchorName`   will copy paste all the properties represented by `anchorName`. To declare it use `&`. 
