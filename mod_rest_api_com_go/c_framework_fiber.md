# Introdução ao Framework Fiber em Go
O Fiber é um framework web desenvolvido em Go (também conhecido como Golang), que se destaca por suas características de
alto desempenho, baixa alocação de memória e uma sintaxe elegante e concisa. Desse tópico em diante haverão exemplos de
código em Go & Fiber, assim sendo, para manter esse modulo ágil recomendamos:

> ### Padrão de leitura para código Go & Fiber 
> - **Leia o tópico por inteiro.**
> - **Em caso de dúvida sobre ...:**
>   - `Concorrência` e/ou paralelismo:
>     1. Tente abstrair a assíncronia aplicada e focar no motivo por trás dela.
>     2. Peça ajuda de um colega do time de projetos.
>   - `Sintaxe` e/ou semântica do `Go`:
>     1. Tente [rodar](https://go.dev/play/) o código em questão e contextualizar os resultados.
>     2. Marque os termos que mais geram dúvida e busque-os no [Go by example](https://gobyexample.com).
>     3. Pratique alguns [exercícios de Go](https://exercism.org/tracks/go/concepts).
>     4. Peça ajuda a um colega do time de projetos.
>   - Sintaxe e/ou `semântica` do `Fiber`:
>     1. Busque os termos chave nas tabelas auxiliares.
>     2. Veja o [guia do Fiber](https://docs.gofiber.io/category/guide).
>     3. Peça ajuda a um colega do time de projetos.

## Porque Go & Fiber?
### "Simples e Compacto!"
O Fiber, assim como o Go, tem certa similaridade com um canivete, eles fornecem um grande conjunto de funcionalidades 
comprimidas no menor escopo viável. Sendo mais objetivo, existem melhores soluções para cada aspecto específico da 
stack Go & Fiber, porém nenhum outro conjunto de tecnologias do mercado consegue ser tão amplo e continuar simples.

### Contexto Leve e Rápido
O contexto (context) é uma parte crucial no Fiber para lidar com requisições HTTP de forma eficiente. Ele é usado para 
passar informações e valores entre middlewares e handlers (tratadores). Vamos criar um exemplo de como usar o contexto 
no Fiber:

```go
package main

import (
	"fmt"
	"github.com/gofiber/fiber/v2"
)

func main() {
	app := fiber.New()

	// Rota de exemplo que utiliza o contexto
	app.Get("/hello", func(c *fiber.Ctx) error {
		// Escreve uma resposta com base em dados do contexto
		return c.SendString("Hello, " + c.Query("name"))
	})

	app.Listen(3000)
}
```

Neste exemplo, criamos uma rota "/hello" que usa o contexto para receber o parâmetro "name" da consulta (query) e o 
incorpora na resposta.

### Suporte a Middleware Funcional
O Fiber oferece a flexibilidade de usar middlewares funcionais, o que permite uma maneira diferente de implementar 
middlewares. Vamos criar um exemplo de middleware funcional para autenticação simples:

```go
package main

import (
	"fmt"
	"github.com/gofiber/fiber/v2"
)

func logger(next fiber.Handler) fiber.Handler {
	return func(c *fiber.Ctx) error {
		fmt.Println("Antes da rota")
		err := next(c)
		fmt.Println("Depois da rota")
		return err
	}
}

func main() {
	app := fiber.New()

	// Middleware funcional para log
	app.Use(logger)

	// Rota de exemplo
	app.Get("/", func(c *fiber.Ctx) error {
		return c.SendString("Hello, World!")
	})

	app.Listen(3000)
}
```

Neste exemplo, criamos um middleware funcional chamado "logger" que imprime mensagens antes e depois do tratamento da 
rota. O middleware é aplicado a todas as rotas usando `app.Use(logger)`.

## Conclusão
O Fiber é uma escolha poderosa e eficaz para desenvolvedores que buscam um framework web em Go que combine alto 
desempenho, baixo consumo de memória e uma sintaxe elegante. Com suas características distintas, como roteamento 
eficiente, suporte a middleware flexível e contexto leve, o Fiber se destaca como uma excelente opção para o 
desenvolvimento de aplicativos web escaláveis e de alto desempenho em Go.