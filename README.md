# INFAME · 6 YEARS — Landing Page

Landing page estática para o evento INFAME 6 anos (30.05.2026 · Brasília).
Acesso via QR Code em flyers físicos → conversão direta para Sympla.

## Stack

- HTML/CSS/JS puro (zero build, zero dependência)
- Fonte custom: Justone (`fonts/`)
- Imagens e vídeo locais (`assets/`)

## Estrutura

```
infame-lp/
├── index.html          # LP principal
├── index-print.html    # Versão para impressão / PDF
├── assets/
│   ├── img/            # Imagens (fire-mark, neon, etc)
│   ├── logo/           # Logos
│   └── video/teaser.mp4
└── fonts/Justone.{otf,ttf}
```

## Rodar local

Abrir `index.html` direto no navegador funciona, mas pra evitar problemas de CORS com fontes/vídeo:

```bash
python3 -m http.server 8000
# acessar http://localhost:8000
```

## Deploy

Site é 100% estático — qualquer provedor serve. Opções:

### Vercel (recomendado, mais simples)

1. Push deste repo pro GitHub
2. Em [vercel.com](https://vercel.com), "New Project" → importar o repo
3. Framework: "Other" · Build: vazio · Output: `./`
4. Deploy → URL `*.vercel.app` na hora
5. (Opcional) Adicionar domínio custom em "Domains"

### Netlify

1. Push pro GitHub
2. [netlify.com](https://netlify.com) → "Add new site" → "Import from Git"
3. Build command: vazio · Publish directory: `./`
4. Deploy

### GitHub Pages

1. Push pro GitHub
2. Settings → Pages → Source: `main` / root
3. URL: `https://<user>.github.io/<repo>/`

### Cloudflare Pages

1. Push pro GitHub
2. [pages.cloudflare.com](https://pages.cloudflare.com) → Create → Connect Git
3. Build command: vazio · Output: `./`

## Subir pro GitHub (primeira vez)

Repo já inicializado localmente. Faltam estes passos:

```bash
cd ~/Documents/infame-lp

# criar repo remoto via gh CLI (se tiver instalado)
gh repo create infame-lp --public --source=. --remote=origin --push

# OU manualmente: criar repo vazio no github.com, depois:
git remote add origin git@github.com:<usuario>/infame-lp.git
git branch -M main
git push -u origin main
```

## Links

- Ingressos: https://www.sympla.com.br/evento/infame-6-years/3360116
- Instagram: https://www.instagram.com/sejainfame
