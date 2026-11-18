# Metodologia — avaliação no iPhone XR

## 1. Delineamento

Pesquisa comparativa, com medidas quantitativas (tamanho informado na loja, espaço ocupado e tempo de inicialização) e avaliações qualitativas (fluidez e enquadramento). Unidade experimental: **um iPhone XR**; aplicativos: WhatsApp, Telegram e Signal.

A proposta original previa dois celulares, mas foi adaptada para um único aparelho disponível. Portanto, não se pretende estimar diferenças entre modelos de smartphone ou entre Android e iOS.

## 2. Caracterização do dispositivo

Antes dos testes, preencher [dados/dispositivo.csv](../dados/dispositivo.csv), incluindo versão do iOS, armazenamento disponível e condições de teste. Registrar versões dos três aplicativos em [dados/medicoes.csv](../dados/medicoes.csv).

## 3. Padronização

1. Atualizar ou registrar as versões dos três apps; evitar atualizações no meio da coleta.
2. Usar a mesma rede Wi-Fi e o mesmo ambiente de teste, com bateria suficiente e sem modo Pouca Energia, ou registrar qualquer exceção.
3. Definir uma tela final comparável: **tela principal pronta para interação**. Autenticação e telas introdutórias não integram o tempo de abertura.
4. Garantir que os aplicativos já estejam instalados, configurados e com as permissões necessárias.
5. Evitar notificações e registrar intercorrências.
6. Executar os testes de forma próxima no tempo. Se possível, alternar a ordem dos aplicativos nas rodadas para reduzir o viés de ordem.

## 4. Medições

### 4.1 Tamanho de download

Consultar o tamanho apresentado na **App Store** para a versão disponível no dia da coleta. Registrar valor, unidade, data e versão. Esse indicador não é necessariamente o mesmo que transferência efetiva de rede.

### 4.2 Tamanho instalado

Consultar **Ajustes > Geral > Armazenamento do iPhone**. Registrar o tamanho do app e, quando disponível, documentos e dados separadamente; o total ocupado pode variar com histórico de mensagens e mídia. Não comparar volumes de dados pessoais como se fossem exclusivamente tamanho do software.

### 4.3 Tempo de inicialização

Para cada aplicativo:

1. Acessar o seletor de apps e encerrar o aplicativo.
2. Partir da tela inicial do iPhone e iniciar a cronometragem no toque no ícone.
3. Parar quando a tela principal estiver renderizada e utilizável.
4. Repetir **três vezes**, usando sempre o mesmo cronômetro externo ou método de gravação e registrando exceções.
5. Calcular a média: **(t1 + t2 + t3) / 3**. Opcionalmente relatar mínimo, máximo e variação.

Três repetições são uma amostra pequena: não inferir diferenças estatisticamente significativas apenas das médias.

### 4.4 Fluidez das animações

Executar roteiro comum: abrir lista de conversas, rolar a lista, abrir uma conversa de teste, voltar e acessar configurações. Classificar como **boa / regular / ruim**, acrescentando exemplos observáveis (travamentos, atraso na resposta ou transições suaves). Evitar acessar dados de terceiros.

### 4.5 Enquadramento na tela

Examinar os mesmos tipos de tela: lista principal, conversa de teste e configurações. Observar botões cortados, sobreposição, legibilidade, espaçamentos e adaptação à área da câmera e às bordas. Classificar como **adequado / problema observado**, com descrição e imagem quando cabível.

### 4.6 Consumo de RAM

A RAM por aplicativo **não é exposta diretamente nos Ajustes do iOS**. Somente registrar valor numérico caso se utilize ferramenta apropriada e se documentem procedimento, unidade e confiabilidade. Sem isso, preencher **não mensurado**; não substituir por uso de bateria ou por armazenamento.

## 5. Registro e análise

Preencher uma linha por aplicativo em [dados/medicoes.csv](../dados/medicoes.csv), com valores observados e média calculada. Registrar evidências conforme [evidencias/README.md](../evidencias/README.md). Confrontar resultados com a pesquisa tecnológica em [docs/pesquisa-tecnologica.md](pesquisa-tecnologica.md).

## 6. Limitações

- Apenas um dispositivo e um sistema operacional.
- Diferentes históricos de uso, conteúdos e caches dos aplicativos.
- Cronometragem manual e avaliação subjetiva da fluidez.
- Ausência de métrica direta de RAM sem instrumentação adequada.
- Pesquisa das stacks limitada ao que as empresas tornam público.

**Importante:** a metodologia não determina antecipadamente qual app é mais rápido ou qual tecnologia é melhor.
