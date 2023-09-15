# Introdução REST API  
## Oque é uma API
Uma **API (Interface de Programação de Aplicativos)** é um conjunto de regras e protocolos que permitem que diferentes 
softwares se comuniquem e interajam uns com os outros. Ela define como solicitar serviços ou recursos de um aplicativo 
ou sistema, bem como como receber e interpretar as respostas.

## Oque significa REST
**REST**, que significa *Representational State Transfer*, é um estilo de arquitetura de software usado para projetar 
redes de comunicação em sistemas distribuídos. O REST se baseia em princípios como o uso de recursos identificáveis por 
URLs, métodos HTTP padrão (GET, POST, PUT, DELETE) para interações e um sistema de estado uniforme. Ele promove a 
simplicidade, escalabilidade e a facilidade de manutenção.

# Oque são os Métodos HTTP
O **HTTP (Hypertext Transfer Protocol)** é um protocolo de comunicação utilizado na World Wide Web para transferir 
dados entre um cliente (geralmente um navegador web) e um servidor web. Ele define vários métodos padrão que especificam
o tipo de ação que está sendo solicitada em relação a um recurso identificado por uma URL. Aqui estão quatro dos métodos 
HTTP padrão mais comuns:

- **GET**: O método GET é usado para solicitar a recuperação de um recurso, geralmente uma página da web, identificado 
por uma URL. Ele é usado quando você deseja obter informações do servidor, como ler uma página da web ou recuperar 
dados, e não deve ter efeitos colaterais no servidor.
- **POST**: O método POST é usado para enviar dados para o servidor para criar ou atualizar um recurso. Ele é comumente
usado para enviar informações de formulários da web para o servidor. Ao contrário do GET, o POST pode ter efeitos
colaterais, como a criação de um novo registro em um banco de dados.
- **PUT**: O método PUT é usado para atualizar ou substituir completamente um recurso existente ou criar um recurso se
ele não existir. Ele envia os dados necessários para substituir o recurso especificado na URL. O PUT é usado para
operações de atualização de dados.
- **DELETE**: O método DELETE é usado para solicitar a remoção de um recurso identificado por uma URL. Ele instrui o
servidor a excluir o recurso especificado. É usado para operações de exclusão de dados.

Esses quatro métodos são fundamentais para a interação entre clientes e servidores na web e são a base para muitas das 
operações que ocorrem durante a navegação na internet e a comunicação com serviços web.

## Finalmente, oque é REST API
**REST API** é uma API que segue os princípios do REST. Ela usa URLs para identificar recursos, métodos HTTP para 
realizar operações em recursos (como recuperar, criar, atualizar ou excluir) e usa o sistema de estado uniforme para 
definir o estado atual dos recursos. As REST APIs são amplamente usadas na web para criar serviços da web que podem ser 
acessados e consumidos por diferentes aplicativos e plataformas, tornando a comunicação entre sistemas mais eficiente e 
flexível.

