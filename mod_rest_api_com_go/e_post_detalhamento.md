# Método POST com Fiber
Pela importância do método POST, é válido mostrar aqui como implementa-lo usando Go & Fiber. Segue então um exemplo de
código para receber um dado qualquer no formato string e retornar "Dados recebidos: <Dado enviado>".

## Implementação
O método POST é usado para enviar dados ao servidor para que ele possa ser processado ou armazenado. No contexto do 
framework Fiber, você pode criar endpoints POST para receber dados de clientes, como formulários da web, aplicativos 
móveis ou qualquer outra fonte de entrada. Aqui está como você pode implementar um endpoint POST em um aplicativo Fiber:

```go
package main

import (
	"github.com/gofiber/fiber/v2"
)

func main() {
	// Crie uma instância do Fiber
	app := fiber.New()

	// Defina um handler para o endpoint POST "/submit"
	app.Post("/submit", func(c *fiber.Ctx) error {
		// Obtenha os dados enviados pelo cliente
		data := c.FormValue("dados")

		// Faça algo com os dados (por exemplo, armazene em um banco de dados)
		// Neste exemplo, apenas retornaremos os dados recebidos
		return c.SendString("Dados recebidos: " + data)
	})

	// Inicie o servidor na porta 3000
	err := app.Listen(":3000")
	if err != nil {
		panic(err)
	}
}
```

Neste exemplo, criamos um endpoint POST em "/submit". Quando um cliente faz uma solicitação POST para este endpoint, o 
servidor Fiber recebe os dados enviados pelo cliente usando `c.FormValue("dados")`. Você pode acessar esses dados e 
realizar ações como armazená-los em um banco de dados ou processá-los de acordo com as necessidades do seu aplicativo.

Em seguida, o servidor responde ao cliente com uma mensagem que inclui os dados recebidos. Este é apenas um exemplo 
simples, e na prática, você pode executar tarefas mais complexas com os dados recebidos em um endpoint POST, como 
validação, autenticação e muito mais.

Lembre-se de que, ao criar um endpoint POST, você deve configurar os cabeçalhos e o corpo da solicitação do cliente 
corretamente para que os dados sejam enviados ao servidor Fiber.

# Teste
Para testar o código do servidor Fiber que implementa um endpoint POST, você pode usar uma ferramenta como o `curl` ou 
um cliente HTTP em Go, como o `http.Client`. Aqui está um exemplo de como você pode testar o código com o `curl`:

Suponha que você tenha o código do servidor Fiber que mencionei anteriormente em um arquivo chamado `main.go`. Primeiro,
certifique-se de que o servidor esteja em execução:

```bash
go run main.go
```

Agora, você pode usar o `curl` para enviar uma solicitação POST para o endpoint "/submit". Abra um terminal e execute o 
seguinte comando:

```bash
curl -X POST http://localhost:3000/submit -d "dados=MeusDadosAqui"
```

Neste exemplo, estamos usando o `curl` para enviar uma solicitação POST para o servidor em execução em 
`http://localhost:3000/submit`. O parâmetro `-d` é usado para especificar os dados que você deseja enviar. No caso, 
estamos enviando "dados=MeusDadosAqui" como dados de exemplo.

Após executar o comando `curl`, você deve receber uma resposta do servidor Fiber que inclui os dados que você enviou. A 
resposta será exibida no terminal.

Você pode ajustar os dados enviados e os parâmetros da solicitação POST conforme necessário para testar diferentes 
cenários ou tipos de dados. Além disso, se você estiver desenvolvendo um aplicativo cliente em Go, pode usar o pacote `net/http` para enviar solicitações POST programaticamente em vez do `curl`.