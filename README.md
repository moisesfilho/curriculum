# Portfólio Profissional - Moisés Alves Carneiro Filho

Site profissional estático para apresentar minha atuação em liderança técnica e arquitetura de software. A página inicial destaca posicionamento, impacto, projetos e experiência; o currículo detalhado permanece disponível em `curriculo.html`, com opção de exportação para PDF.

🔗 **URL Pública:** [https://www.moisesfilho.dev.br](https://www.moisesfilho.dev.br)

## 🛠 Como foi desenvolvido

O projeto é focado no essencialismo e não utiliza frameworks pesados, garantindo um carregamento ultrarrápido:

- **HTML5 Semântico:** Estrutura acessível e responsiva, sem dependência de framework.
- **CSS3:** Folhas de estilo independentes para a landing page e o currículo, com tema claro/escuro.
- **Vanilla JavaScript:** Alternância de idioma e tema, com preferências persistidas no navegador.

## ✨ Funcionalidades

- 🌍 **Português e inglês:** A landing page e o currículo permitem alternância de idioma, mantendo a escolha no `localStorage`.
- 🌓 **Tema claro e escuro:** Detecta a preferência do sistema e permite alternância manual.
- 📄 **Currículo em PDF:** `curriculo.html` oferece versões A4 em português e inglês para download, além de permitir imprimir a versão exibida no navegador.

## 📐 Padrões de Código e Formatação

Para garantir a consistência do código e facilitar a manutenção, o projeto utiliza ferramentas de formatação automatizada:

- **EditorConfig (`.editorconfig`):** Define padrões universais para editores de código (como indentação de 2 espaços, quebra de linha `LF`, codificação UTF-8 e linha em branco no final dos arquivos).
- **Prettier (`.prettierrc`):** O formatador padroniza automaticamente os arquivos (HTML, CSS, Markdown, YAML). Está configurado para manter limites de linha (120 caracteres), aspas simples e regras globais do ecosistema web.
  - Para aplicar as regras manualmente, utilize: `npx prettier --write .`

## 🚀 Processo de Deploy (CI/CD)

A publicação do currículo ocorre de maneira contínua e totalmente automatizada através da infraestrutura do GitHub:

1. O código-fonte principal fica armazenado na branch `main`.
2. Um pipeline do **GitHub Actions** (configurado no arquivo `.github/workflows/static.yml`) é automaticamente disparado a cada `push`.
3. O workflow publica os arquivos estáticos (`index.html`, `curriculo.html`, CSS e demais recursos) no **GitHub Pages**.
4. O repositório está integrado com um domínio customizado (`moisesfilho.dev.br`), com roteamento DNS (`CNAME` e `A`/`AAAA` records) gerenciado de forma externa e certificado SSL (HTTPS) mantido ativamente pela plataforma.
