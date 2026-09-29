# Galleta Cookies Artesanais — site

Site-cardápio da Galleta (Divinópolis–MG), com pedido enviado pelo WhatsApp.
É um site estático: não precisa de build, instalação ou banco de dados.

## Estrutura

```
index.html          página do site
favicon.svg         ícone da aba
assets/img/         fotos
assets/fonts/       fontes
vercel.json         configuração da Vercel
```

## Publicar (GitHub + Vercel)

1. Crie um repositório no GitHub e envie **todo o conteúdo desta pasta** (o `index.html` precisa ficar na raiz do repositório).
2. Na Vercel, clique em **Add New → Project** e importe o repositório.
3. Em **Framework Preset**, escolha **Other**. Deixe *Build Command* e *Output Directory* em branco.
4. Clique em **Deploy**.

A cada novo envio (push) para o GitHub, a Vercel publica a atualização sozinha.

## Onde editar

No final do `index.html`, dentro do `<script>`:

- `LOJA.whatsapp` — número do WhatsApp com DDI e DDD, só dígitos (ex.: `"5537999998888"`). Com o número preenchido, o pedido chega já escrito na conversa.
- `LOJA.horario` — horários de funcionamento.
- `PRODUTOS` — nomes, descrições e preços (`preco`).

Depois de mudar produtos ou preços em `PRODUTOS`, a lista também existe pronta no HTML (para aparecer em visualizadores sem JavaScript).
No navegador, o script redesenha o cardápio com os dados de `PRODUTOS`, então o que vale é o que está no script.
