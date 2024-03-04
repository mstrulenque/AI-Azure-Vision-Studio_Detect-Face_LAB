# AI - Azure: Vision Studio - Detect Face - LAB

---

**LAB Utilizando**: Microsoft **Azure AI | Vision Studio**

**Descrição do LAB**: 

LAB - com o passo-a-passo em texto e print screen, configurando o recurso Azure AI Services, para realização de atividade de detecção de Face em uma imagem e realização de Testes com 2 imagens com as fotos dos personagens do: Filme - De Volta para o Futuro e Seriado: Breaking Bad.
     
**Ações que serão realizadas**:

 - `Azure`:
   - Criar um Resource Group
   - Provisionar o Resource `Azure AI Services`
     
  - `Vision Studio`
    
     - Configuração:
       -   Selecionar um Resource para utilizar com default na utilizaçãomo melhor no treinamento
    
     - LAB:
       - Teste 1:
         - Selecionar a imagem com os Personagens do Seriado "Breaking Bad".
           (arquivo encontra-se na pasta "input" neste repositório do GitHub)
         - Verificar os resultados:
           - "Detect Attributes"
           - "JSON". (Arquivo JSON completo encontra-se na Pasta "output" neste repositório do GitHub)   
       - Teste 2:
         - Selecionar a imagem com os Personagens do Filme "De Volta para o Futuro".
           (arquivo encontra-se na pasta "input" neste repositório do GitHub)
         - Verificar os resultados:
           - "Detect Attributes"
           - "JSON". (Arquivo JSON completo encontra-se na Pasta "output" neste repositório do GitHub)   
---

# 👷 - Preparando Ambiente para realizar o LAB: 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (Criando Resource Group, aprovisionando o Resource "Azure AI Services) e Selecionando o Recurso p/ utilização no `Vision Studio`.


## 1 - Acesse o `Portal Azure`: <a href="https://portal.azure.com"> <img width="99" alt="https://portal.azure.com" src="https://github.com/mstrulenque/dio-lab-azure-ML/assets/63933792/4665d721-98e7-4c24-bc97-f7540d64a917"></a> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; https://portal.azure.com


## 2 - Faça o Login com a sua Conta 🔐
  
## 3 - Crie e Configure um Resource (Recurso)

3.1 - Na `Home`, Clique em `Create Resource`
<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="228" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/dcefd5aa-08ad-42b2-896d-398dc968cbf7">

3.2 - Na página `Create a Resource` no Menu Lateral Esquerdo:
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
- Em `Categories`, Clique em `AI + Machine Learning`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
- Clique no Link `Create` do Serviço `Azure AI services` na coluna esquerda
<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="419" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/fa9355ef-2398-45de-bd6f-99535cc2a0a1">

3.3 - Criar Resource Group preenchendo os campos: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.1 - `Subscription` - Já vem selecionado sua Subscription; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.2.1 - `Resource Group` - Clique no link `Create New` abaixo do campo; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.2.2 - `Resource Group` - Digite um nome para seu Resource Group; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.2.3 - `Resource Group` - Clique no botão `OK`; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.2.4 - `Resource Group` - o nome que você criou aparecerá selecionado no campo de escolha "Resource Group", <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
caso contrário escolha na lista; <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="419" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/65333ccc-5904-4e0e-8a30-e42537426663">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.3 - `Region` - escolha uma Region da Cloud para criação do workspace; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.4 - `Name` Instance = `RG_ai-azure_ai-services` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.5 - `Pricing tier` = `Standard SO` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.6 - Clique no botão `Review + Create`; <br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="423" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/d6883c80-1060-442a-9f96-5c6a6fabb653">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.7 - Revise os Dados e estando tudo correto, Clique no botão `Create`; <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="423" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/08590582-815f-4feb-880d-f64156d55046">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.3.8 - Após a confirmação o Deploy iniciará, e ao final será apresentada uma pagina similar a pagina abaixo: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="543" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/e174d596-d08f-4946-9847-6fda76ab66e2">
<br>

## 4 - Acesse o `Vision Studio`: <a href="https://portal.vision.cognitive.azure.com"> <img width="120" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/30d79834-9020-4fc0-ac21-daf6b3a32910"></a> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; https://portal.vision.cognitive.azure.com
  
## 5 - Selecione o Resource, aprovisionado no passo acima, p/ utilização do Vision Studio

5.1 - Na página `Home - Get Start with Vision`, Clique em `View All Resources`
<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="522" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/99fcbdd4-ad9c-4712-a4fb-d35efab21133">

5.2 - Na página `Select a resource to work with`:
 - Selecione o Resource criado `instance-azure-ai-services`;
 - Clique no botão `Select as Default resource`
 - e depois clique no botão `X` para fechar a janela.
<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="522" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/6aa1a3e5-d717-411c-b23a-81d35868f786">


---

# 🔬 Realizando o LAB - AI - Azure - Vision Studio (Detect Faces): 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (Após Preparação do Ambiente ter sido Finalizado com Sucesso. Vamos inicia o LAB)

<br>


