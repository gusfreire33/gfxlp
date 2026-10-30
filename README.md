# GFX — Página institucional

Site estático, sem build e sem dependências: um `index.html` com o CSS embutido, imagens em `assets/` e fontes do Google Fonts (Sora, Inter, DM Mono).

## Rodar localmente
```bash
cd gfx-site
python3 -m http.server 8080      # ou: npx serve .
# abra http://localhost:8080
```
Abrir o `index.html` direto com duplo clique também funciona.

## Estrutura
```
gfx-site/
├── index.html              # a página inteira (HTML + CSS)
├── assets/
│   ├── gfx-logo-gold.png   # logotipo oficial (ouro)
│   ├── fundador.jpg
│   ├── sede-recife.jpg
│   ├── sede-estudio.jpg
│   ├── sede-estacao.jpg
│   └── equipe/
│       ├── gustavo.jpg     # ⚠ baixa resolução — substituir pelos originais
│       ├── wagner.jpg      # ⚠ idem
│       ├── mariana.jpg     # ⚠ idem
│       └── victor.jpg      # ⚠ idem
└── README.md
```

## Pendências (buscar por `[` no index.html)
- `[Telefone / WhatsApp]`, `[E-mail]`, `[contato@seudominio.com.br]` (href do botão "Fale com a GFX")
- `[Segunda a sexta]` / `[08h às 18h]` — horário de atendimento
- Fotos da equipe em `assets/equipe/` — trocar pelos arquivos originais (mesmos nomes)
- Nome do fundador: a seção "Quem está por trás" usa "Marvin"; o time usa "Wagner César"

## Seções (ids para navegação)
`#topo` hero · `#quem-somos` · `#ecossistema` · `#time` · `#wonnemax` · `#tecnologia` · `#wdx` · `#fundador` · `#recife` · `#localizacao` · `#valores` · `#contato`

## Design
Segue o GFX Design System v1.0: Tinta `#191916` / Carvão `#292925` como base, Ouro GFX `#B77E45` como acento (≤15% da peça), texto de destaque em Ouro Claro `#C9A26A`, sem sombras projetadas, cartões com raio 10px, botões em pílula de 48px, seções separadas por 96px. Tokens de cor e tipografia estão no topo do `<style>` em `index.html`.

## Deploy
É um site estático: suba a pasta em Vercel, Netlify, Cloudflare Pages, GitHub Pages ou qualquer hospedagem com HTML. Nenhum passo de build.

## Sugestões para o Claude Code
- Trocar o bloco de mapa desenhado em `#localizacao` por um `<iframe>` real do Google Maps (endereço: Av. Sport Clube do Recife, 56a — Sala 01, Ilha do Retiro, Recife — PE, 50610-510)
- Ligar o botão "Fale com a GFX" a um link de WhatsApp (`https://wa.me/55...`) ou a um formulário
- Adicionar Open Graph (`og:image` com uma foto da sede) para compartilhamento
