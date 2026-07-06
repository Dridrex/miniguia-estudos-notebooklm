# Miniguia de Estudos com NotebookLM: APIs REST Seguras para Integração de Sistemas

## 1. Contexto e Objetivos

Este projeto foi desenvolvido como parte de um desafio prático da DIO com o objetivo de usar Inteligência Artificial como ferramenta de aprendizagem ativa. O tema escolhido foi:

> **APIs REST seguras para integração de sistemas**

Escolhi esse tema porque ele se conecta diretamente com minha trajetória em TI, automação e desenvolvimento. Atualmente estudo e pratico conceitos relacionados a APIs, integração entre sistemas, automação de processos, dados, Git/GitHub e segurança da informação. Também venho trabalhando em uma API para comunicação entre sistemas, o que torna o assunto útil tanto para estudo quanto para aplicação prática.

### Objetivos de estudo

- Entender melhor os fundamentos de APIs REST.
- Revisar conceitos importantes de HTTP, recursos, métodos e códigos de status.
- Compreender boas práticas de design de APIs.
- Estudar riscos comuns de segurança em APIs.
- Organizar um conjunto de prompts reutilizáveis para revisar o tema no NotebookLM.
- Criar um material de consulta que possa ser usado futuramente em projetos de backend, automação e integração de sistemas.

## 2. Curadoria de Fontes

As fontes abaixo foram selecionadas por serem abertas, confiáveis e úteis para estudar APIs, HTTP, design de serviços e segurança.

### Fonte 1: MDN Web Docs - HTTP

- Link: https://developer.mozilla.org/en-US/docs/Web/HTTP
- Tipo: documentação aberta em texto.
- Motivo da escolha: a MDN é uma referência prática para revisar fundamentos de HTTP, métodos, cabeçalhos, mensagens, status codes e comportamento cliente-servidor.

### Fonte 2: Microsoft REST API Guidelines

- Link: https://github.com/microsoft/api-guidelines
- Tipo: documentação aberta em repositório GitHub.
- Motivo da escolha: apresenta diretrizes de design de APIs REST usadas como referência para consistência, versionamento, nomenclatura, erros e padrões de resposta.

### Fonte 3: Google Cloud API Design Guide

- Link: https://cloud.google.com/apis/design
- Tipo: guia aberto em texto.
- Motivo da escolha: ajuda a entender design orientado a recursos, padrões de nomenclatura, métodos, coleções e boas práticas para APIs em ambientes de escala.

### Fonte 4: OWASP API Security Project

- Link: https://owasp.org/API-Security/
- Tipo: documentação aberta de segurança.
- Motivo da escolha: a OWASP é uma referência mundial em segurança de aplicações. O projeto de segurança de APIs ajuda a entender riscos como controle de acesso quebrado, autenticação fraca, exposição excessiva de dados e consumo inseguro de APIs.

### Fonte 5: PostgreSQL Documentation - Tutorial

- Link: https://www.postgresql.org/docs/current/tutorial.html
- Tipo: documentação aberta em texto.
- Motivo da escolha: bancos relacionais são muito usados em APIs. A documentação do PostgreSQL ajuda a revisar conceitos de tabelas, consultas, filtros e organização de dados para persistência.

## 3. Como usei o NotebookLM

O processo proposto para uso no NotebookLM foi:

1. Criar um novo caderno temático.
2. Fazer upload ou adicionar links das fontes selecionadas.
3. Solicitar resumos estruturados por fonte.
4. Comparar conceitos entre as fontes.
5. Gerar glossário.
6. Pedir exemplos práticos.
7. Refinar os prompts quando as respostas ficassem genéricas.
8. Consolidar o material final em formato de miniguia.

## 4. Engenharia de Prompts e Cicatrizes

Esta seção documenta os prompts estratégicos usados, variações testadas e dificuldades encontradas.

### Prompt 1: resumo inicial do tema

```text
Com base nas fontes adicionadas, explique o que é uma API REST para uma pessoa que está começando em desenvolvimento backend. Use exemplos simples e organize a resposta em tópicos.
```

**Objetivo:** obter uma explicação inicial clara.

**Resultado esperado:** um resumo com conceitos como cliente, servidor, recurso, endpoint, método HTTP e resposta.

**Cicatriz:** quando o prompt era muito amplo, a IA respondia de forma genérica. A melhoria foi pedir explicitamente "para uma pessoa que está começando" e "organize em tópicos".

### Prompt 2: comparação entre design e segurança

```text
Compare boas práticas de design de APIs REST com boas práticas de segurança de APIs. Separe a resposta em duas colunas: decisões de design e riscos de segurança relacionados.
```

**Objetivo:** conectar arquitetura com segurança.

**Resultado esperado:** associação entre design de endpoints, autenticação, validação, controle de acesso, erros e exposição de dados.

**Cicatriz:** a IA inicialmente misturava design com implementação. A melhoria foi pedir duas colunas e exigir relação direta com riscos de segurança.

### Prompt 3: checklist prático

```text
Crie um checklist prático para revisar uma API REST antes de publicá-la. Inclua itens de HTTP, design, banco de dados, autenticação, autorização, tratamento de erros, logs e documentação.
```

**Objetivo:** transformar o estudo em ferramenta aplicável.

**Resultado esperado:** checklist útil para projetos reais.

**Cicatriz:** a primeira resposta trouxe muitos itens teóricos. A melhoria foi pedir "antes de publicá-la" para tornar a resposta mais operacional.

### Prompt 4: glossário

```text
Crie um glossário com os principais conceitos das fontes estudadas. Para cada termo, traga uma definição curta e um exemplo prático em contexto de API REST.
```

**Objetivo:** consolidar vocabulário técnico.

**Resultado esperado:** termos como endpoint, recurso, payload, autenticação, autorização, status code, idempotência, paginação e rate limit.

**Cicatriz:** algumas definições vieram longas demais. A melhoria foi pedir "definição curta" e "exemplo prático".

### Prompt 5: revisão ativa

```text
Crie 15 perguntas de revisão sobre APIs REST seguras, divididas em fácil, médio e difícil. Depois, forneça um gabarito comentado.
```

**Objetivo:** transformar a IA em ferramenta de estudo ativo.

**Resultado esperado:** perguntas para testar compreensão.

**Cicatriz:** sem pedir níveis de dificuldade, as perguntas ficavam muito parecidas. A divisão em fácil, médio e difícil melhorou a progressão do estudo.

## 5. Miniguia de Estudo

### 5.1 O que é uma API REST?

Uma API REST é uma forma de comunicação entre sistemas usando recursos representados por URLs e operações realizadas principalmente com métodos HTTP.

Exemplo:

```text
GET /clientes
POST /clientes
GET /clientes/10
PUT /clientes/10
DELETE /clientes/10
```

Nesse exemplo, `clientes` é um recurso. Cada método HTTP representa uma intenção diferente.

### 5.2 Conceitos principais

**Cliente:** aplicação que faz a requisição, como um navegador, app mobile ou sistema externo.

**Servidor:** sistema que recebe a requisição, processa a regra de negócio e devolve uma resposta.

**Endpoint:** endereço usado para acessar um recurso ou ação da API.

**Recurso:** entidade principal manipulada pela API, como cliente, pedido, produto ou usuário.

**Payload:** corpo da requisição ou resposta, geralmente em JSON.

**Status code:** código HTTP que indica o resultado da operação.

**Autenticação:** processo de confirmar quem é o usuário ou sistema.

**Autorização:** processo de verificar o que o usuário ou sistema pode acessar.

### 5.3 Métodos HTTP mais comuns

| Método | Uso comum | Exemplo |
|---|---|---|
| GET | Buscar dados | `GET /produtos` |
| POST | Criar novo recurso | `POST /produtos` |
| PUT | Atualizar recurso inteiro | `PUT /produtos/10` |
| PATCH | Atualizar parte do recurso | `PATCH /produtos/10` |
| DELETE | Remover recurso | `DELETE /produtos/10` |

### 5.4 Códigos de status úteis

| Código | Significado | Uso prático |
|---|---|---|
| 200 | OK | Requisição processada com sucesso |
| 201 | Created | Recurso criado com sucesso |
| 400 | Bad Request | Dados inválidos enviados pelo cliente |
| 401 | Unauthorized | Falta autenticação |
| 403 | Forbidden | Usuário autenticado, mas sem permissão |
| 404 | Not Found | Recurso não encontrado |
| 500 | Internal Server Error | Erro interno no servidor |

### 5.5 Boas práticas de design

- Usar nomes de recursos claros e no plural.
- Evitar verbos desnecessários nas URLs.
- Usar corretamente os métodos HTTP.
- Padronizar respostas de erro.
- Documentar endpoints, parâmetros e exemplos.
- Aplicar versionamento quando houver mudanças incompatíveis.
- Usar paginação em listas grandes.
- Evitar retornar dados desnecessários.

Exemplo melhor:

```text
GET /clientes/10/pedidos
```

Exemplo pior:

```text
GET /buscarPedidosDoCliente?id=10
```

### 5.6 Boas práticas de segurança

- Validar entradas recebidas pela API.
- Aplicar autenticação adequada.
- Verificar autorização em cada recurso.
- Evitar exposição excessiva de dados.
- Usar HTTPS.
- Não retornar detalhes sensíveis em mensagens de erro.
- Registrar logs úteis para investigação.
- Proteger endpoints administrativos.
- Aplicar rate limiting quando necessário.
- Revisar dependências e componentes utilizados.

### 5.7 Riscos comuns em APIs

Com base no projeto OWASP API Security, alguns riscos importantes são:

- Controle de acesso quebrado.
- Autenticação mal implementada.
- Exposição excessiva de dados.
- Falta de validação de entrada.
- Configuração incorreta.
- Consumo inseguro de APIs externas.
- Falta de logs e monitoramento.

### 5.8 Checklist rápido antes de publicar uma API

- Os endpoints estão documentados?
- Os métodos HTTP fazem sentido?
- A API valida os dados recebidos?
- Existe autenticação?
- Existe autorização por recurso?
- Os erros são padronizados?
- Dados sensíveis são protegidos?
- Listagens grandes usam paginação?
- A API usa HTTPS?
- Existem logs úteis?
- O banco de dados está protegido contra consultas inseguras?
- Existe controle de versão?
- Há testes básicos para fluxos principais?

## 6. Glossário

| Termo | Definição curta | Exemplo |
|---|---|---|
| API | Interface para sistemas conversarem | Sistema A consulta dados do Sistema B |
| REST | Estilo arquitetural baseado em recursos | `/clientes`, `/pedidos` |
| Endpoint | URL de acesso a uma operação | `/clientes/10` |
| Recurso | Entidade manipulada pela API | Cliente, pedido, produto |
| JSON | Formato comum de troca de dados | `{ "nome": "Ana" }` |
| Payload | Corpo da requisição ou resposta | Dados enviados em um POST |
| HTTP | Protocolo usado na comunicação web | GET, POST, PUT, DELETE |
| Status code | Código de resultado da requisição | 200, 201, 404 |
| Autenticação | Verifica identidade | Login, token JWT |
| Autorização | Verifica permissão | Usuário pode acessar apenas seus dados |
| Rate limit | Limite de requisições | 100 requisições por minuto |
| Paginação | Divisão de listas grandes | `?page=1&limit=20` |
| Webhook | Chamada automática entre sistemas | Sistema envia evento para outro |
| SQL | Linguagem para banco relacional | `SELECT * FROM clientes` |

## 7. Prompts Reutilizáveis

### Prompt para revisar conceitos

```text
Explique [conceito] em APIs REST com definição simples, exemplo prático e erro comum relacionado.
```

### Prompt para gerar checklist

```text
Crie um checklist para revisar uma API REST sobre [tema], incluindo design, segurança, dados, erros e documentação.
```

### Prompt para comparar fontes

```text
Compare o que as fontes dizem sobre [tema]. Aponte convergências, diferenças e recomendações práticas.
```

### Prompt para estudar segurança

```text
Liste os principais riscos de segurança relacionados a [tipo de endpoint] e sugira formas de mitigação.
```

### Prompt para simular entrevista técnica

```text
Faça 10 perguntas de entrevista sobre APIs REST seguras para nível júnior, com respostas comentadas.
```

### Prompt para transformar estudo em projeto

```text
Com base neste tema, sugira um projeto de portfólio simples, com funcionalidades, endpoints, banco de dados e requisitos de segurança.
```

## 8. Ideia de Projeto Futuro

Uma aplicação prática para consolidar esse estudo seria:

> **API de controle de candidaturas e vagas remotas**

Funcionalidades:

- Cadastro de vagas.
- Status de candidatura.
- Score de compatibilidade.
- Autenticação de usuário.
- CRUD de empresas e vagas.
- Relatórios simples.
- Integração futura com fontes externas.

Esse projeto permitiria aplicar APIs REST, banco de dados, autenticação, documentação, segurança e automação em um problema real.

## 9. Conclusão

O uso do NotebookLM neste desafio ajuda a transformar a IA em uma ferramenta de aprendizagem ativa. Em vez de apenas pedir respostas prontas, o processo exige selecionar boas fontes, formular perguntas melhores, comparar respostas, identificar falhas e consolidar o conhecimento.

O tema de APIs REST seguras é relevante porque conecta desenvolvimento backend, integração entre sistemas, automação, dados e segurança da informação. Esses conhecimentos são importantes para construir soluções mais confiáveis, organizadas e úteis em ambientes profissionais.

## 10. Descrição curta para entrega na DIO

Projeto de caderno temático criado com apoio do NotebookLM sobre APIs REST seguras para integração de sistemas. O repositório apresenta contexto, objetivos de estudo, curadoria de fontes abertas, prompts testados, dificuldades encontradas, miniguia consolidado, glossário e prompts reutilizáveis para revisão futura.

