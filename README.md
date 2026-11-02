# 🛠️ Supervisório de Manutenção Industrial

**Da abertura à conclusão: acompanhe suas ordens de serviço em um só painel.**

![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=flat-square&logo=googlesheets&logoColor=white)
![Licença: a definir](https://img.shields.io/badge/Licen%C3%A7a-a%20definir-lightgrey?style=flat-square)
![Status: a informar](https://img.shields.io/badge/Status-a%20informar-lightgrey?style=flat-square)

**Status do projeto:** [INFORMAR STATUS DO PROJETO]

<!-- Atualize os badges de licença e status após preencher as informações. Adicione badges de outras tecnologias somente depois de confirmar seu uso. -->

## Visão geral

A falta de visibilidade sobre as solicitações de manutenção dificulta o acompanhamento das demandas no chão de fábrica: quais equipamentos precisam de atendimento, quais ordens estão em execução e quais já foram concluídas?

Este projeto é um **supervisório de manutenção industrial em Google Sheets** para abrir, acompanhar e finalizar Ordens de Serviço (OS), com visualização em tempo real do andamento das requisições.

A aba **PAINEL** reúne indicadores, listas por status e os dados das OS ativas. A aba **BASE** mantém os dados brutos e o histórico das ordens de serviço.

**Demonstração ou modelo da planilha:** [LINK]

> O uso de Google Forms e Google Apps Script ainda precisa ser confirmado: [CONFIRMAR TECNOLOGIAS E SUAS FUNÇÕES].

## 🎬 Demonstração

Os exemplos abaixo apresentam o ciclo de uma OS e a visão geral do painel.

<!--
Preparação dos GIFs:
1. Crie uma pasta assets na mesma pasta do README.md.
2. Identifique o conteúdo de cada animação e renomeie os arquivos:
   - 01-os-pendente.gif
   - 02-os-atuando.gif
   - 03-os-concluida.gif
   - 04-visao-geral.gif
3. Confira a correspondência dos quatro arquivos originais:
   Video-Project-3.gif, Video-Project-3-_1_.gif,
   Video-Project-5.gif e Video-Project-6.gif.
4. Remova os comentários de troca após validar as animações.
-->

### 1. Chegada de uma nova OS

![Nova OS com status PENDENTE em vermelho no painel](./assets/01-os-pendente.gif) <!-- trocar pelo GIF correto -->

*Uma nova requisição aparece como PENDENTE, com o cronômetro em execução e o aumento do contador de pendências.*

### 2. Atendimento em andamento

![OS com mantenedor atribuído e status ATUANDO em amarelo](./assets/02-os-atuando.gif) <!-- trocar pelo GIF correto -->

*Com o mantenedor atribuído, a OS passa para ATUANDO e os contadores e percentuais são atualizados.*

### 3. Conclusão da OS

![Conclusão de uma OS e atualização dos indicadores do painel](./assets/03-os-concluida.gif) <!-- trocar pelo GIF correto -->

*A OS deixa a tabela ativa, aumenta a contagem de concluídas e tem seu número incluído na lista de requisições concluídas.*

### 4. Visão geral do painel

![Visão geral do supervisório de manutenção industrial](./assets/04-visao-geral.gif) <!-- trocar pelo GIF correto -->

*O painel reúne indicadores, listas de requisições por status, ordens ativas e acesso ao relatório de OS.*

## Funcionalidades

- 📊 **Indicadores de manutenção:** contadores de OS pendentes, em atendimento, concluídas e total, acompanhados de percentuais e barras coloridas por status.
- 🔎 **Requisições agrupadas:** listas dos números de requisição separadas por status.
- 📋 **Tabela de OS ativas:** visualização dos dados necessários para acompanhar cada atendimento.
- ⏱️ **Cronômetro automático por OS:** tempo decorrido no formato `0d 00:02:08`.
- 🚦 **Identificação visual dos status:** vermelho para PENDENTE, amarelo para ATUANDO e verde para CONCLUÍDO.
- 📄 **Relatório de OS:** botão dedicado à geração do relatório das ordens de serviço.
- 🗂️ **Histórico centralizado:** armazenamento dos dados brutos e das OS na aba BASE.

### Dados exibidos na tabela ativa

| Campo | Informação |
| --- | --- |
| REQ | Número da requisição |
| Carimbo de data/hora | Data e hora registradas para a solicitação |
| Nome do solicitante | Identificação de quem abriu a OS |
| Setor | Setor relacionado à solicitação |
| Equipamento | Equipamento informado na OS |
| Descrição do problema | Problema relatado pelo solicitante |
| Mantenedor | Responsável atribuído ao atendimento |
| Status | Situação atual da OS |
| Cronômetro | Tempo decorrido exibido para a OS |

## ⚙️ Como funciona

**🔴 PENDENTE → 🟡 ATUANDO → 🟢 CONCLUÍDO**

| Etapa | O que acontece | Efeito no painel |
| --- | --- | --- |
| **PENDENTE** | O solicitante abre uma requisição. | A OS aparece na tabela ativa, com destaque vermelho e cronômetro em execução. A contagem de pendentes é atualizada. |
| **ATUANDO** | Um mantenedor é atribuído e a OS passa para atendimento. | O status fica amarelo, e os indicadores e as listas refletem a mudança. |
| **CONCLUÍDO** | O atendimento é finalizado. | A OS sai da tabela ativa, passa a integrar a contagem de concluídas e aparece na lista de requisições concluídas. |

O histórico das ordens de serviço fica armazenado na aba **BASE**.

### Procedimentos operacionais

- **Abertura de OS:** [FORMULÁRIO / DIGITAÇÃO MANUAL / OUTRO]
- **Atribuição do mantenedor:** [DESCREVER]
- **Finalização da OS:** [DESCREVER]
- **Geração do relatório:** [DESCREVER]
- **Formato do relatório:** [DESCREVER — PDF, PLANILHA OU OUTRO]
- **Referência de início e regra de encerramento do cronômetro:** [DESCREVER]
- **Mecanismo e frequência de atualização do painel:** [DESCREVER]

## Estrutura da planilha

| Aba | Finalidade | Conteúdo |
| --- | --- | --- |
| **PAINEL** | Acompanhar a situação da manutenção. | Contadores, percentuais, barras por status, listas de requisições, tabela de OS ativas, cronômetros e botão **Relatório de OS**. |
| **BASE** | Armazenar os registros das ordens de serviço. | Dados brutos e histórico de todas as OS. |

## 🚀 Como instalar e usar

### Preparação

1. **Acesse a demonstração ou o modelo da planilha.**  
   Link: [](https://docs.google.com/spreadsheets/d/1dXLN3grWKeStdwWQfBYL_hHtlB_8AJS1MB_oO4I5byU/edit?usp=sharing)]]

2. **Crie sua cópia seguindo as instruções do projeto.**  
   Procedimento para copiar o modelo: [DESCREVER]

3. **Confira os requisitos de acesso.**  
   Conta, permissões e compartilhamento necessários: [DESCREVER]

4. **Realize a configuração inicial.**  
   Configurações da planilha e de eventuais integrações: [DESCREVER]  
   Caso Google Forms ou Google Apps Script façam parte do projeto, documente aqui os vínculos, as autorizações e as etapas necessárias: [DESCREVER / NÃO SE APLICA]

### Operação

5. **Abra uma OS.**  
   Método de abertura: [FORMULÁRIO / DIGITAÇÃO MANUAL / OUTRO]  
   Instruções de preenchimento: [DESCREVER]

6. **Acompanhe a requisição na aba PAINEL.**  
   Localize o número da REQ e confira o status **PENDENTE**, os dados da solicitação e o cronômetro.

7. **Atribua o mantenedor e inicie o atendimento.**  
   Procedimento: [DESCREVER]  
   Confira a mudança para **ATUANDO** e a atualização dos indicadores.

8. **Finalize a OS após o atendimento.**  
   Procedimento: [DESCREVER]  
   Confira sua saída da tabela ativa e sua inclusão na contagem e na lista de concluídas.

9. **Consulte o histórico ou gere um relatório.**  
   Utilize a aba **BASE** para consultar os registros e o botão **Relatório de OS** para gerar o relatório.  
   Etapas de geração e formato de saída: [DESCREVER]

## Tecnologias utilizadas

| Tecnologia | Aplicação no projeto |
| --- | --- |
| **Google Sheets** | Interface do supervisório, painel de acompanhamento e armazenamento dos registros nas abas PAINEL e BASE. |
| **[CONFIRMAR: Google Forms]** | [DESCREVER A FUNÇÃO OU REMOVER SE NÃO FOR UTILIZADO] |
| **[CONFIRMAR: Google Apps Script]** | [DESCREVER A FUNÇÃO OU REMOVER SE NÃO FOR UTILIZADO] |
| **[OUTRAS TECNOLOGIAS, SE HOUVER]** | [DESCREVER OU REMOVER] |

**Lista final de tecnologias:** [Google Sheets, Apps Script, etc.]

## Possíveis melhorias futuras

As sugestões abaixo são possibilidades de evolução; não representam funcionalidades já implementadas nem um compromisso de entrega.

- [ ] Classificar OS por prioridade ou criticidade.
- [ ] Adicionar filtros por setor, equipamento, mantenedor e período.
- [ ] Notificar responsáveis sobre novas requisições e mudanças de status.
- [ ] Incluir indicadores de tempo de espera e duração dos atendimentos.
- [ ] Permitir o registro de observações e evidências da manutenção.
- [ ] Criar análises de recorrência de falhas por equipamento.
- [ ] Ampliar a documentação de configuração e uso.

## Autor e licença

**João Victor Olinto Bernardo**

- **Contato:** joaobernardo0590@gmail.com

**Licença:** [MIT / outra]

<!-- Após definir a licença, inclua o arquivo LICENSE no repositório e atualize o badge no início deste README. -->
