# O Essencial da Bíblia · páginas de venda e captura

Páginas do livro **O Essencial da Bíblia: o 80/20 do Antigo e do Novo Testamento**, organizado por Michael Castilho.

| Página | Endereço (GitHub Pages) | Para quê |
| --- | --- | --- |
| `index.html` | `/o-essencial-da-biblia/` | Página de vendas (preço único) |
| `mapa/index.html` | `/o-essencial-da-biblia/mapa/` | Isca gratuita: o mapa "A Bíblia em uma página" |

Funil sugerido: link na bio do Instagram e na descrição dos vídeos do YouTube → **/mapa/** (cadastro e download grátis) → convite para a página de vendas.

## Configuração

Tudo o que precisa ser ajustado fica no bloco `CONFIGURAÇÃO`, no fim de cada página.

**Página de vendas (`index.html`)**

```js
const CHECKOUT_URL = '';   // link do checkout (Hotmart, Kiwify etc.)
```

Preço único de R$ 47. Enquanto `CHECKOUT_URL` estiver vazio, os botões levam à seção da oferta.

**Isca (`mapa/index.html`)**

```js
const FORM_ENDPOINT = 'https://…sibforms.com/serve/…';  // endereço do formulário do Brevo (já configurado)
const FIELD = { nome: 'NOME', email: 'EMAIL' };    // nomes dos campos do formulário do Brevo
```

Enquanto `FORM_ENDPOINT` estiver vazio, o mapa é liberado sem guardar o cadastro.

## Publicar no GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → Branch: `main` / `(root)`.

> O livro e os bônus pagos em PDF **não** ficam neste repositório. O único PDF público é o mapa gratuito em `mapa/`.
