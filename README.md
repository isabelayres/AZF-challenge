# AZF-challenge

Este é meu primeiro projeto de IA construído com recursos gratuitos para o AFG Challenge - AZ900.

## Introdução

Este repositório contém informações sobre a criação do Agente Papers, No **Azure AI Foundry**.

## Descrição do agente

Esse agente tem o objetivo de manipular os dados registrados em uma planilha em Excel denominada papers. Essa planilha foi obtida por meio de pesquisas em bases de dados especializadas. Os dados foram exportados no formato RIS e reunidos em um arquivo CSV. Após essa reunião eles foram exportados para uma planilha XLX.

## Objetivo do agente

O agente deve auxiliar a pessoa pesquisadora a extrair dados de forma inteligente e rápida. Embora seja possível criar filtros e tabelas dinâmicas no Excel, os metadados dessa planilha são inconsistentes, pois vieram de bases de dados diferentes (Ebsco, Dimension, Proquest dentre outras). A ideia é que o agente possa automatizar as pesquisas a essa fonte de dados.

## Fluxos</br>

<img src="Attachments/Images/fluxo1.png" align=center alt="fluxo1"></br></br>
<img src="Attachments/Images/fluxo2.jpeg" align=center alt="fluxo2"></br></br>
<img src="Attachments/Images/fluxo3.jpeg" align=center alt="fluxo3"></br></br>

## Execução - Passo-a-passo da Criação do Agente

Após a criação do recurso do AI Foundry na plataforma Azure, e do respectivo projeto, fomos direcionados para o AI Foundry Portal e executamos os passos a seguir.

#### a) Na barra esquerda buscamos a opção <b>AGENTS</b> e clicamos no Botão azul NEW AGENT conforme a figura a seguir:
<img src="Attachments/Images/agente_01.jpg" align=center alt="passo1">
</br>

### b) Depois que o agente é criado ao clicarmos sobre ele temos acesso ao painel de SETUP, onde a configuração é finalizada.
Os campos a seguir foram preenchidos:
1) Agent Name</br>
✔ Papers
<img src="Attachments/Images/agente_02.jpg" alt="figura2"></br>
2) Deployment (antes da criação do agente deve-se passar por essa etapa)
✔ gpt 4.1 - esse foi o único aceito na nossa conta </br>
3) Instructions:</br>
✔ Fornecemos instruções para o agente:</br>
=> Você deve responder questões relacionadas ao conteúdo da planilha papers. Você emails somente quando solicitado. Você não responde nenhuma outra questão sobre qualquer outro assunto.
4) Knowledge</br>
Não utilizamos em nosso agente.
5) Actions</br>
Incluímos duas Actions em nosso agente (ele vai ter que trabalhar😁) </br>
✔ Code Interpreter Action </br>
Optamos por esta ação pois ela manipula dados não estruturados. Devido à restrições da conta Trial, não foi possível utilizar recursos mais apropriados para essa finalidade. As figuras abaixo ilustram esse processo:</br>
Tela antes da criação da Action:</br>
<img src="Attachments/Images/agente_03.jpg" alt="Figura2"></a></br></br>
Tela com o resultado depois do upload do arquivo que contém os dados a serem utilizados pelo Agente:</br>
<img src="Attachments/Images/agente_04.jpg" alt="Figura4"></a>
</br>
✔ Logi App Action</br>
Criamos uma Action para enviar os dados manipulados por e-mail.
As figuras a seguir mostram a inserção das informações básicas da configuração:<br>
<img src="Attachments/Images/agente_07.jpg" alt="Figura 5"></br></br>
<img src="Attachments/Images/agente_08.jpg" alt="Figura 6">
</br>
Na Figura abaixo validamos a conta do Outlook utilizada para envio dos e-mails.</br>
<img src="Attachments/Images/agente_09.jpg" alt="figura 7"></br>
Na Figura abaixo é validada a criação do Recurso.</br>
<img src="Attachments/Images/agente_10.jpg" alt="figura 8">
Finalmente na figura abaixo o Schema gerado e podemos então finalizar a criação.</br></br>
<img src="Attachments/Images/agente_11.jpg" alt="figura 9"></br>
</br>
<b>Cumpridas essas etapas testamos o Agente Papers no Try Playground.</b>

## Playground
Nossa primeira conversa com agente é visualizada nas sequência de imagens a seguir.
A primeira questão foi perguntar ao Agente quantas linhas existem na planilha, ao que ele respondeu corretamente: 8.459 linhas.</br>
<img src="Attachments/Images/agente_12.jpg" alt="figura 10"></br>
A segunda pergunta foi pedir para que ele verificasse a ocorrência da palavra _cataloging _ ao que ele respondeu corretamente: 2.309 linhas. </br>
<img src="Attachments/Images/agente_13.jpg" alt="figura 11"></br>
Depois foi solicitado o envio dessa planilha por e-mail.
<img src="Attachments/Images/agente_14.jpg" alt="figura 12"></br>
Após essa pequena rodada de testes concluímos que nosso Agente está pronto para cumprir sua missão!
</br>
<a href="https://1drv.ms/b/c/099f7545fc79e21a/EVFwi0OZ_f1NoTgaC1foVQABQ4xtjFvHyHco4IzldHPU-Q?e=rdbBwK"> Baixe o arquivo PDF com a conversa completa</a></br>

## Referências</br>
[AI Foundry na Prática](./Azure_AI_Foundry_na_Pratica_aula_2.md)
