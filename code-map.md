# curriculum Code Map

Site pessoal de curriculo estatico, publicado como frontend sem backend.

## Arquivos

| Caminho | Responsabilidade |
| --- | --- |
| `index.html` | Landing page profissional bilíngue, com posicionamento, métricas atribuídas, projetos, casos técnicos e trajetória. |
| `home.css` | Tema, layout responsivo e apresentação visual da landing page e estudos de caso. |
| `curriculo.html` | Currículo detalhado bilíngue, com áreas de atuação resumidas, controles de tema, idioma e impressão/PDF. |
| `index.css` | Tema, layout responsivo e apresentação visual do currículo detalhado. |
| `CNAME` | Dominio usado na publicacao. |
| `robots.txt` | Politica de indexacao do site. |
| `.github/` | Automacao de publicacao/qualidade. |
| `README.md` | Documentacao do projeto. |

## Stack e validacao

HTML, CSS e JavaScript nativos, sem manifest de dependencias. A entrada e
`index.html`; a validacao principal e abrir a pagina em navegador desktop e
mobile e verificar o workflow do GitHub Actions. O repositorio nao possui
testes automatizados nem etapa local de build.
