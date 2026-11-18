# Etapa 2 — Pesquisa tecnológica e classificação dos aplicativos

**Data da pesquisa:** 18/11/2026  
**Escopo:** clientes **iOS** de WhatsApp, Telegram e Signal, para posterior comparação no iPhone XR.  
**Situação:** pesquisa documental preliminar concluída; medições práticas ainda pendentes.

## 1. Critérios de classificação

- **Finalidade:** comunicação / mensagens instantâneas.
- **Plataforma avaliada:** iOS.
- **Tipo de implementação:** nativo, híbrido ou web, segundo evidências do cliente iOS.
- **Stack:** separar **interface e aplicativo iOS**, **bibliotecas compartilhadas** e **backend**. Uma linguagem usada numa biblioteca não implica que todo o aplicativo seja escrito nela.
- **Nível de evidência:** código público é evidência direta; exigências de vagas de engenharia são indício da stack, mas não descrevem todos os componentes de produção.

## 2. Quadro comparativo

| Critério | WhatsApp | Telegram | Signal |
| --- | --- | --- | --- |
| Categoria | Mensagens instantâneas | Mensagens instantâneas | Mensagens instantâneas |
| Plataforma desta pesquisa | iOS | iOS | iOS |
| Classificação preliminar | Cliente nativo iOS (inferência fundamentada em vagas de engenharia) | Cliente nativo iOS (código-fonte público) | Cliente nativo iOS (código-fonte público) |
| Linguagens documentadas | Swift, Objective-C e C++ em requisitos de vagas para iOS; uso exato não verificado | Swift, Objective-C e componentes C/C++ no projeto iOS | Swift, Objective-C no projeto iOS; Rust na biblioteca compartilhada libsignal |
| Ferramentas / bibliotecas documentadas | iOS SDK / frameworks, citados em vagas | Xcode e Bazel no guia oficial de compilação | Xcode, CocoaPods, libsignal (Swift binding para código Rust) |
| Código-fonte completo do cliente disponível publicamente? | Não verificado nesta pesquisa | Sim, repositório oficial | Sim, repositório oficial |
| Backend, banco de dados e infraestrutura | Não determinados nesta pesquisa | Não determinados nesta pesquisa | Não determinados nesta pesquisa |

### WhatsApp

Uma vaga de **engenharia iOS do WhatsApp/Meta** menciona experiência com **Objective-C, C++, Swift e iOS SDK**. Isso sustenta que tais tecnologias são relevantes às equipes de desenvolvimento iOS; **não** permite assegurar qual porcentagem do aplicativo emprega cada uma nem concluir que todo o código usa essas três linguagens. A classificação **nativa** é inferência apoiada pela especialização iOS das vagas, não inspeção pública do aplicativo distribuído.

**Evidência:** [vaga iOS do WhatsApp divulgada no LinkedIn](https://br.linkedin.com/jobs/view/whatsapp-software-engineer-technical-leadership-ios-at-whatsapp-4477773017). Outra reprodução da descrição: [Meta/WhatsApp iOS](https://www.metaintro.com/job/whatsapp-software-engineer-ios-at-meta-d9a2d976-fb64-5629-b4b1-59a5c2928c2c).

**Pendente:** documentação primária de arquitetura do cliente iOS, framework de UI específico, backend e armazenamento.

### Telegram

O Telegram publica o [código-fonte do cliente iOS](https://github.com/TelegramMessenger/Telegram-iOS). No projeto é possível verificar **Swift**, arquivos de **Objective-C** e dependências/componentes **C/C++**. O [guia oficial de compilação](https://github.com/TelegramMessenger/Telegram-iOS/blob/master/README.md) documenta uso de **Xcode** e infraestrutura de build com **Bazel**. A [página oficial de aplicativos do Telegram](https://telegram.org/apps/) informa que seus clientes são de código aberto e oferece informações de verificação de builds.

**Classificação:** cliente iOS nativo, com componentes em diferentes linguagens. Não confundir ferramenta de build (Bazel) com framework de interface.

**Pendente:** documentar bibliotecas específicas de interface e persistência e diferenciar o cliente da infraestrutura de servidor.

### Signal

O [código-fonte oficial do Signal para iOS](https://github.com/signalapp/Signal-iOS) evidencia desenvolvimento para a plataforma Apple, incluindo **Swift** e componentes **Objective-C**. O arquivo [SignalApp.swift](https://github.com/signalapp/Signal-iOS/blob/main/Signal/AppLaunch/SignalApp.swift) é exemplo direto de código Swift do cliente. A biblioteca [libsignal](https://github.com/signalapp/libsignal/blob/main/swift/README.md) descreve bindings Swift para uma implementação de componentes compartilhados em **Rust** por meio de interface FFI em C.

**Classificação:** cliente iOS nativo que integra biblioteca compartilhada de baixo nível. **Rust não deve ser apresentado como a linguagem de toda a interface do Signal.**

**Pendente:** identificar com precisão bibliotecas de UI/persistência e a arquitetura de servidor a partir de documentação específica.

## 3. Discussão inicial — escolhas tecnológicas

Nos três casos, o desenvolvimento dedicado ao iOS é coerente com a necessidade de interação responsiva, notificações, chamadas, acesso aos recursos do aparelho e integração ao sistema. O emprego de componentes compartilhados em C/C++ ou Rust pode facilitar reaproveitamento de funcionalidades entre plataformas, mas esta pesquisa documental **não demonstra** superioridade de desempenho.

Uma alternativa hipotética de desenvolvimento multiplataforma seria **React Native** ou **Flutter**, com possível compartilhamento de código. Contudo, afirmar que uma delas seria superior exige discutir manutenção, interoperabilidade, APIs nativas, criptografia, complexidade e testes. Não atribuir a WhatsApp, Telegram ou Signal o uso dessas tecnologias sem evidência.

## 4. Limites e cuidados

1. **Stack parcial ≠ stack completa:** os dados aqui dizem respeito principalmente ao cliente iOS.
2. **Vagas ≠ prova de implementação:** habilidades exigidas não comprovam, por si só, uso de uma linguagem em toda a versão de produção.
3. **Classificação do cliente ≠ classificação dos serviços:** backend e infraestrutura são outra camada.
4. **Não correlacionar linguagem e desempenho diretamente:** diferenças de inicialização ou armazenamento podem resultar de cache, mídia, versão, rede e funções oferecidas.
5. A definição exata de “nativo”, “híbrido” e “web” deverá ser conferida com os materiais teóricos da disciplina, se disponibilizados.

## 5. Fontes consultadas

Acesso em **18 nov. 2026**:

1. TELEGRAM. *Telegram Applications*. https://telegram.org/apps/.
2. TELEGRAMMESSENGER. *Telegram-iOS* (repositório). https://github.com/TelegramMessenger/Telegram-iOS.
3. TELEGRAMMESSENGER. *Telegram iOS Source Code Compilation Guide*. https://github.com/TelegramMessenger/Telegram-iOS/blob/master/README.md.
4. SIGNALAPP. *Signal-iOS* (repositório). https://github.com/signalapp/Signal-iOS.
5. SIGNALAPP. *SignalApp.swift*. https://github.com/signalapp/Signal-iOS/blob/main/Signal/AppLaunch/SignalApp.swift.
6. SIGNALAPP. *libsignal — Swift binding README*. https://github.com/signalapp/libsignal/blob/main/swift/README.md.
7. WHATSAPP/META. *Software Engineer (Technical Leadership) — iOS* (vaga reproduzida no LinkedIn). https://br.linkedin.com/jobs/view/whatsapp-software-engineer-technical-leadership-ios-at-whatsapp-4477773017.

## 6. Próxima etapa

Preencher [../dados/dispositivo.csv](../dados/dispositivo.csv) com as configurações reais do iPhone XR e [../dados/medicoes.csv](../dados/medicoes.csv) com os resultados medidos, usando [metodologia.md](metodologia.md). Depois integrar os números e observações à [análise comparativa](analise-comparativa.md).
