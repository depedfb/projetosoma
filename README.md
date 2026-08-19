# 🎓 Guia Prático de Auxílio Estudantil — UTFPR
### Projeto SOMA 2026 • Universidade Tecnológica Federal do Paraná

[![UTFPR](https://img.shields.io/badge/UTFPR-Campus%20Francisco%20Beltr%C3%A3o-002F6C?style=flat-square&logo=academia)](https://www.utfpr.edu.br/)
[![Edital](https://img.shields.io/badge/Edital-01%2F2026%20PROGRAD%2FASSAE-F3C400?style=flat-square)](https://sei.utfpr.edu.br/sei/publicacoes/controlador_publicacoes.php?acao=publicacao_visualizar&id_documento=6394999&id_orgao_publicacao=0)
[![Privacy](https://img.shields.io/badge/Privacidade-100%25%20Client--Side-10B981?style=flat-square)](#-privacidade-e-segurança-lgpd)
[![License](https://img.shields.io/badge/Licen%C3%A7a-Open%20Source-blue?style=flat-square)](LICENSE)

Aplicação web estática, interativa e acessível criada para orientar e simplificar a inscrição dos estudantes no **Programa de Auxílio Estudantil da UTFPR (Edital Nº 01/2026 PROGRAD/ASSAE)**.

---

## 📌 Principais Funcionalidades

- 🧭 **Simulador Interativo de Elegibilidade (Wizard):** Assistente passo a passo que calcula a renda per capita familiar, analisa critérios do edital e gera uma lista personalizada de documentos e declarações necessárias.
- 📖 **Navegação Linear e Estruturada:** 28 tópicos organizados cobrindo desde a preparação inicial até o envio e acompanhamento do resultado no Portal do Aluno.
- 🏢 **Seletor de Contatos dos 13 Câmpus:** Consulta rápida a e-mails, telefones, horários de atendimento e responsáveis da ASSAE/NUAPE em cada cidade da UTFPR.
- 📥 **Central de Downloads Integrada:** Acesso direto a todos os modelos de declaração oficiais (`.docx`) e tutoriais passo a passo (`.pdf`).
- 🌓 **Acessibilidade e Temas:** Suporte a Tema Claro e Tema Escuro (*Dark Mode*), com detecção automática e persistência anti-flicker.
- 🔍 **Busca em Tempo Real:** Pesquisa instantânea em todos os tópicos e termos do edital com realce visual dos resultados.
- 🔒 **Conformidade LGPD:** Armazenamento 100% local no navegador (`localStorage`), sem coleta nem envio de dados a servidores terceiros, incluindo botão para limpeza imediata em computadores públicos.

---

## 📁 Estrutura do Projeto

```text
soma-pagina-auxilio/
├── css/
│   └── style.css            # Design System institucional UTFPR, layout responsivo e temas
├── documentos/              # Declarações oficiais (.docx) e manuais/tutoriais em PDF
│   ├── declaracao-01-renda.docx
│   ├── declaracao-02-situacao-moradia.docx
│   ├── declaracao-03-atividade-rural.docx
│   ├── declaracao-04-independencia-financeira.docx
│   ├── declaracao-05-diversas-situacoes.docx
│   ├── declaracao-06-pagamento-aluguel.docx
│   ├── declaracao-07-nao-obrigatoriedade-irpf.docx
│   ├── declaracao-08-renda-terceiros.docx
│   ├── termo-desligamento-voluntario.docx
│   ├── edital-auxilio-estudantil.pdf
│   ├── tutorial-comprovante-irpf.pdf
│   ├── tutorial-extrato-cnis.pdf
│   ├── tutorial-inscricao-portal.pdf
│   └── tutorial-reaproveitamento-documentos.pdf
├── js/
│   ├── app.js               # Lógica da aplicação, SPA, rotas hash, wizard e persistência
│   └── data.js              # Árvore de dados estruturada do guia e itens de download
├── index.html               # Estrutura HTML principal (Single Page Application)
├── .gitignore               # Regras de exclusão Git (arquivos locais e temporários)
└── README.md                # Documentação do projeto
```

---

## 🛠️ Tecnologias Utilizadas

- **HTML5 Semântico:** Estrutura acessível com suporte a leitores de tela e metadados.
- **CSS3 Moderno:** Variáveis (*CSS Custom Properties*), Flexbox, CSS Grid e animações fluidas.
- **JavaScript Vanilla (ES6+):** Roteamento cliente via hash (`#page-X`), renderização dinâmica e sem dependências externas.
- **Web Storage API (`localStorage`):** Persistência de progresso, respostas do simulador e preferências de tema.

---

## 🔒 Privacidade e Segurança (LGPD)

Todo o funcionamento do guia é executado estritamente **no lado do cliente (Client-Side)**:
- Nenhuma informação preenchida no simulador de renda é transmitida para a rede.
- As preferências e respostas ficam salvas exclusivamente no `localStorage` do dispositivo utilizado.
- Para estudantes utilizando computadores públicos (como laboratórios e bibliotecas), o menu lateral dispõe do botão **"Limpar Meus Dados / Reset"**, que apaga todos os registros locais instantaneamente.

---

## 👥 Créditos & Realização

**Projeto SOMA 2026** — Universidade Tecnológica Federal do Paraná (Câmpus Francisco Beltrão)

- **Desenvolvimento & Elaboração:** 
  - Andrey Luisi Dantas Matias
  - Samuel Thiago Telles Rodrigues
- **Orientação:** 
  - Prof. Kleber Durat

