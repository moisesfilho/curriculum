# Currículo Digital - Moisés Alves Carneiro Filho

Página web estática que hospeda meu currículo profissional. O projeto foi desenvolvido com foco em alta performance, acessibilidade e escaneabilidade — tanto para leitura humana rápida quanto para robôs e ferramentas automatizadas de recrutamento (ATS).

🔗 **URL Pública:** [https://www.moisesfilho.dev.br](https://www.moisesfilho.dev.br)

## 🛠 Como foi desenvolvido

O projeto é focado no essencialismo e não utiliza frameworks pesados, garantindo um carregamento ultrarrápido:

- **HTML5 Semântico:** Estrutura sólida (`<header>`, `<main>`, `<article>`) para facilitar a interpretação do conteúdo por sistemas de leitura e indexadores.
- **CSS3:** Estilização moderna e responsiva utilizando Variáveis (Custom Properties) para gerenciar o Design System e a alternância de temas.
- **Vanilla JavaScript:** Scripts puros e leves injetados diretamente no documento para gerenciar o estado da aplicação instantaneamente (prevenindo _FOUC - Flash of Unstyled Content_).

## ✨ Funcionalidades

- 🌍 **Internacionalização (PT/EN):** O currículo possui texto fluido em Português e Inglês. A alternância entre os idiomas é feita de forma instantânea na interface, sem necessidade de recarregar a página. A escolha do usuário é persistida no `localStorage` do navegador.
- 🌓 **Dark Mode (Modo Escuro):** O layout alterna dinamicamente entre o tema claro e escuro. O sistema detecta automaticamente a preferência nativa do sistema operacional (`prefers-color-scheme`) como padrão e permite a troca manual via botão na interface, também salvando o estado no `localStorage`.
- 📄 **Baixar PDF (Otimizado para ATS):** Um recurso integrado de exportação utilizando a funcionalidade de impressão do navegador (`window.print()`). Por meio da diretiva `@media print` no CSS, a interface esconde ativamente elementos não imprimíveis (como botões e seletores) e gera um PDF estruturado e limpo contendo apenas o idioma ativo. Esse formato é extremamente favorável para análise automatizada por plataformas ATS (_Applicant Tracking Systems_).

## 📐 Padrões de Código e Formatação

Para garantir a consistência do código e facilitar a manutenção, o projeto utiliza ferramentas de formatação automatizada:

- **EditorConfig (`.editorconfig`):** Define padrões universais para editores de código (como indentação de 2 espaços, quebra de linha `LF`, codificação UTF-8 e linha em branco no final dos arquivos).
- **Prettier (`.prettierrc`):** O formatador padroniza automaticamente os arquivos (HTML, CSS, Markdown, YAML). Está configurado para manter limites de linha (120 caracteres), aspas simples e regras globais do ecosistema web.
  - Para aplicar as regras manualmente, utilize: `npx prettier --write .`

## 🚀 Processo de Deploy (CI/CD)

A publicação do currículo ocorre de maneira contínua e totalmente automatizada através da infraestrutura do GitHub:

1. O código-fonte principal fica armazenado na branch `main`.
2. Um pipeline do **GitHub Actions** (configurado no arquivo `.github/workflows/static.yml`) é automaticamente disparado a cada `push`.
3. O workflow faz o empacotamento e sobe os arquivos estáticos para o serviço **GitHub Pages**.
4. O repositório está integrado com um domínio customizado (`moisesfilho.dev.br`), com roteamento DNS (`CNAME` e `A`/`AAAA` records) gerenciado de forma externa e certificado SSL (HTTPS) mantido ativamente pela plataforma.
