# Tabela de Métodos Fiber

| Método                         | Descrição                                                                           |
|--------------------------------|-------------------------------------------------------------------------------------|
| `New()`                        | Cria uma nova instância do aplicativo Fiber.                                        |
| `Use(...func(*fiber.Ctx))`     | Adiciona middlewares globais ao aplicativo, que são executados antes de cada rota.  |
| `Get(route string, ...)`       | Define uma rota para o método HTTP GET.                                             |
| `Post(route string, ...)`      | Define uma rota para o método HTTP POST.                                            |
| `Put(route string, ...)`       | Define uma rota para o método HTTP PUT.                                             |
| `Delete(route string, ...)`    | Define uma rota para o método HTTP DELETE.                                          |
| `Patch(route string, ...)`     | Define uma rota para o método HTTP PATCH.                                           |
| `Head(route string, ...)`      | Define uma rota para o método HTTP HEAD.                                            |
| `Options(route string, ...)`   | Define uma rota para o método HTTP OPTIONS.                                         |
| `All(route string, ...)`       | Define uma rota para todos os métodos HTTP (GET, POST, ...).                        |
| `Static(prefix, root)`         | Serve arquivos estáticos a partir de um diretório.                                  |
| `Group(prefix string)`         | Cria um grupo de rotas com um prefixo comum.                                        |
| `Route(route string)`          | Cria uma nova instância de rota para a rota especificada.                           |
| `Connect(route string, ...)`   | Define uma rota para o método HTTP CONNECT.                                         |
| `Trace(route string, ...)`     | Define uma rota para o método HTTP TRACE.                                           |
| `WebSocket(route string, ...)` | Define uma rota para lidar com conexões WebSocket.                                  |

# Estruturas e valores Fiber

| Struct/Valor              | Descrição                                                                                                                                    |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `fiber.App`               | Estrutura principal que representa o aplicativo Fiber e contém configurações e funcionalidades para gerenciar o aplicativo.                  |
| `fiber.Ctx`               | Estrutura que representa o contexto de uma requisição, contendo informações e funcionalidades relacionadas a uma requisição HTTP específica. |
| `fiber.Config`            | Estrutura que contém as configurações do aplicativo Fiber, permitindo a personalização de comportamentos como porta, tempo limite, etc.      |
| `fiber.Error`             | Estrutura que representa um erro no Fiber, contendo informações sobre o status do erro e a mensagem associada.                               |
| `fiber.Handler`           | Tipo de função que representa um handler (tratador) para uma rota, utilizado para tratar requisições HTTP.                                   |
| `fiber.Map`               | Estrutura de dados que fornece uma maneira eficiente de trabalhar com mapas (dicionários) em middlewares e rotas do Fiber.                   |
| `fiber.Route`             | Estrutura que representa uma rota no Fiber, contendo informações sobre a rota, como método HTTP, caminho, middleware associado, etc.         |
| `fiber.Storage`           | Estrutura de armazenamento que oferece uma maneira de armazenar e acessar dados na aplicação Fiber, como variáveis de sessão.                |
| `fiber.ETagOptions`       | Estrutura que define as opções para geração de ETags (Entity Tags) para controle de cache de resposta.                                       |
| `fiber.Limiter`           | Estrutura que representa um limitador de taxa (rate limiter) para limitar a taxa de requisições em rotas específicas.                        |
| `fiber.ProxyConfig`       | Estrutura que define as configurações para o middleware de proxy reverso, usado para redirecionar solicitações para outro servidor.          |
| `fiber.Static`            | Estrutura que representa as configurações para servir arquivos estáticos usando o middleware de arquivos estáticos.                          |
| `fiber.WebSocketUpgrade`  | Estrutura que representa uma atualização de protocolo para WebSockets, permitindo o uso de conexões WebSocket em rotas específicas.          |
| `fiber.WsMessage`         | Estrutura que representa uma mensagem WebSocket, contendo dados e informações sobre o tipo da mensagem (texto ou binário).                   |
| `fiber.WsHandler`         | Tipo de função que representa um handler (tratador) para conexões WebSocket, usado para tratar comunicação em tempo real via WebSocket.      |
| `fiber.MapFunc`           | Tipo de função que define um mapeamento personalizado usado para transformar e manipular valores em middlewares e rotas do Fiber.            |
| `fiber.HandlerSignature`  | Assinatura de função usada para definir o tipo de função que atua como handler (tratador) em rotas do Fiber.                                 |

