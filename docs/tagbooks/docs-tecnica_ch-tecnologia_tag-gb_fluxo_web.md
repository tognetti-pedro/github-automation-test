# CH Tecnologia - Tagbook fluxo - web

## Link das telas
[Layout do Ambiente](figma-url)

## Perguntas de negócio
1. **qual o nome do app?**
   - **Evento:** `interaction_fluxo`
   - **Dimensão/Parâmetro:** `cd_environment_name` com valor `Tag GB`
   - **Como consultar no GA4:** Criar um relatório de Exploração personalizado (Explore) utilizando a dimensão personalizada `cd_environment_name` cruzada com a métrica de Total de Eventos para identificar o volume de interações realizadas no produto Tag GB.

## Tabela de Eventos
| Índice | Evento | Dimensões | Descrição | Código de Implementação | Observações |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | interaction_fluxo | cd_interaction_detail, cd_vs_name, cd_filter_type, cd_tagging_type, cd_product_type, cd_environment_name | Medir a interação do usuário ao clicar para escolher o arquivo na tela de dados da interface. | dataLayer.push({ "event": "analytics-event", "event_name": "interaction_fluxo", "cd_interaction_detail": "click:escolher-arquivo", "cd_vs_name": "dados-da-interface", "cd_filter_type": "Não se aplica", "cd_tagging_type": "sem-flora", "cd_product_type": "web", "cd_environment_name": "Tag GB" }) | Evento disparado no clique do botão Escolher arquivo. O parâmetro cd_environment_name identifica o nome específico do produto (Tag GB). |

## Documentações para implementação
- [Eventos de Ecommerce Avançado para Plataforma GB](https://alquimia.gb.tech/docs/default/component/analytics-markdown-generator-backstage/guides/implementacao_ecommerce_GA4/)
- [Eventos de Ecommerce Avançado](https://developers.google.com/analytics/devguides/collection/ga4/ecommerce?hl=pt-br)
- [Eventos de interação via Flora](https://sites.google.com/grupoboticario.com.br/martech-digital-analytics/hub-de-conhecimento/treinamentos-valida%C3%A7%C3%B5es/tagueamento/autotagging-flora-ga4)