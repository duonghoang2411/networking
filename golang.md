GOLANG SYNTAX
==================
Syntax - Defined - Variable types
----------
### Variable types
- `bool`

- `string`

- `int  int8  int16  int32  int64`
- `uint uint8 uint16 uint32 uint64 uintptr`

- `byte` // alias for uint8

- `rune` // alias for int32

- `float32 float64`

- `complex64 complex128` ????

### Defined syntax
- `variableName variableType`
- `variableName variableType = value`

### Syntax
- Forget `;` in code ? it okay, golang don't need it
- Import
```
import "fmt"
//or
import(
    "fmt"
    "math"
)
```

What golang can do ?
----

### Multiple Results

```
func swap(x, y string) (string, string) {
	return y, x
}

func main() {
	a, b := swap("hello", "world")
	fmt.Println(a, b)
}
```

### Named return values

```
func split(sum int) (x, y int) {
	x = sum * 4 / 9
	y = sum - x
	return
}

func main() {
	fmt.Println(split(17))
}
```
### Variable default value

- If one variable had declare without value, it will had a default value 
```
func main() {
	var i int
	var j float32
	var c bool
	fmt.Println(i, j)
}
```
- Result: `0 0 false`

### Variable init

- Much variable can init value in one line with different value
```
var i, j int = 1, 2

func main() {
	var c, python, java = true, false, "no!"
	fmt.Println(i, j, c, python, java)
}
```
- Result: `1 2 true false no`

### Short variable declarations

- Like python, variable in golang no need a type to declare
```
func main() {
	k := 3
	fmt.Println(k)
}
```
- Result: `3` and k now is `int`

### Get type and value

var (
	ToBe   bool       = false
	MaxInt uint64     = 1<<64 - 1
	z      complex128 = cmplx.Sqrt(-5 + 12i)
)

func main() {
	fmt.Printf("Type: %T Value: %v\n", ToBe, ToBe)
	fmt.Printf("Type: %T Value: %v\n", MaxInt, MaxInt)
	fmt.Printf("Type: %T Value: %v\n", z, z)
}
- Result
```
Type: bool Value: false
Type: uint64 Value: 18446744073709551615
Type: complex128 Value: (2+3i)
```

Basic syntax
------------

### Type convert


```
func main() {
	var x, y int = 3, 4
	var f float64 = math.Sqrt(float64(x*x + y*y)) // value float
	var z uint = uint(f) // not it unsigned int
	fmt.Println(x, y, z)
}
```
- Result: `3 4 5`

### Constants


```
const Pi = 3.14

func main() {
	const World = "世界"
	fmt.Println("Hello", World)
	fmt.Println("Happy", Pi, "Day")

	const Truth = true
	fmt.Println("Go rules?", Truth)
}
```
- Result
```
Hello 世界
Happy 3.14 Day
Go rules? true
```
 Keyword
--------------

```
break        default      func         interface    select
case         defer        go           map          struct
chan         else         goto         package      switch
const        fallthrough  if           range        type
continue     for          import       return       var
```

 Operators and punctuation
------
```
+    &     +=    &=     &&    ==    !=    (    )
-    |     -=    |=     ||    <     <=    [    ]
*    ^     *=    ^=     <-    >     >=    {    }
/    <<    /=    <<=    ++    =     :=    ,    ;
%    >>    %=    >>=    --    !     ...   .    :
     &^          &^=
```
