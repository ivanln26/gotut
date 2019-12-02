# Golang

## Hello World

```golang
package main

import "fmt"

func main() {
    fmt.Println("Hola mundo")
}
```

## Variables

```golang
// var nombre tipo = valor
var x int = 10
const text string = "hello world" // constante
y := 100 // shot statement
```

### Tipos de variables

* Booleanos: bool
* Numericos:
    * int
    * uint
    * float32
    * float64
    * byte
* Cadena de texto: string

## Operadores

* == `igualacion`
* != `desigual`
* \> >= `mayor que / mayor o igual que`
* < <= `menor que / menor o igual que`
* && `y`
* || `o`

## Funciones

```golang
package main

import "fmt"

// func nombre(parametro tipo[, ...]) tipo_retorno { ... }
func add(x int, y int) int {
    return x + y
}

func main() {
    fmt.Println(add(10, 5))
}
```

## Condicionales

### If / else

```golang
if "A" == "B" {
    return "Son iguales"
} else {
    return "Son distintos"
}
```

### Switch

```golang
package main

import (
	"fmt"
	"time"
)

func main() {
	fmt.Println("Cuando es sabado?")
	today := time.Now().Weekday()
	switch time.Saturday {
	case today + 0:
		fmt.Println("Hoy.")
	case today + 1:
		fmt.Println("Manana.")
	case today + 2:
		fmt.Println("En dos dias.")
	default:
		fmt.Println("Falta mucho.")
	}
}
```


## Loops

### For

```golang
for i := 0; i < 10; i++ {
    fmt.Println(i)
}
```

### While

```golang
i := 0

for i < 100 {
    i++
}
```

### Forever

```golang
for {
    // ...
}
```

## Pointers

```golang
package main

import "fmt"

func main() {
    i := 10
    j := &i

    fmt.Println(j)
    fmt.Println(*j)
    *j = 5
    fmt.Println(i)
}
```
