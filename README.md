# D&R Realty — Premium Multilingual Website

Projeto estático premium criado para substituir a experiência atual de **drrealtyma.com**, usando o site existente como fonte factual e as referências visuais definidas pelo cliente como direção de qualidade (sem copiar layouts).

## O que está incluído

- Home completa em **English**, **Português (BR)** e **Español**.
- Hero com **vídeo 4K de Boston** em movimento (Pexels, free-to-use), com controle de pausa e suporte a `prefers-reduced-motion`.
- Navegação responsiva, CTAs, busca orientativa, serviços, regiões, equipe, avaliações, contato, mapa e recrutamento.
- Equipe e contatos baseados no site atual da D&R Realty.
- `privacy.html`, `terms.html`, `thanks.html`, `404.html`, `robots.txt`, `sitemap.xml`, favicon, Open Graph e JSON-LD `RealEstateAgent`.
- Preservação de UTMs/gclid/fbclid em `sessionStorage` para futura integração com LeadPilot CRM.
- Eventos preparados em `dataLayer` para telefone, e-mail, busca e formulário.
- Configurações de headers para Netlify/Vercel.

## Estrutura de idiomas

- `/index.html` — English (default)
- `/pt/index.html` — Português (BR)
- `/es/index.html` — Español

## Como abrir no computador

A forma mais confiável é abrir a pasta do projeto no terminal e executar:

```bash
python -m http.server 8000
```

Depois abra `http://localhost:8000` no navegador.

Também é possível abrir `index.html` diretamente, mas um servidor local reproduz melhor o comportamento de produção.

## Antes de publicar

O projeto é uma **production candidate**, não uma versão final de produção. Ver `SITE-QUALITY-REPORT.md`.

Os principais itens que exigem confirmação/configuração são:

1. Conectar um **form endpoint real** (idealmente LeadPilot CRM/API) no lugar do fallback atual por e-mail.
2. Configurar **GA4/Tag Manager** e validar eventos reais.
3. Conectar/validar **MLS/IDX** em uma fonte autorizada e atual.
4. Confirmar com o cliente se todos os membros da equipe, telefones, e-mails e serviços continuam atuais.
5. Validar avaliações na fonte original (Google/Zillow/etc.) antes da publicação.
6. Receber/confirmar **número(s) de licença, brokerage disclosures e Equal Housing disclosures** aplicáveis.
7. Revisar juridicamente Privacy/Terms e necessidade de consentimento de cookies.
8. Hospedar localmente os ativos autorizados da marca/equipe e produzir uma versão otimizada do vídeo hero (1080p WebM/MP4) para performance.
9. Executar Lighthouse/Core Web Vitals no domínio final e validar SSL, redirects, Search Console e headers reais do host.

## Fontes usadas no projeto

- Dados factuais e fotos da equipe: `https://drrealtyma.com/`
- Vídeo hero de Boston: Pexels, vídeo 12595925, James Hamar (free to use under Pexels license)
- Imagens editoriais de Boston/interiores: Pexels (free-to-use assets)

Nenhuma listagem ativa, estatística de vendas, número de anos, prêmio, licença ou depoimento novo foi inventado.
