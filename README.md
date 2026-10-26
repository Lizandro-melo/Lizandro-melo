<div align="center">

# Lizandro Melo

**Desenvolvedor Back-end · Python/Django · Next.js · Automação**

Fundador da Controll — software de gestão para pequenos negócios brasileiros

<br/>

<a href="https://www.linkedin.com/in/lizandromelo/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:lizandro.melllo@gmail.com"><img src="https://img.shields.io/badge/E--mail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="E-mail" /></a>
<a href="https://agenda.controll.dev.br"><img src="https://img.shields.io/badge/Controll_Agenda-0F172A?style=for-the-badge" alt="Controll Agenda" /></a>
<a href="https://fit.controll.dev.br"><img src="https://img.shields.io/badge/Controll_Fit-0F172A?style=for-the-badge" alt="Controll Fit" /></a>

</div>

<br/>

## Sobre

Atuo no suporte N1 a N3 da Icatu Seguros, pela FixConsulting, onde automatizei rotinas com RPA, chatbot e Power Automate. Minha base inclui também administração de infraestrutura (Active Directory, Windows Server, KACE), e em paralelo desenvolvo produto próprio.

Construo sistemas SaaS multi-tenant em **Python/Django** e **Next.js**, com Celery, Redis e PostgreSQL, empacotados em Docker e validados por CI. Fundei a **Controll**, que mantém dois produtos: agendamento online para prestadores de serviço e gestão para academias.

- **Formação:** Análise e Desenvolvimento de Sistemas, UNISUAM
- **Certificações:** trilhas de Java, JavaScript, front-end e back-end pela Alura
- **Localização:** Rio de Janeiro, RJ
- **Busco:** posições de Desenvolvedor Back-end ou Full-stack, e projetos de automação e integração

<br/>

## Produtos

### Controll Agenda

Agendamento online para quem atende com hora marcada: barbearias, salões, clínicas e profissionais autônomos, inclusive com atendimento em domicílio. O cliente marca sozinho em uma página do negócio e o prestador deixa de organizar a agenda pelo WhatsApp.

**[agenda.controll.dev.br](https://agenda.controll.dev.br)**

- Agenda baseada na duração real do serviço, somada aos adicionais, com grade e folgas por profissional.
- Regra central: o sistema não aceita dois agendamentos no mesmo horário do mesmo profissional.
- Confirmações e lembretes automáticos por e-mail ou WhatsApp.
- Cobrança de multa por falta e pagamento no local ou pelo site, via Asaas.
- Atendimento em domicílio, com taxa de deslocamento por bairro.
- Página própria com a marca do negócio e área do cliente sem senha, com confirmação do telefone por código.

`Django` `Django REST Framework` `Celery` `Redis` `Next.js` `React` `Tailwind` `Asaas` `Docker`

<br/>

### Controll Fit

CRM, vendas e operação diária para academias independentes. Foi desenhado para academias de uma unidade, com 100 a 800 alunos.

**Status:** em desenvolvimento · **[fit.controll.dev.br](https://fit.controll.dev.br)**
- CRM com funil kanban, leads, campanhas e automações de follow-up, boas-vindas e reativação.
- Ponto de venda, planos, serviços agendáveis com crédito de uso e cobranças via Asaas (PIX, boleto e cartão).
- Agenda de turmas e de serviços, com controle de vagas por sessão e presença.
- Integração com WhatsApp (Evolution API) e e-mail, com SMTP por tenant e senha cifrada em repouso.
- Multi-tenant com permissões por papel (RBAC), JWT com rotação e blacklist, e throttling por escopo.
- Mais de 1.700 testes automatizados entre backend e frontend.

`Django` `Django REST Framework` `Celery` `PostgreSQL` `Redis` `Next.js` `React` `TypeScript` `Evolution API` `Asaas` `Docker` `Nginx`

<br/>

## Decisões de engenharia

Pontos em que os dois produtos exigiram escolhas técnicas deliberadas:

| Problema | Abordagem |
|---|---|
| Dois clientes tentando o mesmo horário | Bloqueio transacional (`select_for_update`) na criação do agendamento, com regras validadas em ordem |
| Reenvio de requisição duplicando cobrança ou crédito | Idempotência verificada antes do débito |
| Vaga e crédito do aluno são coisas diferentes | Eixos separados: cancelar fora do prazo libera o horário, mas consome o crédito |
| Dados de academias diferentes no mesmo banco | Multi-tenant com isolamento por chave estrangeira, permissões fail-closed e testes de isolamento |
| Decisões que se perdem com o tempo | Registro de decisões (ADR), roadmap e log de tarefas versionados junto com o código |

<br/>

## Stack

| | |
|---|---|
| **Back-end** | Python, Django, Django REST Framework, Celery, Java, Spring Boot |
| **Front-end** | TypeScript, JavaScript, React, Next.js, Tailwind CSS |
| **Dados** | PostgreSQL, MySQL, Redis, Pandas |
| **Infraestrutura** | Docker, Nginx, GitHub Actions, Linux, Active Directory, Windows Server |
| **Automação** | Power Automate, Selenium, RPA, chatbots, integrações via API |

<br/>

## Contato

Aberto a conversas sobre oportunidades, projetos de automação e integração de sistemas.

[LinkedIn](https://www.linkedin.com/in/lizandromelo/) · [lizandro.melllo@gmail.com](mailto:lizandro.melllo@gmail.com)
