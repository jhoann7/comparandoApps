# Análise comparativa — resultados e discussão

**Autor:** Jhoann Carllos Feitosa Araújo.

> **Análise concluída com os dados disponíveis** (18/11/2026; WhatsApp 26.45.75, Telegram 13.2.2, Instagram 456.0.0). Ver também [relatório completo](relatorio-final.md). Capturas ainda pendentes.

## 1. Síntese dos resultados

Resultados registrados:

| Critério | WhatsApp | Telegram | Instagram |
| --- | --- | --- | --- |
| Tamanho na App Store | 385,3 MB | 167,8 MB | 693,7 MB |
| Armazenamento ocupado | 5,35 GB | 230 MB | 2,63 GB |
| Tempo médio de abertura (n = 3) | **1,70 s** | **1,12 s** | **2,30 s** |
| Fluidez | **Boa** | **Boa** | **Regular** |
| Enquadramento | **Adequado** | **Adequado** | **Adequado** |
| RAM | Não mensurado* | Não mensurado* | Não mensurado* |

*Manter como não mensurado caso não haja instrumentação apropriada. Os valores são os informados pelo usuário para o iPhone XR; não houve separação de tamanho do app versus documentos e dados. Conversão dos valores em GB para a planilha feita na convenção decimal (1 GB = 1.000 MB). Data da coleta: 18/11/2026. Versões: WhatsApp 26.45.75; Telegram 13.2.2; Instagram 456.0.0.

### Tempos individuais de inicialização

| Aplicativo | Medição 1 | Medição 2 | Medição 3 | Média calculada |
| --- | ---: | ---: | ---: | ---: |
| WhatsApp | 1,74 s | 1,62 s | 1,73 s | 1,6967 s (≈ 1,70 s) |
| Telegram | 1,37 s | 1,15 s | 0,85 s | 1,1233 s (≈ 1,12 s) |
| Instagram | 1,35 s | 1,34 s | 4,22 s | 2,3033 s (≈ 2,30 s) |

**Cálculo:** média = (t1 + t2 + t3) / 3. Todos os tempos em segundos. Os resultados foram coletados pelo autor em um único iPhone XR; a data e as versões dos apps estão registradas.

**Interpretação preliminar:** Telegram teve a menor média, seguido de WhatsApp e Instagram. A terceira abertura do Instagram (4,22 s) foi muito superior às duas primeiras (1,35 s e 1,34 s) e influenciou sua média. Manter esse valor no conjunto original; uma repetição futura pode investigar a variação, sem substituir silenciosamente o dado. O armazenamento livre previamente informado foi 300 MB, mas não há prova de que tenha provocado o tempo elevado. Apenas três repetições por app não sustentam conclusão geral sobre desempenho nem causalidade tecnológica.

### Observações preliminares

- WhatsApp apresenta maior ocupação no aparelho (5,35 GB).
- Telegram apresenta menor ocupação no aparelho (230 MB).
- Instagram apresenta maior tamanho listado na App Store (693,7 MB).
- Não há base para concluir superioridade de otimização: dados de usuário, mídias, cache e histórico podem contribuir para diferenças.

### Avaliação qualitativa de navegação e interface

- **WhatsApp:** fluidez boa e enquadramento adequado; não foram registradas observações adicionais.
- **Telegram:** fluidez boa e enquadramento adequado; não foram registradas observações adicionais.
- **Instagram:** fluidez regular e enquadramento adequado; não foram registradas observações adicionais ou indicação específica de atrasos.
- Os três aplicativos tiveram enquadramento considerado adequado no iPhone XR. O Instagram teve avaliação subjetiva de fluidez inferior às dos mensageiros, mas não é possível determinar a causa apenas com essa classificação.
- A avaliação é qualitativa e específica do dispositivo e das condições de teste; não equivale a medição de FPS ou RAM.

## 2. Interpretação dos resultados

**Telegram:** menor média de inicialização (1,12 s), menor espaço ocupado (230 MB), fluidez boa e enquadramento adequado. É o melhor resultado observado para esses indicadores neste iPhone XR, não uma prova de superioridade da stack.

**WhatsApp:** média de 1,70 s, ocupação de 5,35 GB e fluidez boa; o armazenamento também pode incluir mídias e histórico de conversas.

**Instagram:** média de 2,30 s e fluidez regular; a terceira abertura de 4,22 s destoou das outras duas. Como rede social, possui escopo funcional mais amplo do que os mensageiros.

## 3. Análise fundamentada das tecnologias

- **WhatsApp:** vagas de engenharia iOS mencionam Swift, Objective-C e C++; essa evidência não revela toda a implementação. A boa experiência observada é compatível com um cliente iOS funcional, sem estabelecer causalidade entre linguagem e velocidade.
- **Telegram:** cliente iOS de código público com Swift, Objective-C, componentes C/C++ e ferramentas de build Xcode/Bazel. Sua inicialização observada foi menor, mas cache e conteúdo dos apps não foram controlados.
- **Instagram:** documentação histórica e de engenharia relata Objective-C/Swift, IGListKit e componentes React Native em experiências específicas. A fluidez regular observada não prova que o uso de React Native seja a causa.

Alternativas como **Swift nativo**, **React Native** ou **Flutter** podem ser consideradas conforme compartilhamento de código, manutenção, integração ao sistema, segurança e escopo das funcionalidades. Não há evidência suficiente nestes testes para recomendar mudança de stack de qualquer um dos três.

## 4. Memória RAM e limitações

O iOS não fornece nos Ajustes o consumo de RAM individual dos aplicativos. Sem instrumentação específica, esse critério foi registrado como **não mensurado** para todos os três. Armazenamento em MB ou GB não equivale à RAM.

Limitações adicionais: um único dispositivo; três repetições; 300 MB livres informados; conteúdo e caches não padronizados; avaliação subjetiva de fluidez; finalidades diferentes dos apps. Nenhuma dessas limitações autoriza modificar ou descartar valores observados.

## 5. Conclusão

No iPhone XR analisado em 18/11/2026, o Telegram apresentou os menores valores observados de tempo médio de inicialização e armazenamento ocupado, com boa fluidez e enquadramento adequado. WhatsApp também teve boa fluidez, enquanto Instagram foi avaliado com fluidez regular. Não foi possível demonstrar que as diferenças decorram das stacks tecnológicas. A pesquisa documental e os testes são informativos para o contexto específico, mas não generalizáveis para outras plataformas.

Para desenvolvimento completo da discussão e referências, consultar o [relatório final](relatorio-final.md) e a [pesquisa tecnológica](pesquisa-tecnologica.md).
