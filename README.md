# Análise de Sentimento com o Azure AI Language Studio

Neste exercício, você aprenderá a explorar os recursos do Azure AI Language para analisar avaliações de hotéis e determinar se elas são predominantemente positivas ou negativas. Usaremos o **Language Studio** para realizar análises de sentimento, extração de frases-chave e identificação de entidades em textos.

## O que é Processamento de Linguagem Natural (PLN)?

O **Processamento de Linguagem Natural (PLN)** é uma subárea da Inteligência Artificial que lida com a interação entre computadores e linguagens humanas. Ele permite que sistemas entendam, interpretem e respondam a textos ou falas de maneira significativa. Exemplos de aplicações incluem a análise de sentimentos, a extração de entidades e a tradução automática.

## Cenário do Exercício

Suponha que uma agência de viagens fictícia, **Margie’s Travel**, incentive seus clientes a enviarem avaliações sobre suas estadias em hotéis. O objetivo deste exercício é usar o Azure AI Language para:

- **Identificar** se as avaliações são positivas ou negativas.
- **Extrair frases-chave** para melhorar a análise.
- **Analisar menções a entidades**, como locais ou pessoas.

## Passo 1: Criar um Recurso de Linguagem no Azure

1. **Acesse o portal do Azure**: [Portal Azure](https://portal.azure.com).
2. **Criar um Recurso de Linguagem**:
   - No painel, clique em **Criar um recurso** e pesquise por **Serviço de Idioma**.
   - Selecione **Criar um Plano de Serviço de Idioma** e avance conforme as instruções.
3. **Configurações**:
   - **Assinatura**: Selecione a sua assinatura do Azure.
   - **Grupo de Recursos**: Crie ou selecione um grupo de recursos exclusivo.
   - **Região**: Escolha a região mais próxima de sua localização (exemplo: **East US 2**).
   - **Nível de Preço**: Selecione **Free F0** ou **S**, se o Free F0 não estiver disponível.
   - Complete a criação do recurso clicando em **Revisar + Criar** e, em seguida, **Criar**.

![image](https://github.com/user-attachments/assets/2b0d309c-8c56-4420-8097-0c42594105b5)


## Passo 2: Configurar o Recurso no Language Studio

1. **Acesse o Azure Language Studio**: [Language Studio](https://language.cognitive.azure.com) e faça login.
2. **Selecione o Recurso Criado**:
   - Quando solicitado, configure o **Diretório do Azure**, a **Assinatura do Azure** e o **Tipo de Recurso**.
   - Selecione o recurso de **Idioma** que você acabou de criar.

![image](https://github.com/user-attachments/assets/a3918b1b-7ca9-424f-9349-9901fb70aa19)


3. **Confirmar Configuração**: Clique em **Concluído** para finalizar a configuração.

> **Nota**: A partir de julho de 2023, os serviços de IA do Azure passaram a abranger o que antes era denominado **Serviços Cognitivos e Serviços de IA Aplicados do Azure**. Ambos os nomes se referem ao mesmo tipo de serviço.

## Passo 3: Analisar Avaliações no Language Studio

1. **Iniciar Análise de Sentimento**:
   - No **Language Studio**, selecione a aba **Classificar texto** e clique em **Analisar sentimento e extrair opiniões**.
   - Selecione o idioma do texto como **Inglês** e, em seguida, escolha seu **Recurso de Linguagem**.
   
2. **Inserir o Texto**:
   - Insira o seguinte texto de avaliação para análise de sentimento:
   
   ```plaintext
   Eu estou muito feliz com os resultados que obtivemos neste projeto, tudo deu certo e foi uma experiência incrível!
