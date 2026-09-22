# Laboratório Educacional de Engenharia Social com SEToolkit

> Projeto desenvolvido para fins exclusivamente educacionais, em ambiente controlado e com dados fictícios.

## Sobre o projeto

Este repositório documenta um laboratório prático de conscientização sobre **phishing** e engenharia social, realizado como parte de um desafio da [Digital Innovation One (DIO)](https://www.dio.me/).

O objetivo foi compreender como páginas fraudulentas podem coletar informações enviadas por formulários e, principalmente, identificar os riscos envolvidos e as medidas de prevenção.

## Objetivos de aprendizagem

- Utilizar o Kali Linux em um laboratório virtualizado.
- Conhecer recursos do Social-Engineer Toolkit (SEToolkit).
- Compreender o funcionamento de formulários HTTP e requisições POST.
- Observar como informações podem ser expostas em páginas fraudulentas.
- Documentar limitações técnicas, resultados e medidas defensivas.
- Praticar documentação e versionamento com GitHub.

## Ambiente do laboratório

| Componente | Utilização |
|---|---|
| Kali Linux | Sistema operacional da máquina virtual |
| Oracle VirtualBox | Virtualização do ambiente |
| SEToolkit | Simulação controlada de engenharia social |
| Firefox | Acesso à página local de treinamento |
| Git e GitHub | Versionamento e documentação |

A máquina virtual estava em modo de rede **Bridge**, utilizando um endereço IP privado da rede local. O servidor foi encerrado imediatamente após o teste.

## Escopo e regras de segurança

O laboratório foi executado somente em equipamento próprio e com autorização.

- Nenhuma credencial real foi utilizada.
- A página possuía um aviso explícito de simulação educacional.
- O endereço do laboratório não foi compartilhado com terceiros.
- Logs, relatórios e valores capturados não foram publicados.
- O servidor local foi encerrado após a validação.
- O projeto não deve ser utilizado contra pessoas, empresas ou sistemas sem autorização formal.

## Procedimento realizado

### 1. Inicialização do SEToolkit

A ferramenta foi iniciada com privilégios administrativos limitados ao processo:

```bash
sudo setoolkit
```

### 2. Seleção do módulo

O seguinte caminho foi utilizado nos menus da ferramenta:

```text
Social-Engineering Attacks
└── Website Attack Vectors
    └── Credential Harvester Attack Method
```

### 3. Teste do Site Cloner

Inicialmente, foi testado o método **Site Cloner** seguindo a proposta original do desafio. Entretanto, o SEToolkit não conseguiu clonar a página moderna de autenticação do Facebook.

Essa limitação pode ocorrer porque serviços atuais utilizam conteúdo dinâmico, redirecionamentos, controles de segurança e outros mecanismos incompatíveis com a clonagem simples realizada pela ferramenta.

### 4. Adaptação segura do laboratório

Para concluir o aprendizado sem tentar contornar as proteções do serviço real, foi utilizada a opção **Custom Import** com uma página local denominada **Social Lab**.

A página:

- identificava claramente que se tratava de uma simulação;
- solicitava somente dados fictícios;
- era executada localmente;
- utilizava um formulário POST para demonstrar o fluxo de informações;
- não utilizava logotipos, códigos ou arquivos pertencentes ao Facebook.

### 5. Validação

A página educacional foi acessada pelo navegador dentro do ambiente controlado. Após o envio de valores fictícios, o terminal do SEToolkit identificou os parâmetros do formulário, demonstrando como informações submetidas a uma página fraudulenta podem ser expostas.

Ao final, o servidor foi encerrado com `Ctrl + C`.

## Resultado

O laboratório demonstrou com sucesso:

- disponibilização de uma página de treinamento em servidor HTTP local;
- envio de informações fictícias por formulário;
- identificação dos parâmetros POST pelo SEToolkit;
- importância de verificar endereço, protocolo e legitimidade de páginas de autenticação;
- necessidade de adaptar tutoriais antigos às proteções presentes em aplicações modernas.

> As evidências publicadas neste repositório devem ocultar endereços de rede, senhas e qualquer outra informação sensível.

## Como reconhecer e evitar phishing

- Verifique cuidadosamente o domínio antes de informar dados.
- Desconfie de mensagens com urgência, ameaça ou promessa de vantagem.
- Evite abrir links de login recebidos por mensagens inesperadas.
- Utilize gerenciadores de senhas, que ajudam a identificar domínios incorretos.
- Ative autenticação multifator sempre que possível.
- Nunca reutilize a mesma senha em serviços diferentes.
- Em caso de dúvida, acesse o serviço digitando o endereço oficial no navegador.

## Aprendizados

Além do uso básico do SEToolkit, este projeto reforçou conhecimentos sobre:

- engenharia social;
- funcionamento de requisições HTTP;
- campos de formulários e método POST;
- endereçamento IP privado;
- serviços executados em portas de rede;
- limites éticos e legais dos testes de segurança;
- documentação técnica para portfólio.

## Aviso legal e ético

Este conteúdo foi criado exclusivamente para aprendizado, conscientização e demonstração em ambiente autorizado. A captura de credenciais, falsificação de páginas e acesso a sistemas sem consentimento podem constituir crimes.

O autor não incentiva o uso deste material para atividades maliciosas.

## Autor

**Francisco David de Assis Pereira**

- GitHub: [@FDavidPereira](https://github.com/FDavidPereira)
- Área de interesse: Cibersegurança, SOC, Blue Team e Red Team
