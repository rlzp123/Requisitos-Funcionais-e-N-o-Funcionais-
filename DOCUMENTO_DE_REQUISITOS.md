# Documento de Requisitos — Industrial Control Tower

**Versão:** 1.0  
**Status:** Em planejamento  
**Tipo de projeto:** Desenvolvimento de software  
**Ambiente inicial:** Simulação industrial com dados fictícios

---

## 1. Apresentação

O Industrial Control Tower é uma plataforma web proposta para acompanhar e integrar informações de diferentes áreas de uma operação industrial. A ideia é reunir dados de pedidos, estoque, produção e logística em um só lugar, facilitando a identificação de problemas e o acompanhamento dos resultados.

Na primeira etapa, o sistema será desenvolvido em um ambiente de simulação. Os dados serão fictícios, mas deverão representar situações possíveis em uma indústria de fabricação de cabos.

## 2. Problema que o sistema pretende resolver

Cada setor da indústria trabalha com informações próprias. Quando esses dados ficam separados, pode ser difícil perceber como um problema em uma área afeta as demais.

Um exemplo é a falta de matéria-prima: ela pode impedir o andamento de uma ordem de produção, comprometer um pedido e gerar atraso na entrega.

O sistema pretende facilitar a visualização dessas relações, reunindo informações e destacando situações que precisam de atenção.

## 3. Objetivos

### 3.1 Objetivo geral

Desenvolver uma plataforma web que integre informações de diferentes setores industriais, apresente indicadores e ajude a identificar riscos e gargalos da operação.

### 3.2 Objetivos específicos

- Centralizar informações operacionais.
- Acompanhar pedidos e prazos de entrega.
- Consultar a disponibilidade de matérias-primas.
- Monitorar ordens e linhas de produção.
- Identificar possíveis atrasos e gargalos.
- Relacionar ocorrências entre departamentos.
- Gerar alertas para situações críticas.
- Apresentar indicadores em painéis.
- Permitir a importação de dados por planilhas.
- Apoiar a tomada de decisões com análises e recomendações.

## 4. Usuários do sistema

O sistema deverá atender pessoas com diferentes responsabilidades na operação.

| Perfil | Uso previsto |
|---|---|
| Administrador | Gerenciar usuários e configurações. |
| Gestor industrial | Acompanhar os indicadores gerais. |
| Planejador de produção | Consultar capacidade e programação. |
| Responsável pelo estoque | Acompanhar materiais e disponibilidade. |
| Responsável comercial | Consultar pedidos e prazos. |
| Responsável pela logística | Acompanhar entregas. |

As permissões de cada perfil deverão ser definidas durante o planejamento detalhado.

## 5. Escopo e módulos

### 5.1 Dashboard executivo

Deverá apresentar uma visão geral da operação, incluindo:

- Quantidade de pedidos em andamento.
- Pedidos com risco de atraso.
- Situação do estoque.
- Ordens de produção em andamento.
- Utilização da capacidade produtiva.
- Alertas operacionais.
- Gráficos de desempenho.

### 5.2 Monitoramento de pedidos

Deverá permitir cadastrar e acompanhar pedidos, com informações como cliente, produtos, quantidade, data de recebimento, prazo de entrega e status. Também deverá relacionar pedidos às ordens de produção e destacar possíveis riscos de atraso.

### 5.3 Gestão de estoque

Deverá permitir cadastrar matérias-primas e acompanhar quantidade disponível, estoque mínimo, movimentações e consumo. O módulo também deverá ajudar a identificar materiais críticos e necessidades de abastecimento.

### 5.4 Monitoramento da produção

Deverá permitir cadastrar linhas e ordens de produção, consultar produtos fabricados, quantidades planejadas e produzidas, capacidade, datas previstas e status. Também deverá ajudar a identificar atrasos e gargalos.

### 5.5 Inteligência operacional

Deverá cruzar informações dos setores para identificar situações que possam afetar a operação, como riscos de atraso, falta de materiais, excesso de demanda em uma linha e dependências entre departamentos. As análises poderão apresentar estimativas de impacto e recomendações.

### 5.6 Central de alertas

Deverá reunir alertas relacionados a pedidos, estoque e produção. Os alertas poderão ser classificados por criticidade, consultados posteriormente e acompanhados até sua resolução.

## 6. Requisitos funcionais

Os requisitos funcionais descrevem as ações que o sistema deverá oferecer.

| Código | Requisito |
|---|---|
| RF01 | O sistema deve permitir a autenticação de usuários. |
| RF02 | O sistema deve permitir o cadastro de pedidos. |
| RF03 | O sistema deve permitir o cadastro de matérias-primas. |
| RF04 | O sistema deve permitir o controle de estoque. |
| RF05 | O sistema deve permitir o cadastro de linhas de produção. |
| RF06 | O sistema deve permitir o cadastro de ordens de produção. |
| RF07 | O sistema deve apresentar indicadores operacionais. |
| RF08 | O sistema deve identificar pedidos com risco de atraso. |
| RF09 | O sistema deve identificar riscos de falta de materiais. |
| RF10 | O sistema deve identificar gargalos produtivos. |
| RF11 | O sistema deve gerar alertas operacionais. |
| RF12 | O sistema deve permitir a importação de planilhas. |
| RF13 | O sistema deve relacionar informações entre departamentos. |
| RF14 | O sistema deve apresentar recomendações operacionais. |

## 7. Requisitos não funcionais

Os requisitos não funcionais definem características de qualidade e condições técnicas esperadas.

| Código | Requisito |
|---|---|
| RNF01 | A aplicação deverá possuir interface responsiva. |
| RNF02 | O sistema deverá utilizar autenticação segura. |
| RNF03 | O banco de dados deverá manter a integridade referencial. |
| RNF04 | As APIs deverão possuir validação de dados. |
| RNF05 | O sistema deverá apresentar mensagens de erro compreensíveis. |
| RNF06 | O sistema deverá possuir estrutura modular. |
| RNF07 | Os dados deverão possuir mecanismos de proteção e controle de acesso. |
| RNF08 | O sistema deverá permitir evolução e integração futura. |

## 8. Cenários de uso

### 8.1 Pedido com risco de atraso

O sistema identifica um pedido com prazo próximo cuja ordem de produção ainda não foi iniciada. A situação deverá ser destacada para que a gestão possa acompanhar o risco.

### 8.2 Risco de falta de matéria-prima

O sistema compara o estoque disponível com o consumo previsto, identifica ordens afetadas e apresenta um alerta de abastecimento.

### 8.3 Gargalo produtivo

O sistema compara a capacidade de uma linha com a demanda programada. Quando a demanda ultrapassar a capacidade disponível, deverá indicar as ordens possivelmente afetadas.

### 8.4 Impacto entre departamentos

Uma matéria-prima indisponível pode comprometer uma ordem de produção, afetar um pedido e exigir a reprogramação de uma entrega. O sistema deverá relacionar essas informações para facilitar a análise do impacto.

## 9. Arquitetura prevista

A arquitetura inicial considera a separação entre interface, backend, processamento de dados e armazenamento.

| Camada | Tecnologia prevista | Responsabilidade |
|---|---|---|
| Frontend | React | Interface e dashboards. |
| Estilização | CSS | Layout e identidade visual. |
| Backend | Node.js e Express | APIs e regras de negócio. |
| Processamento | Python, Pandas e Scikit-learn | Análise e tratamento de dados. |
| Banco de dados | PostgreSQL | Armazenamento relacional. |
| Importação | Excel e CSV | Entrada de dados externos. |

### 9.1 Fluxo básico

1. Os dados são cadastrados ou importados.
2. O backend valida e organiza as informações.
3. Os dados são armazenados no PostgreSQL.
4. O processamento analisa as informações necessárias.
5. Os resultados são disponibilizados por APIs.
6. A interface apresenta indicadores, alertas e recomendações.

## 10. Dados previstos

As principais entidades consideradas inicialmente são:

- Usuários.
- Clientes.
- Pedidos e itens dos pedidos.
- Produtos.
- Matérias-primas.
- Estoque e movimentações.
- Linhas de produção.
- Ordens de produção.
- Consumo de materiais.
- Registros de produção.
- Entregas.
- Alertas.
- Ocorrências operacionais.

O modelo definitivo e os relacionamentos entre essas entidades ainda deverão ser definidos na etapa de modelagem do banco de dados.

## 11. Ambiente de simulação

Como não há acesso autorizado aos sistemas internos da empresa de referência, a primeira versão utilizará dados fictícios.

A base inicial é uma estimativa e poderá mudar durante o desenvolvimento.

| Entidade | Quantidade estimada |
|---|---:|
| Pedidos | 100 |
| Matérias-primas | 30 |
| Linhas de produção | 5 |
| Clientes | 20 |
| Ordens de produção | 80 |
| Registros históricos | A definir |
| Ocorrências operacionais | A definir |

A simulação deverá permitir testar pedidos com prazos diferentes, falta de materiais, atrasos, capacidades distintas nas linhas, mudanças na programação e impactos nas entregas.

## 12. Primeira versão (MVP)

A primeira versão deverá priorizar:

1. Autenticação de usuários.
2. Dashboard executivo.
3. Cadastro e acompanhamento de pedidos.
4. Cadastro e controle de estoque.
5. Cadastro de linhas e ordens de produção.
6. Regras básicas para identificar riscos.
7. Central de alertas.
8. Importação de dados fictícios.

Modelos preditivos, otimização automática da produção e integrações com sistemas industriais ficam como possibilidades para versões futuras.

## 13. Restrições e premissas

- Os dados utilizados inicialmente serão fictícios.
- Não haverá integração com sistemas internos da Prysmian sem autorização.
- As recomendações serão inicialmente baseadas em regras de negócio.
- Modelos de aprendizado de máquina dependerão da disponibilidade de dados adequados.
- A plataforma será inicialmente uma aplicação web.
- O sistema não deverá alterar programações industriais reais de forma autônoma.
- As recomendações deverão ser avaliadas pelos responsáveis pela operação.

## 14. Etapas previstas de desenvolvimento

| Etapa | Principais atividades |
|---|---|
| Planejamento | Definir requisitos, MVP, regras e equipe. |
| Estrutura técnica | Configurar frontend, backend, banco e APIs. |
| Módulos | Desenvolver dashboard, pedidos, estoque, produção e alertas. |
| Inteligência operacional | Criar regras de risco, cruzamento de dados e recomendações. |
| Testes | Validar cenários, integrações e consistência dos dados. |
| Apresentação | Preparar o ambiente demonstrativo e documentar os resultados. |

## 15. Pontos que ainda precisam ser definidos

Algumas decisões permanecem em aberto e deverão ser discutidas antes ou durante a implementação:

- Quais funcionalidades serão obrigatórias no MVP?
- Qual será o fluxo completo dos pedidos?
- Como será feito o relacionamento entre estoque e produção?
- Quais indicadores serão exibidos no dashboard?
- Quais regras serão usadas para classificar os riscos?
- Como ficará o modelo definitivo do banco de dados?
- Como serão divididas as responsabilidades da equipe?
- Qual será o cronograma de desenvolvimento?

## 16. Considerações finais

O Industrial Control Tower pretende facilitar o acompanhamento da operação industrial, reunindo informações que normalmente ficam distribuídas entre diferentes setores. Com isso, a equipe poderá visualizar melhor os impactos de problemas no estoque, na produção, nos pedidos e nas entregas.

Este documento reúne a proposta inicial do sistema. Ele deverá ser atualizado conforme o escopo, as regras de negócio e as decisões técnicas forem definidos.

---

**Documento de requisitos do sistema — Industrial Control Tower**  
**Versão 1.0**
