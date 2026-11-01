# O Essencial da Bíblia · páginas de venda e captura

Páginas do livro **O Essencial da Bíblia: o 80/20 do Antigo e do Novo Testamento**, organizado por Michael Castilho.

| Página | Endereço (GitHub Pages) | Para quê |
| --- | --- | --- |
| `index.html` | `/o-essencial-da-biblia/` | Página de vendas com a promoção de lançamento |
| `mapa/index.html` | `/o-essencial-da-biblia/mapa/` | Isca gratuita: o mapa "A Bíblia em uma página" |

Funil sugerido: link na bio do Instagram e na descrição dos vídeos do YouTube → **/mapa/** (cadastro e download grátis) → convite para a página de vendas.

## Configuração

Tudo o que precisa ser ajustado fica no bloco `CONFIGURAÇÃO`, no fim de cada página.

**Página de vendas (`index.html`)**

```js
const PROMO_END = '2026-11-04T23:59:59-03:00';   // fim da promoção (horário de Brasília)
const PRICE = { promo: 47, regular: 97 };
const STACK_TOTAL = 198;                          // soma da pilha de valor
const CHECKOUT = { promo: '', regular: '' };      // links do checkout com cada preço
```

Quando o contador zera, a página troca sozinha para o preço normal e para o link `CHECKOUT.regular`. Para um novo lançamento, basta mudar `PROMO_END`.

**Isca (`mapa/index.html`)**

```js
const FORM_ENDPOINT = '';                          // endereço que recebe os cadastros
const FIELD = { nome: 'nome', email: 'email' };    // nomes dos campos esperados pelo serviço
const PROMO_END = '2026-11-04T23:59:59-03:00';     // o mesmo prazo da página de vendas
```

Enquanto `FORM_ENDPOINT` estiver vazio, o mapa é liberado sem guardar o cadastro.

## Publicar no GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → Branch: `main` / `(root)`.

> O livro e os bônus pagos em PDF **não** ficam neste repositório. O único PDF público é o mapa gratuito em `mapa/`.
