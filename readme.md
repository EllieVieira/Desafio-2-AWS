# Desafio DIO - AWS Step Functions

Este projeto foi desenvolvido como parte do desafio da DIO para praticar **workflows automatizados com AWS Step Functions**.  
O objetivo foi criar e documentar um fluxo simples que orquestra duas funções Lambda de forma automatizada.

---

## O que é o AWS Step Functions

O **AWS Step Functions** é um serviço que permite orquestrar vários serviços da AWS (como Lambda, S3, DynamoDB, entre outros) em fluxos de trabalho visuais e automatizados.  
Ele coordena cada etapa de um processo, garantindo que as tarefas sejam executadas na ordem correta, com tratamento de erros, condições, e transições definidas.

De forma simples: é como um “diretor” que chama os “atores” (funções e serviços da AWS) na hora certa, conforme o roteiro definido.

---

## O que foi feito neste desafio

1. Criação de **duas funções Lambda**:
   - `inicioFunction`: representa o início do processo.
   ![Diagrama](https://imgur.com/HyPLUkO)
   <br>

   - `fimFunction`: representa o término do processo.
   ![Diagrama](https://imgur.com/blwiEy6)


2. Criação de uma **Step Function** que executa:
   - O estado **“Início”**, que chama a `inicioFunction`;
   - Depois o estado **“Fim”**, que chama a `fimFunction`.

3. Execução do fluxo completo, mostrando como a Step Function coordena as funções automaticamente.

---

## Imagens do Projeto

**Tela do workflow no Step Function**
![Diagrama](https://imgur.com/eywdaDw)
<br>

**Execução bem-sucedida**
![Resultado](https://imgur.com/KARqIRW)


---

## Aprendizados

##### Entendimento do conceito de orquestração de serviços com Step Functions.  
Durante o desafio, pude compreender melhor o conceito de orquestração de serviços, que basicamente consiste em coordenar diferentes recursos da AWS para que trabalhem juntos de forma automatizada. O **AWS Step Functions** atua como um “diretor” do processo, definindo a ordem das etapas, as condições de execução e o tratamento de possíveis erros. Isso torna possível criar fluxos bem estruturados e confiáveis, garantindo que cada parte do sistema execute exatamente no momento certo.

##### Integração prática entre AWS Lambda e Step Functions.    
A integração entre o **AWS Lambda** e o **Step Functions** foi um dos pontos principais do projeto. Ao conectar as duas funções Lambda criadas — uma representando o início e outra o fim do processo —, consegui visualizar na prática como o Step Functions gerencia a execução de forma automática. Essa integração elimina a necessidade de criar código adicional para controlar a sequência de chamadas, permitindo que o fluxo siga a lógica definida no diagrama do Step Functions de maneira simples e eficiente.

##### Visualização de fluxos automatizados e controle de execução no console da AWS
Outro ponto importante foi a experiência de visualizar o fluxo completo diretamente no console da AWS. A interface do Step Functions permite acompanhar em tempo real cada etapa do processo, identificando facilmente o que foi executado, o que ainda está em andamento e se houve algum erro. Essa visualização ajuda muito no entendimento do funcionamento do workflow e torna o monitoramento e o ajuste das execuções algo bem mais prático e intuitivo.

---

## Referências

- [Documentação oficial do AWS Step Functions](https://docs.aws.amazon.com/step-functions/)
- [Documentação AWS Lambda](https://docs.aws.amazon.com/lambda/)
- [Plataforma DIO](https://www.dio.me)

---

## Autora

**Ellie Vieira**  
Desenvolvedora em formação • Explorando automação e computação em nuvem  
[GitHub](https://github.com/EllieVieira)
