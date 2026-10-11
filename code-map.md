# curriculum Code Map

Site pessoal de curriculo estatico, publicado como frontend sem backend.

## Arquivos

| Caminho | Responsabilidade |
| --- | --- |
| `index.html` | Documento, estrutura da pagina e conteudo do curriculo em portugues e ingles. |
| `index.css` | Tema, layout responsivo e apresentacao visual. |
| `CNAME` | Dominio usado na publicacao. |
| `robots.txt` | Politica de indexacao do site. |
| `.github/` | Automacao de publicacao/qualidade. |
| `README.md` | Documentacao do projeto. |

## Stack e validacao

HTML, CSS e JavaScript nativos, sem manifest de dependencias. A entrada e
`index.html`; a validacao principal e abrir a pagina em navegador desktop e
mobile e verificar o workflow do GitHub Actions. O repositorio nao possui
testes automatizados nem etapa local de build.
