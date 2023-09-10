# Método GET com Fiber
Pela importância do método GET, é válido mostrar aqui como implementa-lo usando Go & Fiber. Segue então um exemplo de 
código para servir um "hello, world!".

## Implementação & Teste
Primeiro, você precisa garantir que o Fiber esteja instalado em seu ambiente Go. Você pode fazer isso usando o seguinte comando:
```bash
go get github.com/gofiber/fiber/v2
```

Aqui está um exemplo de código que cria um servidor web básico com um endpoint GET usando o Fiber:
```go
package main

import (
	"log"
	"github.com/gofiber/fiber/v2"
)

func main() {
	// Cria uma nova instância do Fiber 
	app := fiber.New()
  
	// Configura a rota GET `/hello` 
	app.Get("/hello", func (c *fiber.Ctx) error {
		return c.SendString("Hello, World!")
	})

    // Pede para o app observar a porta 3000 e 
    // armazena em status o resultado
	status := app.Listen(":3000")
	
	// Imprime na tela o status do app e encerra o programa
	log.Fatal(status)
}
```

Neste exemplo, estamos importando o Fiber, criando uma instância do aplicativo `fiber` e definindo um handler para o
endpoint GET "/hello". Quando alguém acessa "/hello" no navegador ou faz uma solicitação GET para esse endpoint, o
servidor responde com a mensagem "Hello, World!".

Para executar o exemplo, você pode salvar o código em um arquivo chamado `main.go` e, em seguida, executar:
```bash
go run main.go
```

Se tudo estiver configurado corretamente, você poderá acessar `http://localhost:3000/hello` em seu navegador e ver a
resposta "Hello, World!" retornada.
