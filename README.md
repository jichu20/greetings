# Saludos en Go

Este paquete proporciona una forma simple de obtener saludos personalizados en Go.

## Instlaación 
Ejecute el siguiente comando para instalar el paquete:

```sh 
go get -u github.com/jichu20/greetings
```

## Uso 

Aquí tienes un ejemplo de como utilizar el paquete en tu código 

```go

package main

import (
	"fmt"
	"log"

	"github.com/jichu20/greetings"
)

func main() {

	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	message, err := greetings.Hello("Borja")
	if err != nil {
		log.Fatal(err)
	}

	fmt.Println(message)

	names := []string{"Borja", "Javier", "Jorge"}
	messages, err := greetings.Hellos(names)

	for _, saludos := range messages {
		fmt.Println(saludos)
	}
}

```