# GoLang Introdução
## Oque é GoLang?
GoLang, ou simplesmente Go, é uma linguagem de programação de código aberto desenvolvida pelo Google. Ela é conhecida 
por sua simplicidade, eficiência e suporte à concorrência, tornando-a ideal para o desenvolvimento de software escalável
e de alto desempenho.

## Simples, Segura e Performática
- **Simples:** GoLang foi projetada com uma sintaxe simples e intuitiva que facilita a leitura e a manutenção do 
código. Isso torna a linguagem acessível a desenvolvedores de diferentes níveis de experiência e acelera o 
desenvolvimento de software.
- **Segura:** A linguagem Go enfatiza a segurança por meio de recursos como verificação de limites de array, 
tratamento de erros robusto e uma forte tipagem estática. Isso ajuda a evitar erros comuns de programação que 
podem levar a vulnerabilidades de segurança.
- **Performática:** GoLang oferece desempenho excepcional devido à sua compilação estática, otimizações de código e 
gerenciamento eficiente de recursos. É uma escolha sólida para aplicativos que exigem alto desempenho, como 
servidores web e sistemas de alto tráfego.

Em resumo, GoLang é uma linguagem de programação que combina simplicidade, segurança e alto desempenho, tornando-a uma 
opção atraente para uma ampla gama de aplicativos e projetos de desenvolvimento.

## Um Pouco de Código
Tente olhar o código a seguir e adivinhar oque ele faz.
```go
package main

import "fmt"

func main() {
numbers := []int{2, 8, 6, 12, 4, 9, 7, 10, 5}

    for i := 0; i < len(numbers); i++ {
        if numbers[i] > 7 {
            numbers[i] = 7
        }
    }

    fmt.Println(numbers)
}
```
*Se você chutou que ...*\
Você pode estar certo ou errado, já que a resposta não vai estar nesse documento. Caso queira 
descobrir, aconselho rodar esse código seguindo um desses links:
- [Instalar o Go](https://go.dev/doc/tutorial/getting-started): Nessa página você verá não só como instalar a linguagem e 
como dar seus primeiros passos na linguagem.
- [Go Playground](https://go.dev/play/): Esse link dá acesso ao compilador online do Go.