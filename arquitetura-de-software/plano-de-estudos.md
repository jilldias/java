# Plano de Estudos: Arquitetura de Software

Este guia foi estruturado de forma progressiva, indo dos fundamentos de design de código até sistemas distribuídos em larga escala e governança.

---

## Fase 1: Fundamentos e Design de Código
O objetivo desta fase é dominar a construção de blocos de software limpos, testáveis e fáceis de manter.

* **Princípios de Design:**
  * SOLID, DRY (Don't Repeat Yourself), KISS (Keep It Simple, Stupid) e YAGNI (You Aren't Gonna Need It).
  * Lei de Demeter e Composição vs. Herança.
* **Design Patterns (GoF):**
  * **Criacionais:** Factory Method, Abstract Factory, Builder, Singleton.
  * **Estruturais:** Adapter, Decorator, Facade, Proxy.
  * **Comportamentais:** Strategy, Observer, Command, Chain of Responsibility.
* **Qualidade e Testes:**
  * Pirâmide de testes (Unitários, Integração, E2E).
  * TDD (Test-Driven Development) e cobertura de código.
* **Prática Recomendada:** Refatorar um sistema legado pequeno aplicando Design Patterns e criando uma suíte de testes automatizados.

---

## Fase 2: Estilos Arquiteturais e Modelagem 
Foco em como organizar a estrutura macro da aplicação e alinhar o código às regras de negócio.

* **Estilos Arquiteturais Clássicos:**
  * Arquitetura em Camadas (N-Tier) e Monolito Modular.
  * Arquitetura Hexagonal (Ports and Adapters).
  * Clean Architecture e Onion Architecture.
* **Domain-Driven Design (DDD):**
  * **Design Estratégico:** Linguagem Ubíqua, Subdomínios e Bounded Contexts (Contextos Delimitados).
  * **Design Tático:** Entidades, Value Objects, Agregados, Repositórios e Domain Events.
* **Documentação de Arquitetura:**
  * C4 Model (Context, Containers, Components, Code).
  * ADRs (Architecture Decision Records) para registrar o "porquê" das escolhas técnicas.
* **Prática Recomendada:** Modelar um domínio complexo (ex: sistema de reservas ou e-commerce) usando DDD, desenhar os diagramas no C4 Model e implementar a estrutura usando Clean Architecture.

---

## Fase 3: Sistemas Distribuídos e Comunicação
Como fazer diferentes serviços conversarem de forma eficiente, resiliente e escalável.

* **Estilos de Distribuição:**
  * Microsserviços vs. Monolitos (quando usar e *trade-offs*).
  * Arquitetura Orientada a Eventos (EDA - Event-Driven Architecture) e Serverless.
* **Comunicação entre Serviços:**
  * **Síncrona:** REST, GraphQL e gRPC.
  * **Assíncrona:** Mensageria e Streaming (RabbitMQ, Apache Kafka).
* **Padrões de Resiliência e Dados Distribuídos:**
  * Circuit Breaker, Retry, Timeout, Bulkhead e Rate Limiting.
  * Saga Pattern (Coreografia vs. Orquestração), Outbox Pattern e CQRS.
  * Teorema CAP, Consistência Eventual e Idempotência.
* **Prática Recomendada:** Criar dois microsserviços que se comunicam de forma assíncrona via fila/tópico, implementando o *Outbox Pattern* para garantir a entrega da mensagem.

---

## Fase 4: Dados, Infraestrutura e Observabilidade 
Aspectos não funcionais (Requisitos Arquiteturais / *-ilities*) que garantem que o sistema sobreviva em produção.

* **Estratégias de Banco de Dados:**
  * SQL vs. NoSQL (Documento, Chave-Valor, Colunar, Grafo).
  * Escalabilidade de dados: Sharding, Particionamento, Replicação e Read Replicas.
  * Estratégias de Cache (Redis, Memcached, CDN, Cache-Aside, Write-Through).
* **Segurança e Redes:**
  * API Gateways, Load Balancers e Reverse Proxies.
  * Autenticação e Autorização (OAuth 2.0, OpenID Connect, JWT).
* **Observabilidade:**
  * Os três pilares: Logs estruturados, Métricas (Prometheus/Grafana) e Tracing Distribuído (OpenTelemetry).
* **Cloud e Containers:**
  * Fundamentos de Docker, Kubernetes e Infraestrutura como Código (Terraform).

---

## Fase 5: Soft Skills, Trade-offs e Governança (Contínuo)
Ser arquiteto envolve tanto pessoas e negócios quanto tecnologia.

* **Análise de Trade-offs:** Tudo em arquitetura tem um custo. Aprenda a avaliar desempenho vs. custo, consistência vs. disponibilidade.
* **Fitness Functions:** Testes automatizados para garantir que as regras arquiteturais não sejam quebradas ao longo do tempo (ex: ArchUnit).
* **Comunicação:** Traduzir riscos técnicos para linguagem de negócios (stakeholders) e liderar tecnicamente sem microgerenciamento.

---

## Bibliografia Essencial
1. *Fundamentos da Arquitetura de Software* — Mark Richards & Neal Ford
2. *Arquitetura Limpa* — Robert C. Martin
3. *Domain-Driven Design* — Eric Evans (ou *Implementing DDD* — Vaughn Vernon)
4. *Designing Data-Intensive Applications* — Martin Kleppmann
