# Relatório — Análise comparativa de aplicativos móveis no iPhone XR

**Disciplina:** Desenvolvimento para Dispositivos Móveis  
**Professor:** Prof. Dr. José Augusto de Sena Quaresma  
**Data da coleta:** 18 de novembro de 2026  
**Autor:** Jhoann Carllos Feitosa Araújo.

## Resumo

O trabalho comparou três aplicativos de comunicação digital disponíveis para iOS — WhatsApp, Telegram e Instagram — em um único iPhone XR, com foco na stack de desenvolvimento, no armazenamento, no tempo de inicialização e na experiência de interface. Foram realizadas três medições de abertura por aplicativo, além de observações de fluidez e enquadramento. O Telegram apresentou a menor média de inicialização (1,12 s), o menor espaço ocupado (230 MB) e boa fluidez. O WhatsApp obteve 1,70 s, fluidez boa e 5,35 GB ocupados; o Instagram apresentou 2,30 s, fluidez regular e 2,63 GB ocupados. Todos tiveram enquadramento considerado adequado. O consumo de memória RAM não foi mensurado diretamente por falta de instrumento confiável no iOS. Os achados descrevem o comportamento observado no aparelho, mas não demonstram superioridade intrínseca de uma stack tecnológica.

**Palavras-chave:** iOS; aplicativos móveis; desempenho; experiência do usuário; análise comparativa.

## 1. Introdução

Os aplicativos móveis são desenvolvidos com diferentes combinações de linguagens, bibliotecas e ferramentas. Tais escolhas podem influenciar a experiência de desenvolvimento e manutenção, a integração com o sistema operacional e o comportamento do aplicativo, mas não bastam, isoladamente, para explicar resultados de desempenho. Esta atividade investiga três aplicativos conhecidos que oferecem mensagens diretas. WhatsApp e Telegram são predominantemente mensageiros, enquanto Instagram é uma rede social que também oferece Direct; essa diferença funcional deve ser considerada.

## 2. Objetivos

**Geral:** comparar tecnologias documentadas e resultados práticos de três aplicativos iOS em um mesmo aparelho.

**Específicos:** (i) identificar e classificar tecnologias do cliente iOS com fontes rastreáveis; (ii) registrar tamanhos informados pela App Store e armazenamento ocupado; (iii) medir três tempos de inicialização por app; (iv) avaliar fluidez e enquadramento; (v) discutir limitações e alternativas de implementação.

## 3. Metodologia

### 3.1 Dispositivo, versões e adaptação

O PDF da atividade previa medições em dois celulares. Em razão da disponibilidade de somente um dispositivo, os testes foram realizados em **um iPhone XR, iOS 18.7.11, capacidade de 64 GB**, com **300 MB de espaço livre informado** no registro do aparelho. A comparação, portanto, é intradispositivo e não pode ser generalizada a outros modelos ou ao Android.

| Aplicativo | Versão testada |
| --- | --- |
| WhatsApp | 26.45.75 |
| Telegram | 13.2.2 |
| Instagram | 456.0.0 |

**Data dos testes:** 18/11/2026.

### 3.2 Procedimentos

O tamanho anunciado foi consultado na App Store; o armazenamento ocupado foi obtido em **Ajustes > Geral > Armazenamento do iPhone**. As medidas não foram decompostas em tamanho do app e documentos/dados; assim, refletem ocupação observada, potencialmente influenciada por conversas, mídias e caches.

Para inicialização, foram coletados três tempos por aplicativo, em segundos, após encerramento e reabertura, até a interface estar utilizável, conforme a metodologia planejada. Calculou-se a média aritmética: **(t1 + t2 + t3) / 3**. A fluidez foi classificada como boa, regular ou ruim e o enquadramento como adequado ou com problemas observados, com base na navegação realizada pelo autor. Não foram coletadas medições instrumentadas de FPS.

### 3.3 Memória RAM — justificativa da não mensuração

O iOS não oferece nos Ajustes uma leitura direta e confiável da **RAM consumida individualmente por cada aplicativo**. Não foi utilizada instrumentação de desenvolvimento apropriada para produzir métricas comparáveis. Por isso, os três registros de RAM foram classificados como **“não mensurado”**. Armazenamento ocupado (GB/MB) e indicadores de bateria não foram utilizados como substitutos, porque medem fenômenos distintos. Essa ausência é uma limitação metodológica explícita, não um resultado zero.

## 4. Pesquisa tecnológica e classificação

A pesquisa se restringe às evidências públicas identificáveis sobre o **cliente iOS**; não pretende reconstruir a stack completa de infraestrutura e servidor.

| App | Classificação e tecnologias documentadas | Grau de certeza |
| --- | --- | --- |
| WhatsApp | Cliente iOS de natureza nativa; vagas de engenharia citam Swift, Objective-C, C++ e SDK iOS | Evidência indireta sobre linguagens; sem inspeção do código completo |
| Telegram | Cliente iOS nativo, com código público em Swift, Objective-C e componentes C/C++; Xcode e Bazel usados no projeto | Evidência direta do repositório oficial |
| Instagram | Base iOS nativa com Objective-C/Swift em documentação de engenharia e uso de componentes React Native em algumas experiências; IGListKit como biblioteca de listas | Evidência pública histórica e parcial; não atribuir toda a aplicação a React Native |

Fontes e ressalvas detalhadas em [pesquisa-tecnologica.md](pesquisa-tecnologica.md). **Nativo** e **uso localizado de tecnologia multiplataforma** não são categorias necessariamente mutuamente excludentes: um app pode integrar módulos de implementação diferente.

## 5. Resultados

### 5.1 Tamanho e armazenamento

| Critério | WhatsApp | Telegram | Instagram |
| --- | ---: | ---: | ---: |
| Tamanho na App Store | 385,3 MB | 167,8 MB | 693,7 MB |
| Armazenamento ocupado no iPhone | 5,35 GB | 230 MB | 2,63 GB |

O Instagram apresentou o maior tamanho indicado pela App Store (693,7 MB). O WhatsApp ocupou mais espaço no aparelho (5,35 GB), enquanto o Telegram apresentou a menor ocupação (230 MB). Esses indicadores têm naturezas distintas e dependem do estado de cada aplicativo. Não se deve interpretar a diferença entre os dois valores como RAM ou como uma medida isolada de eficiência de código.

### 5.2 Tempo de inicialização

| Aplicativo | Medição 1 | Medição 2 | Medição 3 | Média |
| --- | ---: | ---: | ---: | ---: |
| WhatsApp | 1,74 s | 1,62 s | 1,73 s | **1,70 s** |
| Telegram | 1,37 s | 1,15 s | 0,85 s | **1,12 s** |
| Instagram | 1,35 s | 1,34 s | 4,22 s | **2,30 s** |

O Telegram teve a menor média das três aberturas e o Instagram a maior. A terceira observação do Instagram (4,22 s) foi substancialmente superior às duas primeiras (1,35 s e 1,34 s), elevando a média. O dado foi preservado. O tamanho reduzido da amostra não permite inferência estatística robusta, e não foi estabelecida a causa dessa variação.

### 5.3 Fluidez e enquadramento

| Aplicativo | Fluidez | Enquadramento | Observações relatadas |
| --- | --- | --- | --- |
| WhatsApp | Boa | Adequado | Nenhuma |
| Telegram | Boa | Adequado | Nenhuma |
| Instagram | Regular | Adequado | Nenhuma |

Todos os três aplicativos tiveram interfaces consideradas adequadamente enquadradas na tela do iPhone XR. WhatsApp e Telegram foram avaliados como fluidos; Instagram recebeu classificação regular. As categorias são **avaliações subjetivas**, não medições instrumentais de quadros por segundo.

## 6. Discussão fundamentada

### 6.1 A escolha tecnológica foi adequada?

**WhatsApp:** os indícios de desenvolvimento orientado ao iOS são coerentes com requisitos de integração à plataforma, notificações, chamadas e uso constante. A boa fluidez e o tempo médio de 1,70 s são observações compatíveis com uma experiência funcional no aparelho testado, mas não provam que Swift, Objective-C ou C++ sejam a causa. Seus 5,35 GB ocupados podem refletir o histórico de mídia e mensagens, não somente o tamanho do aplicativo.

**Telegram:** o código público documenta uma implementação iOS nativa com diferentes componentes e ferramentas de build. No teste, apresentou inicialização média de 1,12 s, fluidez boa e menor armazenamento ocupado. A stack é plausível para um produto complexo que requer recursos específicos da plataforma; porém, a pesquisa não controlou conteúdo, cache ou outras diferenças necessárias para atribuir os resultados exclusivamente à arquitetura.

**Instagram:** fontes técnicas descrevem uma base nativa para iOS e a utilização de React Native em determinadas experiências, sem demonstrar que todo o aplicativo seja desenvolvido nessa tecnologia. A combinação pode ser apropriada para um produto com feed, mídia e mensagens diretas, ao permitir integração com APIs da plataforma e compartilhamento de implementação em partes do produto. A fluidez regular e a abertura média de 2,30 s no iPhone XR não provam que React Native tenha causado degradação: o Instagram oferece funcionalidades distintas das dos mensageiros, e a terceira abertura destoou das demais.

### 6.2 Seria melhor escolher outra tecnologia?

Uma implementação inteiramente dedicada ao iOS (por exemplo, Swift com ferramentas nativas) pode favorecer integração e ajustes específicos da plataforma, mas tende a exigir implementações separadas para outros sistemas. **React Native** e **Flutter** são alternativas hipotéticas para equipes que desejam maior compartilhamento de código entre plataformas. Nenhuma delas é automaticamente mais rápida, menor ou melhor: a escolha depende de funcionalidade, perfil da equipe, manutenção, acessibilidade, segurança, bibliotecas e necessidade de integração nativa.

Para aplicativos de mensagens com notificações, criptografia e chamadas, uma solução mista — interface nativa ou multiplataforma com módulos nativos para recursos especializados — pode ser viável. Para o Instagram, não seria possível defender uma substituição integral da stack atual com base apenas nas medições feitas aqui. Assim, **não há evidência suficiente para recomendar categoricamente a troca de tecnologia de nenhum dos três produtos**.

### 6.3 Problemas, observações e limites

1. **Apenas um aparelho:** os achados pertencem ao iPhone XR e às versões informadas, não ao mercado inteiro.
2. **Pouco espaço livre:** foram informados apenas 300 MB disponíveis; isso é uma condição potencialmente relevante, mas sua influência não foi isolada experimentalmente.
3. **Três repetições:** amostra pequena para generalizações; a terceira abertura do Instagram merece atenção, não exclusão automática.
4. **RAM sem medição:** limitação justificada pela ausência de ferramenta apropriada; não confundir com armazenamento.
5. **Dados locais não padronizados:** conteúdo de conversas, cache, mídia e uso anterior podem afetar ocupação e desempenho.
6. **Diferença de finalidade:** Instagram é uma rede social com Direct, enquanto os outros dois são mensageiros; as funcionalidades e as telas iniciais não são perfeitamente equivalentes.
7. **Stack incompleta:** apenas tecnologias documentadas foram citadas; não há confirmação de toda a arquitetura dos aplicativos.

## 7. Conclusão

No conjunto de testes realizados em **18/11/2026** no **iPhone XR (iOS 18.7.11)**, o **Telegram apresentou o melhor resultado observado nos indicadores de inicialização e armazenamento**: média de 1,12 segundo, ocupação de 230 MB, boa fluidez e enquadramento adequado. O **WhatsApp** também apresentou boa fluidez e enquadramento adequado, mas ocupou 5,35 GB e teve tempo médio de 1,70 segundo. O **Instagram** apresentou tamanho de 693,7 MB na App Store, 2,63 GB ocupados, tempo médio de 2,30 segundos e fluidez regular, sem problemas relatados de enquadramento.

A pesquisa tecnológica indica diferentes combinações de tecnologias nativas e componentes compartilhados. Entretanto, os resultados não são suficientes para concluir que uma linguagem ou framework específico seja superior ou responsável pelo desempenho constatado. O estudo cumpre o objetivo de comparar dados práticos e escolhas tecnológicas sob condições de um mesmo dispositivo, desde que seus limites sejam explicitados. A coleta de RAM não foi realizada por ausência de instrumentação apropriada. As 11 capturas JPEG foram organizadas no repositório como evidências documentais de interface, informações do dispositivo, App Store e armazenamento.

## 8. Registros visuais

Os arquivos JPEG presentes no repositório documentam as telas indicadas abaixo. Sua existência e nomenclatura foram verificadas; o conteúdo visual não foi auditado nesta revisão.

| Aplicativo / dispositivo | Registros |
| --- | --- |
| iPhone XR | [Informações](../capturas/dispositivo/01-sobre-iphone.jpeg) · [Armazenamento](../capturas/dispositivo/02-armazenamento-iphone.jpeg) |
| WhatsApp | [App Store](../capturas/whatsapp/01-app-store.jpeg) · [Armazenamento](../capturas/whatsapp/02-armazenamento.jpeg) · [Interface](../capturas/whatsapp/03-interface.jpeg) |
| Telegram | [App Store](../capturas/telegram/01-app-store.jpeg) · [Armazenamento](../capturas/telegram/02-armazenamento.jpeg) · [Interface](../capturas/telegram/03-interface.jpeg) |
| Instagram | [App Store](../capturas/instagram/01-app-store.jpeg) · [Armazenamento](../capturas/instagram/02-armazenamento.jpeg) · [Direct](../capturas/instagram/03-interface-direct.jpeg) |

## 9. Referências e documentação

- Material da disciplina: **Aula03Mobile.pdf**, slides 2 a 4, utilizado como referência na atividade.
- TELEGRAMMESSENGER. *Telegram-iOS*. https://github.com/TelegramMessenger/Telegram-iOS. Acesso em: 18 nov. 2026.
- TELEGRAM. *Telegram Applications*. https://telegram.org/apps/. Acesso em: 18 nov. 2026.
- INSTAGRAM. *IGListKit*. https://instagram.github.io/IGListKit/index.html. Acesso em: 18 nov. 2026.
- META ENGINEERING. *React at Meta Connect 2024*. https://engineering.fb.com/2024/10/02/android/react-at-meta-connect-2024/. Acesso em: 18 nov. 2026.
- INSTAGRAM ENGINEERING. *Instant Feedback in iOS Engineering Workflows*. https://medium.com/instagram-engineering/instant-feedback-in-ios-engineering-workflows-c3f6508c76c8. Acesso em: 18 nov. 2026.
- WHATSAPP/META. *Software Engineer (Technical Leadership) — iOS*, vaga referenciada na pesquisa. https://br.linkedin.com/jobs/view/whatsapp-software-engineer-technical-leadership-ios-at-whatsapp-4477773017. Acesso em: 18 nov. 2026.
- Para mais detalhes e ressalvas de fonte, consultar [pesquisa-tecnologica.md](pesquisa-tecnologica.md).

---

**Situação da documentação:** texto conclusivo elaborado a partir dos dados fornecidos. **Documentação consolidada:** 11 arquivos JPEG disponíveis em `capturas/`, sem auditoria visual de seu conteúdo nesta revisão. Autor: Jhoann Carllos Feitosa Araújo.
