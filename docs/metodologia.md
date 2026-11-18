# Metodologia — avaliação no iPhone XR

## 1. Delineamento

Pesquisa comparativa entre aplicativos de comunicação (WhatsApp, Telegram e Instagram), com medidas quantitativas (tamanho informado na loja, espaço ocupado e tempo de inicialização) e avaliações qualitativas (fluidez e enquadramento). Unidade experimental: **um iPhone XR**; aplicativos: WhatsApp, Telegram e Instagram.

A proposta original previa dois celulares, mas foi adaptada para um único aparelho disponível. Portanto, não se pretende estimar diferenças entre modelos de smartphone ou entre Android e iOS.

## 2. Caracterização do dispositivo

O dispositivo informado foi **iPhone XR, iOS 18.7.11, 64 GB, 300 MB livres**. A coleta foi realizada em **18/11/2026**. As versões e os dados coletados estão em [dados/medicoes.csv](../dados/medicoes.csv) e a identificação do aparelho em [dados/dispositivo.csv](../dados/dispositivo.csv).

## 3. Padronização

1. Atualizar ou registrar as versões dos três apps; evitar atualizações no meio da coleta.
2. Ao comparar aplicativos no mesmo aparelho, manter o procedimento tão semelhante quanto possível; condições não registradas não devem ser presumidas.
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

Executar roteiro comum no módulo de mensagens de cada aplicativo: abrir lista de conversas, rolar a lista, abrir uma conversa de teste, voltar e acessar configurações. No Instagram, navegar especificamente até Direct e também registrar separadamente o tempo gasto para chegar a essa seção, se pertinente. Classificar como **boa / regular / ruim**, acrescentando exemplos observáveis (travamentos, atraso na resposta ou transições suaves). Evitar acessar dados de terceiros.

### 4.5 Enquadramento na tela

Examinar os mesmos tipos de tela da área de mensagens: lista de conversas, conversa de teste e configurações. Observar botões cortados, sobreposição, legibilidade, espaçamentos e adaptação à área da câmera e às bordas. Classificar como **adequado / problema observado**, com descrição e imagem quando cabível.

### 4.6 Consumo de RAM

A RAM por aplicativo **não é exposta diretamente nos Ajustes do iOS**. Somente registrar valor numérico caso se utilize ferramenta apropriada e se documentem procedimento, unidade e confiabilidade. Sem isso, preencher **não mensurado**; não substituir por uso de bateria ou por armazenamento.

**Justificativa final da RAM:** não foi realizada medição instrumental de RAM dos três aplicativos. O iOS não expõe o consumo de RAM individual por app nos Ajustes; portanto, o critério ficou registrado como **não mensurado** para todos, sem utilizar armazenamento ou bateria como substitutos.

## 5. Registro e análise

As linhas dos três aplicativos foram preenchidas em [dados/medicoes.csv](../dados/medicoes.csv), com valores observados e médias calculadas. As 11 capturas JPEG estão disponíveis em [capturas/](../capturas/), organizadas por dispositivo e aplicativo; o texto interpretativo e os links individuais estão em [relatorio-final.md](relatorio-final.md).

## 6. Limitações

- Apenas um dispositivo e um sistema operacional.
- Diferentes históricos de uso, conteúdos e caches dos aplicativos.
- Cronometragem manual e avaliação subjetiva da fluidez.
- Ausência de métrica direta de RAM sem instrumentação adequada.
- Pesquisa das stacks limitada ao que as empresas tornam público.
- Instagram é uma rede social com diversas funcionalidades além das mensagens; armazenamento e tempo de abertura do app completo não medem somente seu módulo de mensagens.

**Importante:** a metodologia não determina antecipadamente qual app é mais rápido ou qual tecnologia é melhor.
