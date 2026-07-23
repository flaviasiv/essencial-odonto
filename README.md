# Essencial Odonto — Site Institucional

Site institucional da **Essencial Odonto**, clínica odontológica localizada em Santo André, SP. Desenvolvido por Flavia Sigoli.

## Sobre o projeto

Landing page completa e responsiva para clínica odontológica, com foco em conversão via WhatsApp e apresentação dos serviços oferecidos.

## Tecnologias

- HTML5 semântico (acessibilidade com ARIA)
- CSS3 (variáveis, flexbox, grid, responsividade mobile-first)
- JavaScript vanilla
- [Swiper.js](https://swiperjs.com/) — carrossel de galeria antes/depois
- [Font Awesome 6](https://fontawesome.com/) — ícones
- [Elfsight](https://elfsight.com/) — widget de avaliações Google
- Netlify Forms — formulário de contato sem backend
- JSON-LD (Schema.org `Dentist`) — SEO estruturado
- Google Analytics 4 (gtag.js) — tracking de tráfego
- `robots.txt` + `sitemap.xml` — indexação em buscadores

## Estrutura

```
essencial-odonto-main/
├── index.html        # Página principal
├── style.css         # Estilos globais
├── javascript.js     # Scripts auxiliares
├── robots.txt        # Regras de rastreamento
├── sitemap.xml        # Mapa do site para buscadores
└── assets/           # Imagens, logos e slider
```

## Seções da página

| Seção | Descrição |
|---|---|
| Navbar | Logo + menu hambúrguer + CTA WhatsApp |
| Hero | Chamada principal + botões de ação + trust badges |
| Tratamentos | 6 cards: implantes, prótese protocolo, alinhadores, ortodontia, clínico geral, estética |
| Sobre | Missão, visão e história da clínica |
| Valores | 5 pilares: qualidade, confiança, cuidado humanizado, transformação, acessibilidade |
| Galeria | Carrossel de resultados antes/depois |
| Depoimentos | Widget de avaliações Google (Elfsight) |
| Contato | Endereço, WhatsApp, Instagram, e-mail + mapa Google |
| Footer | Menu, contato, formulário Netlify |
| Float | Botão WhatsApp flutuante |

## Informações da clínica

- **Endereço:** Av. Dom Pedro II, 1300 — Jardim, Santo André, SP — CEP 09080-000
- **WhatsApp:** (11) 99502-0445
- **Instagram:** @essencialodonto
- **E-mail:** comercial.essencialodonto@gmail.com
- **Fundação:** 2018
- **Deploy:** Netlify

## SEO e tracking

**Domínio de produção:** `https://clinicaessencialodonto.com.br/` — usado no `canonical`, Open Graph, JSON-LD, `robots.txt` e `sitemap.xml`. Se o domínio mudar, atualize essas referências.

### Ativar o Google Analytics 4
O `gtag.js` já está no `<head>` do `index.html`, mas com um Measurement ID placeholder (`G-XXXXXXXXXX`):
1. Crie uma propriedade GA4 em [analytics.google.com](https://analytics.google.com/).
2. Copie o Measurement ID (formato `G-XXXXXXXXXX`).
3. Substitua as duas ocorrências de `G-XXXXXXXXXX` em `index.html` (no `src` do script e no `gtag('config', ...)`).

### Google Search Console
1. Adicione a propriedade `https://clinicaessencialodonto.com.br/` em [search.google.com/search-console](https://search.google.com/search-console).
2. Verifique a propriedade (recomendado: via DNS ou pela tag HTML — se optar pela tag HTML, adicione a meta de verificação no `<head>` do `index.html`).
3. Submeta `https://clinicaessencialodonto.com.br/sitemap.xml` na seção "Sitemaps".

### Imagem de compartilhamento (Open Graph)
Hoje o `og:image`/`twitter:image` reaproveita `assets/hero-img.png`. O ideal é substituir por uma imagem dedicada de 1200×630px (logo + slogan) para ficar nítida nos previews do WhatsApp, Instagram e Facebook.
