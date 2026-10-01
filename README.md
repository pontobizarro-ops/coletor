# Páginas públicas do coletor

As quatro páginas que o cadastro do app no TikTok exige, geradas a partir dos
fragmentos versionados em `canal/paginas/`.

| arquivo | serve para |
|---|---|
| `index.html` | Web/Desktop URL — site oficial da ferramenta |
| `termos.html` | Terms of Service URL |
| `privacidade.html` | Privacy Policy URL |
| `autorizado.html` | Redirect URI do Login Kit |

`autorizado.html` lê `code` e `state` da barra de endereço e mostra os dois para
copiar. Ela não envia nada a lugar nenhum: a troca pelos tokens acontece na
máquina de quem publica, que é onde está o `client_secret`.

Para regerar as três primeiras depois de editar `canal/paginas/`, use o script
em `scripts/montar-site.mjs`.
