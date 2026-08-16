# Roda Comigo — site

Site estático. Sem build, sem dependências: é só subir os arquivos.

## Estrutura

```
index.html          página principal
termos.html         Termos de Uso v1.0
privacidade.html    Política de Privacidade v1.0
style.css           estilos das três páginas
img/
  logo.png          logo em versão clara, para fundo escuro (topo e rodapé)
  favicon.png       ícone da aba — 512x512
  og.jpg            imagem de compartilhamento — 1200x630
  corrida-boa.jpeg  print da corrida de R$ 11,60 (R$ 4,46/km)
  corrida-ruim.jpeg print da corrida de R$ 12,30 (R$ 2,49/km)
```

Os HTML e o CSS ficam na **raiz** do repositório. As imagens ficam na pasta `img`,
com esse nome exato, em minúsculas. Nomes de arquivo diferenciam maiúscula de
minúscula no servidor.

## Já configurado

- Checkout: `https://clkdmg.site/pay/roda-comigo` (Digital Manager Guru)
- Vídeo do hero: Panda Video, ID `87b37712-49f5-4a73-b535-177e2493dc9f`
- Contato: `contato@rodacomigo.com`
- Instagram: `@rodacomigo.oscar`
- Preço: R$ 96 ou 12x de R$ 8,00 · acesso por 12 meses
- Banner de cookies com bloqueio de pixels até o aceite

Não há canal de WhatsApp.

## Pendências

1. **Meta Pixel / Google Tag** — colar dentro da função `loadPixels()`, no fim do
   `index.html`. Os pixels só disparam depois do aceite no banner de cookies, que é
   o que a Política de Privacidade promete no item 6.
2. **Domínio autorizado no Panda Video** — liberar `rodacomigo.com` e
   `www.rodacomigo.com` nos domínios permitidos. Sem isso o player do hero aparece
   bloqueado. Durante os testes, liberar também o endereço provisório do GitHub Pages.

## Publicação

Site estático puro. Funciona em GitHub Pages, Cloudflare Pages, Netlify ou Vercel
sem configuração adicional.

Para GitHub Pages com domínio próprio no GoDaddy: quatro registros A no nome `@`
apontando para 185.199.108.153, 185.199.109.153, 185.199.110.153 e 185.199.111.153,
mais um CNAME no nome `www` apontando para `usuario.github.io`.
