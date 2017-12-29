# Language comparison

## Introduction

Here I keep some snippets divided by argument of the language I'm using (Javascript and Python at the moment).

Choose a content, a topic and see the solution implemented in Javascript and Python.

## <a name="anchorContents"></a>Contents
* [Data types](#anchorDataTypes)
* [Logical operators](#anchorLogicalOperators)
* [Control structures](#anchorControlStructures)
	* [If](#anchorIf)
	* [For](#anchorFor)
	* [While](#anchorWhile)
	* [Switch](#anchorSwitch)
* [Array](#anchorArray)
	* [Length](#anchorLength)
	* [Add items](#anchorAdd)
	* [Extract items](#anchorExtract)
	* [Update items](#anchorUpdate)
	* [Remove items](#anchorRemove)
	* [Concatenate and join](#anchorConcatenate)	
	* [Sort and reverse](#anchorSort)	
	* [Find elements](#anchorFind)		
	* [Filter, map and reduce](#anchorFilter)
	* [All, fill, unique](#anchorAll)


### <a name="anchorDataTypes"></a>Data types [^](#anchorContents)

Tipo | Javascript	|	Python | Notes 
---- | ----------- | --------- | ----
Boolean	|	true, false	| True, False	|
Int  | Number(x)            | Int(x)	|	JS: Always 64bit FP. NaN is a number
Long | Number(x)				| long(x) | Python: Only in Python 2.x
Float| Number(x)				| float(x) | 
Complex | math.complex(x)			| complex(x) | 
String | String(x)			|str(x)		| Python: Unicode in Python 3x
Byte | n/a				| bytes(x)  | Python: Only in Python 2.x
Byte array | n/a		| 	bytearray(x) | Python: Only in Python 3.x
Array| Object			| list(x) 	|
Tuple| n/a				| tuple(x) 	|
Set	|  n/a				| set(x) 	|
Frozenset	| n/a			|	frozenset(x) |
Hasmap		| Object			|	dict(x)		|
Null		| null		|	n/a
Undefined	| undefined	|	n/a			

### <a name="anchorLogicalOperators"></a>Data types [^](#anchorContents)

Tipo | Javascript	|	Python | Notes 
---- | ----------- | --------- | ----
Equal			| ==, ===		| == 		| JS: === checks also the type
Not equal 		| !=, !==	| !=, <> 	| JS: !== check also the type
Greater (than)	| >, >=		| >, >=		|
Lesser (than)	| <. <=		| <, <=		|
Contained		| Y.indexOf(X) > -1			| X in Y	|
And				| &&		| and		|
Or				| \|\|		| or		|
Not				| !		| not		|
Bitwise xor		| ( X \|\| Y ) && !( X && Y ) )		| ^			| X or Y but not Y and Y
Ternary			| var x = (cond) ? if_true : if_false	|	x = if_true if (cond) else if_false 	

### <a name="anchorControlStructures"></a>Control structures [^](#anchorContents)

#### <a name="anchorIf">If  [^](#anchorContents)

	//	Javascript
	
	if (cond) {
  		// ...
	} else if (cond2) {
  		// do something
	} else {
  		// ...
  	}
	
	# Python
	
	if (cond):
    	pass
	elif (cond2):
    	pass
	else:
		pass
		
	v = X if (cond) else Y	# If on one line;
	
	
#### <a name="anchorFor">For  [^](#anchorContents)

	// Javascript
	
	for (X = 0; X < 10; X += 1) {
  		// ...
	}
	
	for (element in object) {		// Alternative form
  		// ... 	
	}

	# Python
	
	for X in Y :
    	pass
	else:
    	pass
    
#### <a name="anchorWhile">While  [^](#anchorContents)

	// Javascript
	
	while (cond) {
  		// ...
	}
	
	do {					// do
		// ...
	} while (cond);
	
	# Python
	
	while test:
    	pass
	else:
    	pass

#### <a name="anchorSwitch">Switch  [^](#anchorContents)

	// Javascript
	
	switch(cond) {
		case val1:
			// ...
		case val2:
			// ...
		case val3:
  			// ...
  			break;
		default:
  			// ...
  			break;
	}
	
	# Python
	 
	n/a

### <a name="anchorArray"></a>Array [^](#anchorContents)

#### <a name="anchorLength">Length  [^](#anchorContents)

	// Javascript
	a.length
	
	# Python
	len(a)

#### <a name="anchorAdd">Add items [^](#anchorContents)
	
	// Javascript
	
	a.push(item1, item2, item3, ..., itemN)		// Add at the end. The original is modified.
	a.unshift(item1, item2, item3, ..., itemN) 	// Add at the beginning. The original is modified
	a.splice(start_position, 0, item1, ..., itemN) 	// Insert elements at a position. The original is modified

	# Python
	
	a.append(Item)	# Add at the end. The original is modified
	a.insert(0,Item)	# Add at the beginning. The original is modified
	a.insert(pos,Item) # Insert element at a position
	
#### <a name="anchorExtract">Extract items [^](#anchorContents)

	// Javascript
	
	a[x] // Extract element at position X, zero based
	a.slice(start, end) 	// Extract elements. The original is not modified
	a.slice(0,N)			// Extract first N elements. The original is not modified
	a.slice(-N)				// Extract the last N elements. The original is not modified
	
	# Python
	
	a[x]			# Extract element at position X, zero based
	a[start, end]	# Extract elements. The original is not modified
	a[:N]			# Extract the first N elements. The original is not modified
	a[-N:]  		# Extract the first N elements. The original is not modified
	
#### <a name="anchorUpdate">Update items  [^](#anchorContents)

	// Javascript
	
	a[N] = value	// Update item of position N
	
	# Python 
	
	a[N] = value   // Update item of position N
	
#### <a name="anchorRemove">Remove items [^](#anchorContents)
	
	// Javascript
	
	a.pop()			// Remove and return last item. The original is modified
	a.shift() 		// Remove and return first item. The original is modified
	a.splice(B, 1) 	// Remove item of position N. The original is modified.
	
	# Python
	
	del a[-1]	// Remove last item. The original is modified
	del a[0]	// Remove first item. The original is modified.
	del a[N]	// Remove item of position N. The original is modified.
	
#### <a name="anchorConcatenate">Concatenate and join [^](#anchorContents)
	
	// Javascript
	
	a.concat(arrB) 			// The original is modified
	a.join(separator) 		// The original is not modified
	
	# Python
	
	a + b					# The original is not modified
	'separator'.join(a)		# The original is not modified
	
#### <a name="anchorSort">Sort and reverse [^](#anchorContents)

	// Javascript 
	
	a.sort(function(x,y)()) // The original is modified. Number first, then letters
	a.reverse()		// The original is modified
	
	# Python
	
	a.sort(key=function)	# The original is not modified	a[::-1] 		# The original is not modified

#### <a name="anchorFind">Find elements [^](#anchorContents)

	// Javascript
	a.indexOf(item)	// Returns the first position of the element, -1 if it not exists
	a.find(function(){}) // Returns the value of the first element that satisfies the test
	a.findIndex(function(){}) // Returns the value of the index of the first element that satisfies the test
	
	# Python
	
	a.index(item)	# Returns the firs position of the element, ValueError if it not exists
	filter(function, a)[0] # Returns the value of the first element that satisfies the test
	
#### <a name="anchorFilter">Filter, map and reduce [^](#anchorContents)

	// Javascript
	a.filter(function(x){}) // The original is not modified
	a.map(function(x){})	// The original is not modified
	a.reduce(function(x,y))		// The original is notmodified
	
	# Python
	filter(function, a)		# The original is not modified
	map(function, a)		# The original is not modified
	reduce(function(x,y),a)		# The original is not modified

#### <a name="anchorAll">All, fill and unique  [^](#anchorContents)

	// Javascript
	
	a.every(function(x){}) // Returns True if all the elements pass the test, otherwise return false
	a.fill(element,start,end) // The original array is modified
	a.filter((x, i, y) => y.indexOf(x) == i)	// The original array is not modified

	# Python
	
	all(condition_on_item for item in a)	# Return True if all the elements pass the test, otherwise return false
	a[start,end] = [element for _ in range(end-start)]
	set(a)	# The original is not modified
	
