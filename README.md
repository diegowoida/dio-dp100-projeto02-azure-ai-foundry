# Objetivo
O objetivo deste projeto é desenvolver chat interativo que responderá com base no conteúdo dos seus arquivos PDF. Para isso, utilizaremos conceitos de IA generativa, embeddings e buscas vetorizadas.

✅ Carregue arquivos PDF contendo informações relevantes para seu estudo ou projeto.  
✅ Implemente um sistema de busca vetorial para indexar e recuperar informações dos PDFs.  
✅ Utilize inteligência artificial para gerar respostas baseadas no conteúdo dos documentos carregados.  
✅ Desenvolva um chat interativo onde seja possível realizar perguntas e obter respostas contextuais fundamentadas nos arquivos.  

# 
# Passo a Passo

## 1. Criar o grupo de recursos para o projeto
#### 1.1 Acesse o **[Portal do Azure](https://portal.azure.com/)**;
#### 1.2 Faça _login_ com sua conta **Azure**;
![Captura de tela 2025-03-28 200600](https://github.com/user-attachments/assets/ae15615a-0c82-4521-84a5-1e9753a01ee4)
<p align="center">Imagem 01 - <b>Portal Azure</b></p>  

#### 1.3 Após o _login_ acesse as opções **Create a resource** e selecione **Resource group**;
![Captura de tela 2025-03-28 200617](https://github.com/user-attachments/assets/0b9857dc-69e4-4310-a514-21b420df4f3c)
<p align="center">Imagem 02 - <b>Resource Group</b> dentro do Portal Azure</p>  

#### 1.4 Insira o nome que desejar e em "**Review & Create**".  
![Captura de tela 2025-03-28 200657](https://github.com/user-attachments/assets/06c7b154-8504-4e02-9e7f-b93c649c13e8)
<p align="center">Imagem 03 - Criando um Resource Group</p>  

![Captura de tela 2025-03-28 200725](https://github.com/user-attachments/assets/50b3f344-151e-4dad-9fc1-4b0e29b24d35)
<p align="center">Imagem 04 - Criando um <b>Resource Group</b></p>  

![Captura de tela 2025-03-28 200745](https://github.com/user-attachments/assets/0fd7558c-c536-41ba-876f-cc38d4f953c6)
<p align="center">Imagem 05 - Criação do <b>Resource Group</b> sendo executada</p>  

![Captura de tela 2025-03-28 200756](https://github.com/user-attachments/assets/376d8b9a-12ec-4eac-aef5-926aa719a9da)
<p align="center">Imagem 06 - Criação do <b>Resource Group</b> concluída</p>  

#### 1.5 Acesse o **Resource group** e clique em **Create** para criar o recurso **Azure AI Foundry**.
![Captura de tela 2025-03-28 200819](https://github.com/user-attachments/assets/15f2ecd9-48b4-4edb-baf6-b5d2e6632d6c)
<p align="center">Imagem 07 - Criar <b>Resource</b> dentro do <b>Resource Group</b></p>  

![Captura de tela 2025-03-28 200856](https://github.com/user-attachments/assets/d9b0830c-fae1-4f0a-a1ed-04e4da6bde0d)
<p align="center">Imagem 08 - Selecione o recurso <b>Azure AI Foundry</b></p>  

#### 1.6 Selecione as opções da assinatura Azure, o grupo de recursos, a região e dê um nome para o recuso do **Azure AI Foundry** e clique em **Review + create**.
![Captura de tela 2025-03-28 201104](https://github.com/user-attachments/assets/45b58861-3012-4d53-8cae-bfbb4a3c8a20)
<p align="center">Imagem 09 - Criando o recurso <b>Azure AI Foundry</b></p>  

![Captura de tela 2025-03-28 201213](https://github.com/user-attachments/assets/2beac401-ff84-4e9b-9d20-da14f8b7254e)
<p align="center">Imagem 10 - Recurso <b>Azure AI Foundry</b> sendo criado</p>  

#### 1.7 Após concluir a criação do recurso do **Azure AI Foundry** clique em "**Go to resource**" para acessar o portal
![Captura de tela 2025-03-28 201445](https://github.com/user-attachments/assets/9029ac36-b8b9-4b04-8385-5e5e3c0d2321)
<p align="center">Imagem 11 - Concluído a criação do recurso <b>Azure AI Foundry</b></p>  

---------------------

## 2. Acessar o Azure AI Foundry
#### 2.1 Acesse o **[Portal do Azure AI Foundry](https://ai.azure.com/)**;
- No primeiro acesso será solicitado para criar um novo projeto;
![Captura de tela 2025-03-28 201521](https://github.com/user-attachments/assets/e8bbf1f4-19f7-4fdc-a50d-c2639e9db233)
<p align="center">Imagem 12 - Portal do <b>Azure AI Foundry</b></p>  

#### 2.2 Clique em **New project** dê um nome para o projeto e **Create project**.
![Captura de tela 2025-03-28 201622](https://github.com/user-attachments/assets/75fc0370-8cb7-4d56-b764-44aadb0c2336)
<p align="center">Imagem 13 - Criando um projeto no <b>Azure AI Foundry</b></p>  

#### 2.3 Projeto criado.
![image](https://github.com/user-attachments/assets/40e400f9-0482-4d02-838c-6459c5d388ab)
<p align="center">Imagem 14 - Criando um projeto no <b>Azure AI Foundry</b></p>  

#### 2.4 Para selecionar os modelos acesso no menu lateral "**Models + endpoints** -> **Deploy base model** -> **gpt-4o**" e clique em **Confirm**
![Captura de tela 2025-03-28 202320](https://github.com/user-attachments/assets/89c65f69-038a-4c11-867c-660da8f6fe47)
<p align="center">Imagem 15 - Acessando o menu de <b>Models + endpoints</b></p>  

![Captura de tela 2025-03-28 202739](https://github.com/user-attachments/assets/22ef85dd-1de9-4c6b-ba41-592272f3ca67)
<p align="center">Imagem 16 - Selecionando o modelo <b>GPT-4o</b></p>  

![Captura de tela 2025-03-28 202913](https://github.com/user-attachments/assets/06dd622b-8d88-4901-9403-591a74dfc51a)
<p align="center">Imagem 17 - Criando o modelo <b>GPT-4o</b></p>  

#### 2.5 Repita o processo anterior selecionando o modelo "**text-embedding-3-large**"
![Captura de tela 2025-03-28 203432](https://github.com/user-attachments/assets/316d7c07-26ed-4898-9d42-14d74cfd3399)
<p align="center">Imagem 18 - Selecionando o modelo <b>Text Emedding 3 Large</b></p>  

![Captura de tela 2025-03-28 203513](https://github.com/user-attachments/assets/a33347ff-6295-44da-b57d-d3295c56fbca)
<p align="center">Imagem 19 - Criando o modelo <b>Text Emedding 3 Large</b></p>  

---------------------

## 3. Criando o recurso **Search service**
#### 3.1 Repita os passos da **Etapa 1.5** selecionando o recurso **Search service**
![Captura de tela 2025-03-28 205221](https://github.com/user-attachments/assets/48800b05-68f7-4f64-afc6-14714ded1951)
<p align="center">Imagem 20 - Criando o recurso <b>Search service</b></p>  

![Captura de tela 2025-03-28 205238](https://github.com/user-attachments/assets/4cdd64bf-d43d-4768-bf51-3ef8c5a2460d)
<p align="center">Imagem 21 - Criando o recurso <b>Search service</b></p>  

![Captura de tela 2025-03-28 205401](https://github.com/user-attachments/assets/bc4c2a2e-d9fc-4236-82d0-1a91f188e869)
<p align="center">Imagem 22 - Recurso criado <b>Search service</b></p>  

---------------------

## 4. Importar o dataset
#### 4.1 Com os dois modelos criado, agora acesse no menu lateral do portal **Azure AI Foundry** a opção **Playground** -> **Chat playground**.
![Captura de tela 2025-03-28 204340](https://github.com/user-attachments/assets/a46201d3-5725-40ee-84f6-f8b40ccaec95)
<p align="center">Imagem 23 - Configurações do <b>Chat playground</b></p>  

#### 4.2 Em **Add your data** e depois **Add your data source** -> **Upload files** e selecione o dataset desejado.
![Captura de tela 2025-03-28 204613](https://github.com/user-attachments/assets/66a04219-3ab7-496a-805b-3c60e65242b3)
<p align="center">Imagem 24 - Selecionando sua própria base de dados</p>  

![Captura de tela 2025-03-28 204631](https://github.com/user-attachments/assets/e67a9588-ebd0-463a-8a56-d40a05e533d9)
<p align="center">Imagem 25 - Realizando o envio da base de dados</p>  

#### 4.3 Após selecionar o dataset desejado é necessário fazer a conexão desse dataset com **Search service**
![Captura de tela 2025-03-28 205602](https://github.com/user-attachments/assets/f2957cdb-b598-4abb-94f4-5eaa04a06c89)
<p align="center">Imagem 26 - Conectando a base de dados com o <b>Search service</b></p>  

![Captura de tela 2025-03-28 205653](https://github.com/user-attachments/assets/70520094-30a4-445c-876a-6afdd4245d31)
<p align="center">Imagem 27 - Criando o vetor de indices do <b>Search service</b></p>  

---------------------

## 5. Deploy do chat interativo
#### 5.1 O chat interativo pode ser feito o deploy para um Web app, Teams app ou para o Copilot Studio.
![Captura de tela 2025-03-28 224141](https://github.com/user-attachments/assets/9daae85e-ae53-4252-8c9e-33e7ab480869)
<p align="center">Imagem 28 - Realizando o <b>deploy</b> do chat interativo</p>  
