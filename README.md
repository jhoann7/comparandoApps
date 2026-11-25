# Comparando Apps — Análise de Mercado

Trabalho da disciplina de **Desenvolvimento para Dispositivos Móveis** — Prof. Dr. José Augusto de Sena Quaresma.

## Objetivo

Comparar as tecnologias documentadas, tamanho, armazenamento, tempo de inicialização e experiência de interface no **iPhone XR** dos aplicativos: **WhatsApp, Telegram e Instagram**. Obs: No instagram, foi levado em consideração apenas o sistema de mensagens (direct).

## Dados da pesquisa

| Aparelho | Sistema | Capacidade | Espaço livre | Data da coleta |
| --- | --- | --- | --- | --- |
| iPhone XR | iOS 18.7.11 | 64 GB | 300 MB | 18/11/2026 |

| Aplicativo | Versão | Tamanho na App Store | Armazenamento no iPhone | Média de abertura | Fluidez | Enquadramento |
| --- | --- | ---: | ---: | ---: | --- | --- |
| WhatsApp | 26.45.75 | 385,3 MB | 5,35 GB | 1,70 s | Boa | Adequado |
| Telegram | 13.2.2 | 167,8 MB | 230 MB | **1,12 s** | Boa | Adequado |
| Instagram | 456.0.0 | 693,7 MB | 2,63 GB | 2,30 s | Regular | Adequado |

*Os tempos são médias de três aberturas. Valores individuais em [dados/medicoes.csv](dados/medicoes.csv). Não foram mensurados valores de RAM por aplicativo: os Ajustes do iOS não expõem essa métrica e não houve instrumentação apropriada.*

**Interpretação:** o Telegram apresentou o menor tempo médio e menor ocupação de memória no aparelho celular. Essas observações **não demonstram** que sua stack seja melhor que as outras, pois os aplicativos e seus dados locais são diferentes. Instagram é uma rede social com Direct, e não um mensageiro exclusivamente dedicado.

## Estrutura do repositório

```text
comparandoApps/
├── README.md
├── docs/
│   ├── metodologia.md
│   ├── pesquisa-tecnologica.md
│   ├── analise-comparativa.md
│   └── relatorio-final.md
├── dados/
│   ├── dispositivo.csv
│   └── medicoes.csv
└── capturas/
    ├── dispositivo/
    │   ├── 01-sobre-iphone.jpeg
    │   └── 02-armazenamento-iphone.jpeg
    ├── whatsapp/
    │   ├── 01-app-store.jpeg
    │   ├── 02-armazenamento.jpeg
    │   └── 03-interface.jpeg
    ├── telegram/
    │   ├── 01-app-store.jpeg
    │   ├── 02-armazenamento.jpeg
    │   └── 03-interface.jpeg
    └── instagram/
        ├── 01-app-store.jpeg
        ├── 02-armazenamento.jpeg
        └── 03-interface-direct.jpeg
```

## Documentação

- [Relatório completo: introdução, objetivos, metodologia, resultados, discussão e conclusão](docs/relatorio-final.md)
- [Pesquisa das stacks e classificação com referências](docs/pesquisa-tecnologica.md)
- [Análise comparativa dos resultados](docs/analise-comparativa.md)
- [Metodologia detalhada adaptada para um celular](docs/metodologia.md)
- [Medições originais em CSV](dados/medicoes.csv)
- [Dados do dispositivo em CSV](dados/dispositivo.csv)
- [Capturas JPEG organizadas por aplicativo](capturas/)

## Capturas de tela

As 11 imagens JPEG estão organizadas e acessíveis em:

| Área | App Store | Armazenamento | Interface / versão do iPhone |
| --- | --- | --- | --- |
| iPhone XR | — | [Armazenamento](capturas/dispositivo/02-armazenamento-iphone.jpeg) | [Informações do aparelho](capturas/dispositivo/01-sobre-iphone.jpeg) |
| WhatsApp | [App Store](capturas/whatsapp/01-app-store.jpeg) | [Armazenamento](capturas/whatsapp/02-armazenamento.jpeg) | [Interface](capturas/whatsapp/03-interface.jpeg) |
| Telegram | [App Store](capturas/telegram/01-app-store.jpeg) | [Armazenamento](capturas/telegram/02-armazenamento.jpeg) | [Interface](capturas/telegram/03-interface.jpeg) |
| Instagram | [App Store](capturas/instagram/01-app-store.jpeg) | [Armazenamento](capturas/instagram/02-armazenamento.jpeg) | [Direct](capturas/instagram/03-interface-direct.jpeg) |
