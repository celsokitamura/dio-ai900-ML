# Trabalhando com Machine Learning na Prática no Azure ML

## Criar um espaço de trabalho do Aprendizado de Máquina do Azure

1. Entre no portal do Azure ao usar suas credenciais da Microsoft.https://portal.azure.com

2. Selecione + Criar um recurso, procure Aprendizado de Máquina e crie um novo recurso de Aprendizado de Máquina do Azure

3. Selecione Revisar + criar e, em seguida, selecione Criar. Aguarde até que seu espaço de trabalho seja criado (pode levar alguns minutos) e vá para o recurso implantado.

4. Selecione Iniciar estúdio (ou abra uma nova guia do navegador e navegue até https://ml.azure.com e entre no estúdio do Aprendizado de Máquina do Azure usando sua conta da Microsoft). Feche todas as mensagens exibidas.

5. No estúdio de Aprendizado de Máquina do Azure, você deve ver seu espaço de trabalho recém-criado. Caso contrário, selecione Todos os espaços de trabalho no menu à esquerda e, em seguida, selecione o espaço de trabalho que você acabou de criar.

## Usar o aprendizado de máquina automatizado para treinar um modelo

1. No estúdio de Aprendizado de Máquina do Azure, exiba a página ML automatizada (em Criação).

2. Crie um novo trabalho de ML automatizado com as seguintes configurações, usando Avançar conforme necessário para progredir pela interface do usuário:

3. Envie o trabalho de treinamento. Ele começa automaticamente.

4. Aguarde a conclusão do trabalho. Pode demorar um pouco – agora pode ser um bom momento para uma pausa para o café!

## Reveja o melhor modelo

1. Na guia Visão geral do trabalho de aprendizado de máquina automatizado, observe o melhor resumo do modelo. Captura de tela do melhor resumo de modelo do trabalho de aprendizado de máquina automatizado com uma caixa ao redor do nome do algoritmo.

2. Selecione o texto em Nome do algoritmo para o melhor modelo para exibir seus detalhes.

3. Selecione a guia Métricas e selecione os gráficos de resíduos e predicted_true se ainda não estiverem selecionados.

Analise os gráficos que mostram o desempenho do modelo. O gráfico de resíduos mostra os resíduos (as diferenças entre os valores previstos e reais) como um histograma. O gráfico predicted_true compara os valores previstos com os valores verdadeiros.

## Implantar e testar o modelo

1. Na guia Modelo para obter o melhor modelo treinado pelo seu trabalho de aprendizado de máquina automatizado, selecione Implantar e usar a opção Serviço Web para implantar o modelo

2. Aguarde o início da implantação - isso pode levar alguns segundos. O status de implantação para o ponto de extremidade de aluguel de previsão será indicado na parte principal da página como Em execução.

3. Aguarde até que o status Implantar seja alterado para Bem-sucedido. Isso pode levar de 5 a 10 minutos.

## Testar o serviço implantado

1. No estúdio do Aprendizado de Máquina do Azure, no menu à esquerda, selecione Pontos de extremidade e abra o ponto de extremidade em tempo real de aluguéis de previsão.

2. Na página de ponto de extremidade em tempo real de aluguéis de previsão, exiba a guia Teste.

3. No painel Dados de entrada para testar o ponto de extremidade, substitua o modelo JSON pelos seguintes dados de entrada:

4. Clique no botão Testar.

5. Analise os resultados do teste, que incluem um número previsto de aluguéis com base nos recursos de entrada

O painel de teste pegou os dados de entrada e usou o modelo treinado para retornar o número previsto de aluguéis.

## Limpeza

### Exclua o ponto de extremidade para evitar o uso desnecessário do Azure

1. No estúdio do Aprendizado de Máquina do Azure, na guia Pontos de extremidade, selecione o ponto de extremidade de aluguel de previsão. Em seguida, selecione Excluir e confirme que deseja excluir o ponto de extremidade.

### Para excluir seu espaço de trabalho:

1. No portal do Azure, na página Grupos de recursos, abra o grupo de recursos especificado ao criar seu espaço de trabalho do Aprendizado de Máquina do Azure.

2. Clique em Excluir grupo de recursos, digite o nome do grupo de recursos para confirmar que deseja excluí-lo e selecione Excluir.

