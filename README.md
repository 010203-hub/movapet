# Mova — Landing Page

Site institucional da Mova (escada premium para pets), em HTML/CSS/JS puro, sem dependência de build.

## Arquivos deste projeto

Coloque **todos** os arquivos abaixo na **raiz** do repositório (na mesma pasta):

```
index.html          → a página principal
bege.webp           → foto da escada na cor bege
grafite.webp        → foto da escada na cor grafite
marrom.webp         → foto da escada na cor marrom
azul-marinho.webp   → foto da escada na cor azul-marinho
preto.webp          → foto da escada na cor preto
cinza.webp          → foto da escada na cor cinza
.nojekyll           → arquivo vazio (evita o processamento Jekyll do GitHub)
README.md           → este arquivo
```

> Importante: o `index.html` procura as imagens pelo nome, na mesma pasta (ex.: `grafite.webp`).
> Mantenha os nomes exatamente como estão e todos juntos na raiz.

## Como publicar no GitHub Pages (passo a passo)

1. Crie uma conta no GitHub (se ainda não tiver) e faça login.
2. Clique em **New repository** (novo repositório).
   - Dê um nome, por exemplo `mova`.
   - Marque **Public**.
   - Pode marcar "Add a README" — mas depois substitua pelo desta pasta.
   - Clique em **Create repository**.
3. Envie os arquivos:
   - Na página do repositório, clique em **Add file → Upload files**.
   - Arraste **todos** os arquivos desta pasta (index.html + as 6 imagens .webp + .nojekyll + README.md) de uma vez.
   - Clique em **Commit changes**.
4. Ative o GitHub Pages:
   - Vá em **Settings** (⚙️) → menu lateral **Pages**.
   - Em **Source**, escolha **Deploy from a branch**.
   - Em **Branch**, selecione **main** e a pasta **/ (root)**. Clique em **Save**.
5. Aguarde ~1 minuto. O endereço do site aparecerá no topo da página **Pages**, no formato:
   `https://SEU-USUARIO.github.io/mova/`

Pronto — o site estará no ar.

## Depois de publicar

- Para atualizar algo, é só editar o arquivo no GitHub (ou reenviar) e dar **Commit**. O site atualiza sozinho em ~1 minuto.
- Se as imagens não aparecerem, confirme que os 6 arquivos `.webp` estão na **mesma pasta** do `index.html` e com os nomes exatos.

## Configurar os links de cada cor (loja)

No final do `index.html`, existe um bloco com os links de cada cor. Basta trocar cada `"#"` pela URL da cor correspondente:

```js
var LINKS = {
  "bege":         "#",   // ex.: "https://sualoja.com/escada-bege"
  "grafite":      "#",
  "marrom":       "#",
  "azul-marinho": "#",
  "preto":        "#",
  "cinza":        "#"
};
```

Quando um link for preenchido, o botão **"Conhecer o produto"** passa a levar para a página daquela cor (abrindo em nova aba).

## Domínio próprio (opcional)

Se quiser usar um domínio próprio (ex.: `mova.com.br`), em **Settings → Pages → Custom domain** informe o domínio e configure o DNS conforme as instruções do GitHub. O GitHub cria um arquivo `CNAME` automaticamente.

## Observações técnicas

- Fontes (Inter) e a biblioteca de rolagem suave (Lenis) são carregadas por CDN — funcionam normalmente no GitHub Pages, sem instalação.
- O site é totalmente estático: não há backend, banco de dados nem etapa de build.
- Responsivo (desktop, tablet e celular), com menu mobile e animações que respeitam a preferência de "movimento reduzido".
