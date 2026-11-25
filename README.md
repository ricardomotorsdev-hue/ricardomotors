# Ricardo Motors

Site oficial: https://ricardomotorsconsultoria.com.br/

Site estático: um `index.html` com o texto, o estilo e o código da página, e as fotos em `img/`.
Não tem build, banco de dados nem dependências. Qualquer hospedagem de site estático serve.

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | a página inteira (textos, cores, botões de WhatsApp e Instagram, mapa) |
| `img/` | fotos da página (o nome do arquivo descreve a foto) |
| `og.jpg` | imagem que aparece quando o link é compartilhado no WhatsApp e nas redes |
| `favicon.svg` | ícone da aba do navegador |
| `robots.txt`, `sitemap.xml` | orientações para o Google |
| `vercel.json` | configuração para a Vercel |
| `_headers` | a mesma configuração para Cloudflare Pages ou Netlify, se um dia mudar de hospedagem |

## Como alterar

- Texto: edite direto no `index.html`.
- WhatsApp, Instagram e endereços: no fim do `index.html`, no bloco `window.DEMO_CLIENT`.
- Foto: troque o arquivo em `img/` (mesmo nome) ou aponte o `<img src>` para um arquivo novo.

## Meu site (Painel Renderiza)

O `<script data-codigo="ricardo-motors">` no fim do `<head>` liga o site ao Meu site: o que o cliente publica no
Painel Renderiza aparece por cima do que está no `index.html`. Se o painel não responder, a conta for desconectada ou o
script sair, o site mostra o `index.html` como está (a versão inicial). Não apague as marcações `data-site-*`: são
elas que dizem ao script o que pode mudar.

A cada alteração enviada para a branch principal, a hospedagem publica sozinha.

## Publicação (Vercel)

Importar este repositório na Vercel: preset **Other**, sem comando de build, pasta publicada = raiz.
Domínio: em *Settings > Domains*, adicionar `ricardomotorsconsultoria.com.br` e `www.ricardomotorsconsultoria.com.br` e criar no
Registro.br os registros DNS que a Vercel mostrar.

Feito pela Renderiza em 2026-11-25.
