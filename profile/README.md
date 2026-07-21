<div align="center">

<img src="./assets/logo.png" width="112" height="112" alt="LogHub Open" />

# LogHub Open

**Plataforma open source para coleta, centralização e análise de logs**

[![GitHub Org](https://img.shields.io/badge/GitHub-LogHub--Open-6366F1?logo=github&logoColor=white)](https://github.com/LogHub-Open)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-7C3AED)](https://github.com/LogHub-Open/.github/blob/main/CONTRIBUTING.md)

</div>

---

## O que é a LogHub Open?

A **LogHub Open** é uma organização focada em ferramentas open source para **observabilidade e gerenciamento de logs**. Nosso objetivo é fornecer soluções acessíveis, escaláveis e fáceis de integrar para times de desenvolvimento e operações.

## 🌐 Projetos

| Repositório | Descrição | Stack |
|-------------|-----------|-------|
| [**loghub-sdk**](https://github.com/LogHub-Open/loghub-sdk)<br>![issues](https://img.shields.io/github/issues/LogHub-Open/loghub-sdk?color=6366F1&label=issues)&nbsp;![prs](https://img.shields.io/github/issues-pr/LogHub-Open/loghub-sdk?color=7C3AED&label=PRs)&nbsp;![prs fechados](https://img.shields.io/github/issues-pr-closed/LogHub-Open/loghub-sdk?color=A855F7&label=PRs%20fechados)&nbsp;![last commit](https://img.shields.io/github/last-commit/LogHub-Open/loghub-sdk?color=8B5CF6&label=commit) | SDK Java para logging estruturado, com envio assíncrono para a LogHub API | Java 17, Maven, Logback |
| [**loghub-api**](https://github.com/LogHub-Open/loghub-api)<br>![issues](https://img.shields.io/github/issues/LogHub-Open/loghub-api?color=6366F1&label=issues)&nbsp;![prs](https://img.shields.io/github/issues-pr/LogHub-Open/loghub-api?color=7C3AED&label=PRs)&nbsp;![prs fechados](https://img.shields.io/github/issues-pr-closed/LogHub-Open/loghub-api?color=A855F7&label=PRs%20fechados)&nbsp;![last commit](https://img.shields.io/github/last-commit/LogHub-Open/loghub-api?color=8B5CF6&label=commit) | Backend RESTful para ingestão, armazenamento e consulta de logs | Java 17, Spring Boot, PostgreSQL |
| [**loghub-ui**](https://github.com/LogHub-Open/loghub-ui)<br>![issues](https://img.shields.io/github/issues/LogHub-Open/loghub-ui?color=6366F1&label=issues)&nbsp;![prs](https://img.shields.io/github/issues-pr/LogHub-Open/loghub-ui?color=7C3AED&label=PRs)&nbsp;![prs fechados](https://img.shields.io/github/issues-pr-closed/LogHub-Open/loghub-ui?color=A855F7&label=PRs%20fechados)&nbsp;![last commit](https://img.shields.io/github/last-commit/LogHub-Open/loghub-ui?color=8B5CF6&label=commit) | Interface web para visualização, filtro e diagnóstico de logs | React 19, TypeScript, Vite, Tailwind |

<sub>Os badges de issues, PRs e último commit são dinâmicos (via shields.io) — atualizam sozinhos conforme os repositórios mudam.</sub>

### Arquitetura

```mermaid
flowchart LR
    subgraph Apps["🖥️ Suas Aplicações"]
        A1[App 1 + SDK]
        A2[App 2 + SDK]
        A3[App N + SDK]
    end
    subgraph Backend["⚙️ LogHub API"]
        API[REST API]
        DB[(Database)]
        API --> DB
    end
    subgraph Frontend["🌐 LogHub UI"]
        UI[Interface Web]
    end
    A1 -->|logs| API
    A2 -->|logs| API
    A3 -->|logs| API
    UI -->|consulta| API

    classDef sdk fill:#6366F1,color:#fff,stroke:none
    classDef api fill:#8B5CF6,color:#fff,stroke:none
    classDef ui fill:#7C3AED,color:#fff,stroke:none
    class A1,A2,A3 sdk
    class API,DB api
    class UI ui
```

Suas aplicações usam o **loghub-sdk** para enviar logs estruturados via HTTP para a **loghub-api**, que os armazena e indexa. Você visualiza e analisa os dados através da **loghub-ui**.

## 🤝 Contribuindo

Adoramos contribuições! Seja reportando bugs, sugerindo funcionalidades ou enviando PRs.

1. Leia nosso [Guia de Contribuição](https://github.com/LogHub-Open/.github/blob/main/CONTRIBUTING.md)
2. Confira nosso [Código de Conduta](https://github.com/LogHub-Open/.github/blob/main/CODE_OF_CONDUCT.md)
3. Abra uma issue ou PR no repositório desejado

## 💬 Comunidade

- Encontrou um bug? Abra uma **issue** no repositório correspondente.
- Tem uma ideia? Use as **Discussions** do projeto.
- Questões de segurança? Veja nossa [Política de Segurança](https://github.com/LogHub-Open/.github/blob/main/SECURITY.md).

---

<div align="center">
  <sub>Feito com ❤️ pela comunidade LogHub Open</sub>
</div>
