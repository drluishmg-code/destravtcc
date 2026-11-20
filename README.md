# Destrav TCC — site institucional

Site de divulgação do app **Destrav TCC**, feito na mesma estrutura do site
do AneStudy, com a paleta verde-azulada do ícone do app.

Serve para:
- Divulgar o app (botões "Em breve" para App Store e Google Play, fáceis de
  ativar quando publicar — veja abaixo).
- Hospedar a **Política de Privacidade** e os **Termos de Uso**, exigidos
  pela App Store e pela Google Play e usados nos links da tela de assinatura
  do app.

Endereço (GitHub Pages): https://drluishmg-code.github.io/destravtcc/

| Página | Link |
|---|---|
| Início | https://drluishmg-code.github.io/destravtcc/ |
| Política de Privacidade | https://drluishmg-code.github.io/destravtcc/privacy.html |
| Termos de Uso | https://drluishmg-code.github.io/destravtcc/terms.html |
| Contato / Suporte | https://drluishmg-code.github.io/destravtcc/contact.html |

## Estrutura de pastas

```
destravtcc/
├── index.html          → página principal
├── privacy.html        → Política de Privacidade
├── terms.html          → Termos de Uso (inclui as condições da assinatura)
├── contact.html        → Contato (pode ser usado como "URL de suporte")
├── style.css
├── script.js
├── manifest.json
├── sitemap.xml
├── .nojekyll
├── assets/
│   ├── logo.png              (ícone do app, 512×512)
│   ├── apple-touch-icon.png  (180×180)
│   ├── favicon.ico
│   ├── social-preview.png    (1200×630, imagem de compartilhamento)
│   └── screenshots/          (1290×2796 — mesmo tamanho aceito pela App Store)
│       ├── mapa.jpg
│       ├── situacao.jpg
│       ├── experimentos.jpg
│       ├── rotinas.jpg
│       ├── calendario.jpg
│       ├── previsoes.jpg
│       ├── exportar.jpg
│       └── calendario-escuro.jpg
└── ferramentas/
    └── publicar-lojas.py     → ativa os botões das lojas
```

As capturas foram geradas a partir do próprio app (pasta `www`), com dados
fictícios de exemplo de alguém escrevendo um TCC.

## Quando o app for publicado

1. Abra `ferramentas/publicar-lojas.py` e preencha `APPSTORE_URL` e/ou
   `GOOGLE_PLAY_URL`.
2. Rode, na raiz do repositório: `python3 ferramentas/publicar-lojas.py`
3. Troque "Em breve na App Store e no Google Play" no bloco `#download` do
   `index.html`, se quiser.
4. `git add . && git commit -m "Ativa botões das lojas" && git push`

## Publicar no GitHub Pages

Repositório → Settings → Pages → Source: "Deploy from a branch" →
Branch: `main` / pasta `/ (root)` → Save. Em 1–2 minutos o site fica no ar.
