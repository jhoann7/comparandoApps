# Etapa 2 — Pesquisa tecnológica e classificação dos aplicativos

**Data da pesquisa:** 18/11/2026  
**Escopo:** clientes **iOS** de WhatsApp, Telegram e Instagram, para posterior comparação no iPhone XR.  
**Situação:** levantamento documental concluído dentro do escopo público disponível; análise prática e discussão concluídas em [relatorio-final.md](relatorio-final.md).

## 1. Critérios de classificação

- **Finalidade:** plataformas de comunicação digital com recursos de mensagens diretas. Instagram é primariamente uma rede social; WhatsApp e Telegram são mensageiros.
- **Plataforma avaliada:** iOS.
- **Tipo de implementação:** nativo, híbrido ou web, segundo evidências do cliente iOS.
- **Stack:** separar **interface e aplicativo iOS**, **bibliotecas compartilhadas** e **backend**. Uma linguagem usada numa biblioteca não implica que todo o aplicativo seja escrito nela.
- **Nível de evidência:** código público é evidência direta; exigências de vagas de engenharia são indício da stack, mas não descrevem todos os componentes de produção.

## 2. Quadro comparativo

| Critério | WhatsApp | Telegram | Instagram |
| --- | --- | --- | --- |
| Categoria | Mensagens instantâneas | Mensagens instantâneas | Rede social com mensagens diretas |
| Plataforma desta pesquisa | iOS | iOS | iOS |
| Classificação preliminar | Cliente nativo iOS (inferência fundamentada em vagas de engenharia) | Cliente nativo iOS (código-fonte público) | Base nativa iOS, com uso documentado de React Native em algumas experiências |
| Linguagens documentadas | Swift, Objective-C e C++ em requisitos de vagas para iOS; uso exato não verificado | Swift, Objective-C e componentes C/C++ no projeto iOS | Objective-C documentado pela engenharia do Instagram; Swift presente na evolução da stack iOS; componentes React Native em experiências específicas |
| Ferramentas / bibliotecas documentadas | iOS SDK / frameworks, citados em vagas | Xcode e Bazel no guia oficial de compilação | IGListKit (Objective-C, integração Swift), UIKit/UICollectionView e React Native em partes do produto |
| Código-fonte completo do cliente disponível publicamente? | Não verificado nesta pesquisa | Sim, repositório oficial | Não; IGListKit é biblioteca pública, não o app inteiro |
| Backend, banco de dados e infraestrutura | Não determinados nesta pesquisa | Não determinados nesta pesquisa | Não determinados nesta pesquisa |

### WhatsApp

Uma vaga de **engenharia iOS do WhatsApp/Meta** menciona experiência com **Objective-C, C++, Swift e iOS SDK**. Isso sustenta que tais tecnologias são relevantes às equipes de desenvolvimento iOS; **não** permite assegurar qual porcentagem do aplicativo emprega cada uma nem concluir que todo o código usa essas três linguagens. A classificação **nativa** é inferência apoiada pela especialização iOS das vagas, não inspeção pública do aplicativo distribuído.

**Evidência:** [vaga iOS do WhatsApp divulgada no LinkedIn](https://br.linkedin.com/jobs/view/whatsapp-software-engineer-technical-leadership-ios-at-whatsapp-4477773017). Outra reprodução da descrição: [Meta/WhatsApp iOS](https://www.metaintro.com/job/whatsapp-software-engineer-ios-at-meta-d9a2d976-fb64-5629-b4b1-59a5c2928c2c).

**Pendente:** documentação primária de arquitetura do cliente iOS, framework de UI específico, backend e armazenamento.

### Telegram

O Telegram publica o [código-fonte do cliente iOS](https://github.com/TelegramMessenger/Telegram-iOS). No projeto é possível verificar **Swift**, arquivos de **Objective-C** e dependências/componentes **C/C++**. O [guia oficial de compilação](https://github.com/TelegramMessenger/Telegram-iOS/blob/master/README.md) documenta uso de **Xcode** e infraestrutura de build com **Bazel**. A [página oficial de aplicativos do Telegram](https://telegram.org/apps/) informa que seus clientes são de código aberto e oferece informações de verificação de builds.

**Classificação:** cliente iOS nativo, com componentes em diferentes linguagens. Não confundir ferramenta de build (Bazel) com framework de interface.

**Pendente:** documentar bibliotecas específicas de interface e persistência e diferenciar o cliente da infraestrutura de servidor.

### Instagram

A [equipe de engenharia do Instagram](https://medium.com/instagram-engineering/instant-feedback-in-ios-engineering-workflows-c3f6508c76c8) descreveu sua base nativa iOS em **Objective-C** (artigo histórico). Uma [palestra sobre compilação iOS](https://atscaleconference.com/improving-instagram-ios-build-speeds/) relatou que, em 2020, predominava Objective-C e havia código Swift; isso **não determina a proporção atual** de cada linguagem.

A biblioteca [IGListKit](https://instagram.github.io/IGListKit/index.html), publicada pela própria equipe, é baseada em **Objective-C** e interoperável com **Swift**, utilizada pelo aplicativo para listas de conteúdo.

A [engenharia da Meta informou em 2024](https://engineering.fb.com/2024/10/02/android/react-at-meta-connect-2024/) que **React Native** permitiu desenvolver animações e interações no Instagram. Portanto, o aplicativo não deve ser apresentado como **100% nativo sem componentes multiplataforma**, nem como inteiramente construído em React Native.

**Classificação:** aplicativo iOS com base nativa e uso pontual/documentado de React Native. É necessário distinguir a arquitetura predominante das tecnologias usadas em funcionalidades específicas.

**Pendente:** apuração de arquitetura atual por componente, backend e armazenamento, pois o código completo do app não é disponibilizado.


## 3. Discussão inicial — escolhas tecnológicas

Nos três casos, o uso de componentes nativos para iOS é coerente com a necessidade de interação responsiva, notificações, chamadas, acesso aos recursos do aparelho e integração ao sistema. Tecnologias como C/C++, bibliotecas nativas e React Native atendem a necessidades diferentes; estas evidências **não demonstram** superioridade de desempenho.

Uma alternativa hipotética de desenvolvimento multiplataforma seria **React Native** ou **Flutter**, com possível compartilhamento de código. Contudo, afirmar que uma delas seria superior exige discutir manutenção, interoperabilidade, APIs nativas, criptografia, complexidade e testes. Para o Instagram, há relato oficial do uso de React Native em experiências específicas; não extrapolar tal uso para o aplicativo inteiro nem atribuí-lo aos demais sem evidências.

## 4. Limites e cuidados

1. **Stack parcial ≠ stack completa:** os dados aqui dizem respeito principalmente ao cliente iOS.
2. **Vagas ≠ prova de implementação:** habilidades exigidas não comprovam, por si só, uso de uma linguagem em toda a versão de produção.
3. **Classificação do cliente ≠ classificação dos serviços:** backend e infraestrutura são outra camada.
4. **Não correlacionar linguagem e desempenho diretamente:** diferenças de inicialização ou armazenamento podem resultar de cache, mídia, versão, rede e funções oferecidas.
5. A definição exata de “nativo”, “híbrido” e “web” deverá ser conferida com os materiais teóricos da disciplina, se disponibilizados.
6. Instagram possui escopo mais amplo que os mensageiros. Comparar funcionalidades equivalentes (mensagens diretas), relatando que o app também carrega feed, vídeos e outras funções.

## 5. Fontes consultadas

Acesso em **18 nov. 2026**:

1. TELEGRAM. *Telegram Applications*. https://telegram.org/apps/.
2. TELEGRAMMESSENGER. *Telegram-iOS* (repositório). https://github.com/TelegramMessenger/Telegram-iOS.
3. TELEGRAMMESSENGER. *Telegram iOS Source Code Compilation Guide*. https://github.com/TelegramMessenger/Telegram-iOS/blob/master/README.md.
4. INSTAGRAM ENGINEERING. *Instant Feedback in iOS Engineering Workflows*. https://medium.com/instagram-engineering/instant-feedback-in-ios-engineering-workflows-c3f6508c76c8.
5. INSTAGRAM. *IGListKit Reference*. https://instagram.github.io/IGListKit/index.html.
6. META ENGINEERING. *React at Meta Connect 2024*. https://engineering.fb.com/2024/10/02/android/react-at-meta-connect-2024/.
7. AT SCALE. *Improving Instagram iOS Build Speeds*. https://atscaleconference.com/improving-instagram-ios-build-speeds/.
8. WHATSAPP/META. *Software Engineer (Technical Leadership) — iOS* (vaga reproduzida no LinkedIn). https://br.linkedin.com/jobs/view/whatsapp-software-engineer-technical-leadership-ios-at-whatsapp-4477773017.

## 6. Resultado consolidado

A discussão da adequação das escolhas tecnológicas, das alternativas possíveis e das limitações encontra-se em [relatorio-final.md](relatorio-final.md). Os dados instrumentais disponíveis estão em [../dados/medicoes.csv](../dados/medicoes.csv).
