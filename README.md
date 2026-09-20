# Página de apresentação

Site estático (HTML + CSS, sem build) que apresenta as 4 extensões, com botões para Firefox e Edge.

## Preencher os links das lojas

Edite **só** `links.js` quando cada extensão for aprovada. Link vazio = o botão mostra "Em breve".

## Publicar (GitHub Pages)

Não use o repositório `politica-extensoes`: o endereço dele já é o link da política de privacidade nas lojas e não deve mudar.
Crie um repositório separado, por exemplo `extensoes`, e publique esta pasta:

```
cd site-apresentacao
git init -b main && git add . && git commit -m "Página de apresentação"
gh repo create extensoes --public --source . --push
gh api -X POST repos/nshowdebola-ctrl/extensoes/pages -f "source[branch]=main" -f "source[path]=/"
```

Endereço final: https://nshowdebola-ctrl.github.io/extensoes/ (leva cerca de 1 minuto para aparecer).

Depois, ponha esse endereço no campo "site da página inicial/suporte" de cada loja.
