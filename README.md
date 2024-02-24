# Configuração de Pesquisa de IA do Azure para Insights em Experiências do Cliente

Este guia fornece instruções passo a passo para configurar uma solução de pesquisa de IA do Azure, visando extrair insights das avaliações de clientes da Fourth Coffee, uma rede nacional de cafés. O objetivo é criar um índice de Pesquisa de IA do Azure, enriquecer os dados com habilidades de IA e consultar o índice para obter informações valiosas.

## Passos:

### 1. Criar Recursos do Azure:

   a. Criar um recurso de Pesquisa de IA do Azure no portal do Azure.
   
   - Assinatura: Sua assinatura do Azure.
   - Grupo de Recursos: Selecionar ou criar um grupo de recursos exclusivo.
   - Nome do Serviço: Escolher um nome exclusivo.
   - Localização: Escolher qualquer região disponível.
   - Nível de Preços: Básico.

   b. Criar um recurso de Serviços de IA do Azure:
   
   - Assinatura: Sua assinatura do Azure.
   - Grupo de Recursos: Mesmo grupo do recurso de Pesquisa de IA do Azure.
   - Região: Mesmo local do recurso de Pesquisa de IA do Azure.
   - Nome: Nome exclusivo.
   - Nível de Preços: Standard S0.

### 2. Criar uma Conta de Armazenamento:

   - Criar uma conta de armazenamento no portal do Azure.
   - Configurar a conta com desempenho padrão e redundância localmente redundante (LRS).
   - Permitir acesso anônimo de Blob configurado como Habilitado.

### 3. Carregar Documentos no Armazenamento do Azure:

   - Criar um contêiner chamado "cafe-comentarios" com acesso público.
   - Baixar e extrair os documentos de revisões de café [aqui](https://aka.ms/mslearn-coffee-reviews).
   - Carregar os documentos no contêiner criado.

### 4. Indexar os Documentos:

   - Navegar até o recurso de Pesquisa de IA do Azure e selecionar "Importar dados".
   - Conectar aos dados de armazenamento de blobs do Azure.
   - Adicionar habilidades cognitivas, como OCR, extração de locais, frases-chave, sentimento, etc.
   - Configurar o índice de destino e criar um indexador.

### 5. Consultar o Índice:

   - Utilizar o Gerenciador de Pesquisa no portal do Azure para escrever e testar consultas.
   - Exemplos de consultas JSON para pesquisar todos os documentos, filtrar por localização e sentimento.

### 6. Revisar o Repositório de Conhecimento:

   - Explorar o armazenamento de conhecimento criado durante o processo.
   - Visualizar os dados enriquecidos, como projeções de imagens, tabelas de entidades e frases-chave.

## Insights e Possibilidades:

- A solução permite analisar automaticamente as avaliações dos clientes, identificando locais, sentimentos e frases-chave.
- O repositório de conhecimento oferece uma visão detalhada dos dados enriquecidos, facilitando a compreensão das informações extraídas.
- Os insights obtidos podem ser utilizados para aprimorar as experiências do cliente, identificando áreas de melhoria nos serviços e produtos.

## Ferramentas Beneficiadas:

- **Pesquisa de IA do Azure:** Para indexar, consultar e analisar grandes conjuntos de dados.
- **Serviços de IA do Azure:** Para enriquecer os dados com habilidades cognitivas, como OCR e análise de sentimento.
- **Conta de Armazenamento do Azure:** Para armazenar documentos brutos e dados enriquecidos.
  
## Aprendizados Adquiridos:

- A integração de serviços de IA pode automatizar a extração de insights valiosos.
- O repositório de conhecimento oferece uma maneira eficaz de explorar dados enriquecidos.
- A configuração cuidadosa dos índices e indexadores é crucial para resultados precisos.

Este guia fornece uma estrutura para configurar e explorar uma pesquisa de IA no Azure, oferecendo uma base para análise contínua e melhoria das experiências do cliente.
