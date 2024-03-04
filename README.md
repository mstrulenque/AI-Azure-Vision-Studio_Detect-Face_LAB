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

3.2 - Na página `Create a Resource` no Menu Lateral Esquerdo: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
▶️  Em `Categories`, Clique em `AI + Machine Learning` ;  <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
▶️  Clique no Link `Create` do Serviço `Azure AI services` na coluna esquerda;  <br>
<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
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

5.2 - Na página `Select a resource to work with`: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
▶️  Selecione o Resource criado `instance-azure-ai-services` ; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
▶️  Clique no botão `Select as Default resource` ; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
▶️  e depois clique no botão `X` para fechar a janela; <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="522" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/6aa1a3e5-d717-411c-b23a-81d35868f786">


---

# 🔬 Realizando o LAB - AI - Azure - Vision Studio (Detect Faces): 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (Após Preparação do Ambiente ter sido Finalizado com Sucesso. Vamos inicia o LAB)

<br>

## 1 - Acesse o `Vision Studio`: <a href="https://portal.vision.cognitive.azure.com"> <img width="120" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/30d79834-9020-4fc0-ac21-daf6b3a32910"></a> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; https://portal.vision.cognitive.azure.com
  
## 2 - LAB - `Detect Faces`

2.1 - Na página `Home - Get Start with Vision`: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     ▶️  Clique na Guia `Face` ; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     ▶️  Clique no link `Try it out` do box `Detect faces in an image` ; <br>


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="522" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/bd9ea47c-1ed4-45a5-beec-7b10e13c59d7">

## 3 - LAB - `Detect Faces`

3.1 `Teste 1` - Imagem - Atores Seriado `Breaking Bad` : <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.1.1 - Escolhendo a Imagem 1: `breaking_bad.png` - pasta: `input` - deste repositório GitHub: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          ▶️  Na página `Detect Faces in an image` ; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          ▶️ no Box `Drag and Drop File on File here` ; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          ▶️ Clique no link `Browse for a file` ; <br>
          
<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="296" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/33b6b78e-859e-4697-adfe-e0c225ee0c30">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          ▶️  Escolha o arquivo `breaking_bad.png` da pasta `input` deste repositório GitHub;
   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="488" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/ffd0bfcf-a3aa-40c7-81db-783b4639b38e">


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.1.2 - `Resultado do Processamento` (Imagem 1), pelo `Vision Studio`: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.1.2.1 - Resultado - `Detected Attributes`: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="478" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/11578f29-aec6-4aa3-b5d2-4f172ae48f4a">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.1.2.2 - Resultado - `JSON`: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="478" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/b53b0216-5a2d-436d-b7f8-3b5305b2e7c0">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.1.2.3 - Resultado - `JSON` - Em Arquivo: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
▶️  Encontra-se na pasta `output` deste repositório: <a href = "https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/blob/main/output/face-recognition_img-1_breaking-bad.json" target="_blank"> clique aqui </a>

---

3.2 `Teste 2` - Imagem - Atores Filme `De Volta para o Futuro` : <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.2.1 - Escolhendo a Imagem 2: `Bck_2_the_future.png` - pasta: `input` - deste repositório GitHub: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          ▶️  Na página `Detect Faces in an image` ; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          ▶️ no Box `Drag and Drop File on File here` ; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          ▶️ Clique no link `Browse for a file` ; <br>
          
<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="296" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/33b6b78e-859e-4697-adfe-e0c225ee0c30">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          ▶️  Escolha o arquivo `Bck_2_the_future.png` da pasta `input` deste repositório GitHub;
   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="480" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/3413f6fc-364d-48c4-9cf0-53a03ad2d6f7">


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.2.2 - `Resultado do Processamento` (Imagem 2), pelo `Vision Studio`: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.2.2.1 - Resultado - `Detected Attributes`: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="497" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/784c8c13-3ea5-46ed-8ba2-878d07170a97">


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.2.2.2 - Resultado - `JSON`: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img width="497" alt="image" src="https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/assets/63933792/d60a5fa9-8a5b-4bba-9226-e21fda374753">

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
3.2.2.3 - Resultado - `JSON` - Em Arquivo: <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
▶️  Encontra-se na pasta `output` deste repositório: <a href = "https://github.com/mstrulenque/AI-Azure-Vision-Studio_Detect-FaceLAB/blob/main/output/face-detection_img-2_Bck-2-future.json" target="_blank"> clique aqui </a>
















