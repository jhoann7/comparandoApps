# Comparando Apps — Análise de Mercado

Projeto acadêmico de **Desenvolvimento para Dispositivos Móveis** — Prof. Dr. José Augusto de Sena Quaresma.

## Objetivo

Comparar **WhatsApp, Telegram e Instagram** quanto às tecnologias documentadas, tamanho, armazenamento, tempo de inicialização e experiência de interface no **iPhone XR**.

> **Situação:** pesquisa e relatório concluídos; 11 capturas JPEG organizadas no repositório, com autoria individual identificada.

## Dados da pesquisa

| Aparelho | Sistema | Capacidade | Espaço livre informado | Data da coleta |
| --- | --- | --- | --- | --- |
| iPhone XR | iOS 18.7.11 | 64 GB | 300 MB | 18/11/2026 |

| Aplicativo | Versão | App Store | Armazenamento no iPhone | Média de abertura | Fluidez | Enquadramento |
| --- | --- | ---: | ---: | ---: | --- | --- |
| WhatsApp | 26.45.75 | 385,3 MB | 5,35 GB | 1,70 s | Boa | Adequado |
| Telegram | 13.2.2 | 167,8 MB | 230 MB | **1,12 s** | Boa | Adequado |
| Instagram | 456.0.0 | 693,7 MB | 2,63 GB | 2,30 s | Regular | Adequado |

*Os tempos são médias de três aberturas. Valores individuais em [dados/medicoes.csv](dados/medicoes.csv). Não foram mensurados valores de RAM por aplicativo: os Ajustes do iOS não expõem essa métrica e não houve instrumentação apropriada.*

**Interpretação:** o Telegram apresentou o menor tempo médio e menor ocupação no aparelho testado. Essas observações **não demonstram** que sua stack seja melhor que as outras, pois os aplicativos e seus dados locais são diferentes. Instagram é uma rede social com Direct, e não um mensageiro exclusivamente dedicado.

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

**Observação:** existência, nomes e extensão dos arquivos foram verificados no GitHub; o conteúdo visual de cada JPEG não foi auditado nesta revisão. Se houver dados pessoais identificáveis, recomenda-se ocultá-los antes de divulgação pública.

## Checklist

- [x] Selecionar aplicativos e definir escopo.
- [x] Adaptar testes para um iPhone XR.
- [x] Registrar iOS, capacidade, espaço livre, versões dos apps e data dos testes.
- [x] Pesquisar stacks e classificar os clientes iOS com ressalvas.
- [x] Registrar tamanhos na App Store e armazenamento ocupado.
- [x] Registrar três tempos de inicialização e calcular médias.
- [x] Registrar fluidez e enquadramento.
- [x] Documentar a impossibilidade da medição direta de RAM.
- [x] Concluir discussão fundamentada e relatório textual.
- [x] Organizar e anexar 11 capturas JPEG nas pastas do dispositivo e dos três aplicativos.
- [x] Identificar o autor do trabalho: Jhoann Carllos Feitosa Araújo.

## Limitações

A atividade original propunha dois celulares; aqui foi utilizado apenas o iPhone XR. Também há somente três tempos de abertura por app, dados locais não uniformizados e ausência de instrumentação para RAM. Não é possível atribuir as diferenças de desempenho diretamente às tecnologias usadas. Os 300 MB livres merecem atenção, mas sua influência não foi quantificada.

## Referência da atividade

**Aula03Mobile.pdf**, slides 2 a 4, material de aula utilizado nesta pesquisa. O PDF original não foi publicado no repositório.

## Autoria

**Jhoann Carllos Feitosa Araújo** — autor e responsável pelo desenvolvimento da pesquisa, coleta das medições e documentação.
