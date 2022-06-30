### Where is YAML used? 
- Configuraton files
- Log files
- Caches

#### Benefits of using YAML? 
1. Its very simple and easy to read. 
2. It has a strict syntax. For example: Indentation is important. 
3. Easily convertable to JSON, XML. 
4. Most programming languages have a support for YAML. 
5. More powerful when representing complex data. 
6. Parsing is easy for YAML files. 


- YAML is Case Sensitive. 
- YAML can be a collection of 3 or more documents. use `---` to differentiate between different objects.
- `...`  used to mark the end of the document.


#### Variable declaration
-  Example : 
	`myself: Shubh Karman Singh`
	`fruit: "apple"`
	`job: 'swe'`
All the above declarations can be seen as variable declarations in YAML. We are storing strings here 

Note you have to write the whole sentence in one line if you have a large sentence. 

#### Adding a Multi Line variable
```
bio: Hello this is awesome.
How are you doing 
```
The above **example** will show an error. 
In order to preserve new lines and tabs and stuff. Add `|` in front of the variable declaration. 

For Example: 
```
Bio: | 
This is awesome. My name is Shubh Karman Singh. 
I am a programmer
```

### Adding a Multi Line Declaration to single line.
If you want to specify that the words written in multiple lines later are to be considered as a single sentence, use `>`. 

```
Bio: > 
This is awesome. 
My name is 
Shubh Karman Singh. 
I am 
a 
programmer
```

#### Data Types in YAML
`YAML`automatically detects the data type you declared as a value. But we can explicitly specify the data type as well. 

```
number: 3432
marks: 56.33
booleanVal: No # we can also use: n, N, false, False, FALSE. 
#Same for true -> yes, y, Y, True, TRUE
```

##### Specifying a type
**INT**
```
positiveNum: !!int 45
binNum: !!int 0b11011
octalNum: !!int 034353
Hexadecimal: !!0x3435
commaVal: +540_000 # its same as writing 540,000
exponentialNum: 6.023E56 

# We can also write something like not a number

notANum: .nan 
```

**STR/BOOL**
```
boolVal: !!bool No
stringVal: !!str Hello
```

**NULL**

```
Surname: !!null Null # null or NULL or ~
```

You can also add a *data and time* in YAML as well. If no timeZone added YAML assumes the time/date added to be **UTC**. 

**Date and Time**

```

date: !!timestamp 2002-12-14
indiaTime: 2001-12-15T02:59:43 +5:30

```

