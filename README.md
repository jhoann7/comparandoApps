# Comparando Apps — Análise de Mercado

Projeto acadêmico de **Desenvolvimento para Dispositivos Móveis** — Prof. Dr. José Augusto de Sena Quaresma.

## Objetivo

Comparar **WhatsApp, Telegram e Instagram** quanto às tecnologias documentadas, tamanho, armazenamento, tempo de inicialização e experiência de interface no **iPhone XR**.

> **Situação:** relatório e análise concluídos com os dados fornecidos em 18/11/2026. Capturas de tela reais e identificação da dupla ainda pendentes.

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
├── capturas/
│   ├── README.md
│   ├── dispositivo/README.md
│   ├── whatsapp/README.md
│   ├── telegram/README.md
│   └── instagram/README.md
└── evidencias/
    └── README.md  (redirecionamento para capturas/)
```

## Documentação

- [Relatório completo: introdução, objetivos, metodologia, resultados, discussão e conclusão](docs/relatorio-final.md)
- [Pesquisa das stacks e classificação com referências](docs/pesquisa-tecnologica.md)
- [Análise comparativa dos resultados](docs/analise-comparativa.md)
- [Metodologia detalhada adaptada para um celular](docs/metodologia.md)
- [Medições originais em CSV](dados/medicoes.csv)
- [Dados do dispositivo em CSV](dados/dispositivo.csv)
- [Guia de capturas de tela](capturas/README.md)

## Capturas de tela a anexar

Coloque as capturas nas pastas abaixo, seguindo os nomes indicados nos seus respectivos READMEs:

- [`capturas/dispositivo/`](capturas/dispositivo/) — iOS e armazenamento do iPhone XR.
- [`capturas/whatsapp/`](capturas/whatsapp/) — App Store, armazenamento e interface.
- [`capturas/telegram/`](capturas/telegram/) — App Store, armazenamento e interface.
- [`capturas/instagram/`](capturas/instagram/) — App Store, armazenamento e Direct.

**Importante:** ocultar dados pessoais em prints. Não alterar valores de medições, nem representar capturas posteriores como se fossem da data original.

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
- [x] Estruturar pastas e orientações de capturas.
- [ ] Anexar capturas reais em suas pastas.
- [ ] Identificar os dois integrantes antes da entrega.

## Limitações

A atividade original propunha dois celulares; aqui foi utilizado apenas o iPhone XR. Também há somente três tempos de abertura por app, dados locais não uniformizados e ausência de instrumentação para RAM. Não é possível atribuir as diferenças de desempenho diretamente às tecnologias usadas. Os 300 MB livres merecem atenção, mas sua influência não foi quantificada.

## Referência da atividade

**Aula03Mobile.pdf**, slides 2 a 4, material de aula fornecido pelos integrantes. O PDF original não foi publicado no repositório.

## Autoria

**Trabalho em dupla:** preencher nome dos integrantes antes da entrega.
