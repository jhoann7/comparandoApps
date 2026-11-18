# Análise comparativa — modelo para preenchimento

> **Coleta parcial registrada:** tamanhos informados na App Store, armazenamento ocupado no iPhone XR e três tempos de inicialização por aplicativo. Fluidez e enquadramento foram avaliados qualitativamente; RAM não foi mensurada. Não transformar hipóteses em conclusões.

## 1. Síntese dos resultados

Preencher após os testes:

| Critério | WhatsApp | Telegram | Instagram |
| --- | --- | --- | --- |
| Tamanho na App Store | 385,3 MB | 167,8 MB | 693,7 MB |
| Armazenamento ocupado | 5,35 GB | 230 MB | 2,63 GB |
| Tempo médio de abertura (n = 3) | **1,70 s** | **1,12 s** | **2,30 s** |
| Fluidez | **Boa** | **Boa** | **Regular** |
| Enquadramento | **Adequado** | **Adequado** | **Adequado** |
| RAM | Não mensurado* | Não mensurado* | Não mensurado* |

*Manter como não mensurado caso não haja instrumentação apropriada. Os valores são os informados pelo usuário para o iPhone XR; não houve separação de tamanho do app versus documentos e dados. Conversão dos valores em GB para a planilha feita na convenção decimal (1 GB = 1.000 MB). Data exata e versões dos apps ainda não registradas.

### Tempos individuais de inicialização

| Aplicativo | Medição 1 | Medição 2 | Medição 3 | Média calculada |
| --- | ---: | ---: | ---: | ---: |
| WhatsApp | 1,74 s | 1,62 s | 1,73 s | 1,6967 s (≈ 1,70 s) |
| Telegram | 1,37 s | 1,15 s | 0,85 s | 1,1233 s (≈ 1,12 s) |
| Instagram | 1,35 s | 1,34 s | 4,22 s | 2,3033 s (≈ 2,30 s) |

**Cálculo:** média = (t1 + t2 + t3) / 3. Todos os tempos em segundos. Os resultados foram informados pela equipe para um único iPhone XR; as versões dos apps, data exata e condições de rede ainda estão pendentes.

**Interpretação preliminar:** Telegram teve a menor média, seguido de WhatsApp e Instagram. A terceira abertura do Instagram (4,22 s) foi muito superior às duas primeiras (1,35 s e 1,34 s) e influenciou sua média. Manter esse valor no conjunto original; uma repetição futura pode investigar a variação, sem substituir silenciosamente o dado. O armazenamento livre previamente informado foi 300 MB, mas não há prova de que tenha provocado o tempo elevado. Apenas três repetições por app não sustentam conclusão geral sobre desempenho nem causalidade tecnológica.

### Observações preliminares

- WhatsApp apresenta maior ocupação no aparelho (5,35 GB).
- Telegram apresenta menor ocupação no aparelho (230 MB).
- Instagram apresenta maior tamanho listado na App Store (693,7 MB).
- Não há base para concluir superioridade de otimização: dados de usuário, mídias, cache e histórico podem contribuir para diferenças.

### Avaliação qualitativa de navegação e interface

- **WhatsApp:** fluidez boa e enquadramento adequado; equipe não relatou observações adicionais.
- **Telegram:** fluidez boa e enquadramento adequado; equipe não relatou observações adicionais.
- **Instagram:** fluidez regular e enquadramento adequado; equipe não relatou observações adicionais ou localização específica de atrasos.
- Os três aplicativos tiveram enquadramento considerado adequado no iPhone XR. O Instagram teve avaliação subjetiva de fluidez inferior às dos mensageiros, mas não é possível determinar a causa apenas com essa classificação.
- A avaliação é qualitativa e específica do dispositivo e das condições de teste; não equivale a medição de FPS ou RAM.

## 2. Interpretação

- Qual aplicativo apresentou menor tempo médio de inicialização? A diferença pode refletir conexão, cache, estado de sessão ou conteúdo?
- O armazenamento ocupado reflete apenas o app ou também mídias/documentos?
- Foram observados travamentos ou problemas de interface? Em quais telas?
- Quais características de mensagens são comuns aos três aplicativos?
- Como o feed, os vídeos e outras funções do Instagram limitam comparações diretas com mensageiros dedicados?
- Os dados permitem inferir causalidade da stack no desempenho? **Em geral, não isoladamente.**

## 3. Escolhas tecnológicas

Para cada aplicativo, discutir:
1. Evidências documentais de tecnologias de desenvolvimento.
2. Adequação dessas tecnologias ao objetivo do app.
3. Possíveis alternativas e compromissos (desempenho, manutenção, desenvolvimento multiplataforma, segurança e experiência).
4. Limites das conclusões: comparação empírica em um único iPhone XR não demonstra que determinada linguagem/framework seja superior.

## 4. Problemas e observações

Registrar falhas de acesso, conexão, autenticação, diferenças de conteúdo, inconsistências entre medidas, mudança de versão e restrições da plataforma iOS.

## 5. Conclusão

Produzir somente após levantamento tecnológico, medições e evidências. Destacar escopo, limitações e achados sustentados pelos dados.
