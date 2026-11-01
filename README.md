# O Essencial da Bíblia · página de vendas

Página de vendas do livro **O Essencial da Bíblia: o 80/20 do Antigo e do Novo Testamento**, organizado por Michael Castilho.

## Estrutura

- `index.html`: a página inteira (HTML e CSS em um só arquivo).
- `assets/img/`: amostras de páginas do livro e dos bônus.

## Link de compra

No fim do `index.html` há a linha:

```js
const CHECKOUT_URL = '';
```

Cole entre as aspas o link do checkout (Hotmart, Kiwify etc.). Todos os botões de compra passam a apontar para ele.

## Publicar no GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → Branch: `main` / `(root)`.

> O livro e os bônus em PDF **não** ficam neste repositório. Eles são o produto pago e devem ser entregues pela plataforma de venda.
