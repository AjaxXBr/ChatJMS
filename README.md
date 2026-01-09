📡 ChatJMS — Chat Distribuído com Java JMS


O ChatJMS é um sistema de chat distribuído desenvolvido em Java, utilizando JMS (Java Message Service) em conjunto com o Apache ActiveMQ como broker de mensagens.
O projeto tem como objetivo demonstrar o funcionamento da comunicação assíncrona em sistemas distribuídos, permitindo a troca de mensagens entre múltiplos usuários em tempo real.

O sistema é composto por dois aplicativos principais:

Servidor JMS, responsável pela distribuição das mensagens.

Cliente JMS, que fornece uma interface gráfica para envio e recebimento das mensagens.

🧠 Conceitos Utilizados

Sistemas Distribuídos

Comunicação Assíncrona

Java Message Service (JMS)

Filas (Queues) e/ou Tópicos (Topics)

Apache ActiveMQ

Programação em Java

Interface Gráfica (Swing)

🛠 Tecnologias Utilizadas

Java (JDK 8 ou superior)

JMS (Java Message Service)

Apache ActiveMQ

Swing (Interface Gráfica)

IDE: Eclipse / IntelliJ IDEA / NetBeans (qualquer uma compatível)


🧩 Funcionamento Geral

O servidor JMS é iniciado e conecta-se ao Apache ActiveMQ.

Cada cliente, ao iniciar, informa um código de usuário (identificador único).

O cliente pode:

Enviar mensagens para todos os usuários (broadcast).

Enviar mensagens para um usuário específico, informando seu código.

As mensagens são enviadas ao servidor, que:

Analisa o destinatário.

Distribui corretamente as mensagens usando filas ou tópicos JMS.

As mensagens recebidas são exibidas na interface gráfica do cliente.

🖥 Interface do Cliente

O aplicativo cliente possui os seguintes elementos:

📄 Campo de texto para digitação da mensagem

👤 Campo para digitação do código do destinatário (opcional)

📥 Área de texto para exibição das mensagens recebidas

📤 Botão de envio

⌨️ Envio também pode ser feito pressionando Enter


📦 Requisitos para Execução

Java instalado (JDK 8+)

Apache ActiveMQ instalado e em execução

Variáveis de ambiente JAVA configuradas corretamente

🚀 Como Executar o Projeto
1️⃣ Baixar e iniciar o Apache ActiveMQ

Faça o download do ActiveMQ:

https://activemq.apache.org/


Extraia o arquivo.

Inicie o broker:

Windows:

bin\activemq.bat start


Linux/Mac:

./bin/activemq start


O painel web ficará disponível em:

http://localhost:8161

2️⃣ Executar o Servidor

Abra o projeto do ServidorJMS na IDE.

Execute a classe principal do servidor.

Verifique se a conexão com o ActiveMQ foi realizada com sucesso.

3️⃣ Executar o Cliente

Abra o projeto ClienteJMS.

Execute a aplicação.

Ao iniciar, informe:

Seu código de usuário

Pronto! O chat já estará funcional.

✉️ Tipos de Mensagem

Mensagem Global:
Campo de destinatário vazio → mensagem enviada para todos.

Mensagem Privada:
Campo de destinatário preenchido → mensagem enviada apenas ao usuário informado.
