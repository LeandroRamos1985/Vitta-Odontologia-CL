# D&R Realty — Site Quality Score

**Data da auditoria:** 13/09/2026  
**Build auditado:** pacote estático multilíngue entregue neste ZIP  
**Status geral:** **NOT READY FOR PRODUCTION**  
**Resultado:** 40 Aprovados · 26 Atenção · 0 Falhou · 6 Não aplicáveis  
**Aprovação entre itens aplicáveis:** 40/66 = **60,6%**

> Não existem falhas críticas de estrutura no pacote, porém existem bloqueadores de publicação que dependem de integrações, dados/autorizações do cliente e testes no domínio final. Por isso o projeto **não** recebe `READY FOR PRODUCTION` neste momento.

## Bloqueadores de publicação

- Endpoint real de formulário / integração com LeadPilot CRM ainda não fornecido.
- MLS/IDX autorizado e atualizado ainda não conectado; nenhuma listagem ativa foi inventada.
- GA4/Tag Manager/Search Console sem IDs/verificação do cliente.
- Avaliações exibidas no site atual ainda precisam de verificação na fonte original antes do go-live.
- Licença/brokerage/Equal Housing disclosures aplicáveis precisam ser confirmados.
- Privacy/Terms e eventual consentimento de cookies precisam de revisão jurídica final.
- SSL, redirects, headers reais, Lighthouse e Core Web Vitals só podem ser validados no host/domínio final.
- Logo/fotos da equipe estão referenciados a partir do site atual; para produção recomenda-se hospedar cópias autorizadas no novo projeto.
- Hero usa vídeo 4K remoto de Pexels. Antes do go-live, gerar versão otimizada 1080p (MP4/WebM) hospedada no próprio CDN/site.

## Auditoria dos 72 itens

| # | Item | Status | Evidência / observação |
|---:|---|---|---|
| 1 | CTA principal na primeira dobra | **Aprovado** | Hero contém CTAs principais visíveis sobre vídeo. |
| 2 | CTAs claros e consistentes | **Aprovado** | Linguagem consistente para contato, busca e equipe nos 3 idiomas. |
| 3 | CTA fixo no mobile | **Aprovado** | Barra fixa mobile com telefone e e-mail. |
| 4 | Promessa de tempo de resposta | **Não aplicável** | Não existe SLA específico confirmado; não foi inventada promessa. |
| 5 | Página de obrigado | **Aprovado** | `thanks.html` existe nos 3 idiomas e está `noindex`. |
| 6 | Formulários com validação/erro/sucesso | **Atenção** | Validação HTML/JS existe, mas entrega real usa fallback `mailto:` até haver endpoint. |
| 7 | Links/URLs amigáveis | **Aprovado** | Estrutura limpa `/`, `/pt/`, `/es/` e páginas legais simples. |
| 8 | Cases/resultados autorizados | **Não aplicável** | Nenhum case/resultado foi fornecido; nada foi inventado. |
| 9 | Avaliações reais/verificáveis | **Atenção** | Trechos vêm do site atual; verificação Google/Zillow é obrigatória antes do go-live. |
| 10 | Mapas, endereço e rotas | **Aprovado** | Google Maps + endereço 47 Third St #201, Cambridge, MA 02141. |
| 11 | Responsividade completa | **Atenção** | CSS responsivo implementado e estrutura validada; QA visual final em navegadores/dispositivos reais ainda é obrigatório. |
| 12 | Meta title único | **Aprovado** | Títulos específicos por idioma e tipo de página. |
| 13 | Meta description única | **Aprovado** | Home, Privacy e Terms têm descrições próprias. |
| 14 | H1 único + H2/H3 | **Aprovado** | Auditoria estrutural confirmou 1 H1 nas homes e hierarquia semântica. |
| 15 | Conteúdo sem duplicações desnecessárias | **Aprovado** | Conteúdo segmentado; traduções são localizadas, não blocos repetidos na mesma página. |
| 16 | Alt text contextual | **Aprovado** | Fotos da equipe são `<img>` com `alt`; imagens editoriais em CSS são decorativas. |
| 17 | Breadcrumbs | **Não aplicável** | Site institucional/one-page sem hierarquia profunda. |
| 18 | FAQ + FAQ Schema | **Não aplicável** | Não foi fornecida FAQ real; schema não foi artificialmente criado. |
| 19 | URLs amigáveis | **Aprovado** | Slugs simples e legíveis. |
| 20 | Canonical tags | **Aprovado** | Canonicals definidos e alternates `hreflang` EN/PT-BR/ES. |
| 21 | robots.txt | **Aprovado** | Arquivo criado e sitemap indicado. |
| 22 | sitemap.xml | **Aprovado** | Inclui páginas públicas indexáveis em 3 idiomas. |
| 23 | 404 personalizada | **Aprovado** | `404.html` criada e `noindex`. |
| 24 | Favicon | **Aprovado** | `assets/images/favicon.svg`. |
| 25 | Open Graph | **Aprovado** | OG title/description/url/image configurados. |
| 26 | Imagem social | **Aprovado** | `assets/images/og-dr-realty.png` 1200×630. |
| 27 | Schema LocalBusiness específico | **Aprovado** | JSON-LD `RealEstateAgent` com contatos/endereço/areas. |
| 28 | Search Console | **Atenção** | Projeto preparado; exige verificação do domínio pela conta do cliente. |
| 29 | Links quebrados | **Aprovado** | Auditoria automática local: 0 links internos quebrados; destinos públicos principais revisados. |
| 30 | Indexabilidade | **Aprovado** | Páginas públicas indexáveis; Thanks/404 `noindex`; robots/sitemap coerentes. |
| 31 | Compressão/otimização de imagens | **Aprovado** | Pexels usa parâmetros de compressão; fotos atuais passam por CDN WordPress; OG otimizado. |
| 32 | Formatos modernos | **Atenção** | Alguns assets remotos ainda são JPEG; ideal self-host AVIF/WebP em produção. |
| 33 | Lazy loading | **Atenção** | Fotos da equipe e mapa usam lazy loading; backgrounds editoriais em CSS ainda merecem otimização adicional. |
| 34 | PageSpeed/Lighthouse | **Atenção** | Necessita execução no build hospedado/domínio final. |
| 35 | Core Web Vitals | **Atenção** | Necessita medição real em produção; vídeo 4K deve ser otimizado antes. |
| 36 | Fontes/CSS/JS | **Aprovado** | Fontes do sistema; 1 CSS local e 1 JS local sem framework pesado. |
| 37 | HTTPS/SSL | **Atenção** | Depende do host/domínio final. |
| 38 | Headers de segurança | **Atenção** | `_headers`, `netlify.toml` e `vercel.json` preparados; precisa confirmar resposta HTTP real. |
| 39 | Anti-spam/bot | **Não aplicável** | Formulário ainda não possui backend; implementar no endpoint real. |
| 40 | Tratamento seguro dos dados | **Aprovado** | Build estático não armazena submissões; dados só seguem ao app de e-mail do usuário no fallback atual. |
| 41 | Política de Privacidade | **Atenção** | Criada em 3 idiomas, mas marcada para revisão jurídica final. |
| 42 | Cookies/consentimento | **Atenção** | GA está desativado; mapa/CDNs terceiros devem ser avaliados juridicamente no deploy final. |
| 43 | Dados empresariais no rodapé | **Aprovado** | Telefone, e-mail e endereço reais exibidos. |
| 44 | Google Analytics/equivalente | **Atenção** | Estrutura de eventos pronta; falta Measurement ID/consentimento. |
| 45 | Eventos de conversão | **Atenção** | Eventos `dataLayer` implementados; falta destino analytics real e validação. |
| 46 | Cliques em WhatsApp | **Não aplicável** | WhatsApp não foi confirmado como canal do negócio e não foi inventado. |
| 47 | Envios de formulário monitoráveis | **Atenção** | `lead_form_submit` é disparado ao `dataLayer`; falta GA/CRM real. |
| 48 | Origem/campanha preservada | **Aprovado** | UTM, gclid e fbclid preservados em `sessionStorage`. |
| 49 | Integração LeadPilot CRM | **Atenção** | Estrutura preparada, mas não existe endpoint/credencial fornecido para este cliente. |
| 50 | Teste real dos eventos | **Atenção** | JS e payloads revisados; não há container GA/CRM real para confirmar recepção. |
| 51 | Logo/identidade visual | **Aprovado** | Logo atual da D&R é referenciado; direção visual navy/gold refinada e consistente. |
| 52 | Informações reais do negócio | **Aprovado** | Conteúdo factual deriva do site atual; dados não confirmados foram omitidos. |
| 53 | Telefone/e-mail conferidos | **Aprovado** | `(617) 714-5674` e `homes@drrealtyma.com` conferidos no site atual. |
| 54 | Endereço/horários conferidos | **Aprovado** | Endereço conferido; horários não foram publicados porque não estão confirmados. |
| 55 | Serviços/especialidades conferidos | **Atenção** | Buy/Sell/Rent estão claros; linguagem de suporte a landlords deve ser reconfirmada pelo cliente. |
| 56 | Fotos reais autorizadas | **Aprovado** | Equipe usa fotos do site atual; editoriais usam assets Pexels free-to-use. |
| 57 | Equipe/profissionais conferidos | **Aprovado** | Cinco profissionais, cargos e contatos baseados na página atual da equipe. |
| 58 | Avaliações sem fabricação por IA | **Atenção** | Nenhuma avaliação foi inventada; os trechos atuais precisam de verificação externa antes do go-live. |
| 59 | Conteúdo adaptado ao segmento/local | **Aprovado** | Greater Boston/Cambridge e mercados reais orientam todo o conteúdo. |
| 60 | Conteúdo regulamentado | **Atenção** | License/brokerage/Equal Housing disclosures finais ainda não foram fornecidos. |
| 61 | Teste desktop | **Atenção** | Rotas/HTML/CSS testados localmente; QA visual completo em browser real/hospedado ainda pendente. |
| 62 | Teste mobile | **Atenção** | Breakpoints e CTA mobile implementados; QA visual em aparelhos reais ainda pendente. |
| 63 | Teste de formulários | **Atenção** | Regras/labels/required validados; entrega final depende do endpoint real. |
| 64 | Teste de CTAs | **Aprovado** | Auditoria automática confirmou destinos internos e protocolos principais. |
| 65 | Teste de links externos | **Aprovado** | Destinos principais (site atual, Pexels/Google Maps) revisados; sem HTTP inseguro. |
| 66 | WhatsApp, telefone e e-mail | **Aprovado** | Telefone/e-mail configurados; WhatsApp é N/A por ausência de dado confirmado. |
| 67 | Auditoria SEO | **Aprovado** | Titles, descriptions, H1, canonical, hreflang, schema, robots, sitemap, OG e indexabilidade verificados. |
| 68 | Acessibilidade básica | **Aprovado** | Skip link, labels, foco, estrutura semântica, controles de vídeo e reduced-motion incluídos. |
| 69 | Auditoria de performance | **Atenção** | Arquitetura leve; teste Lighthouse e otimização final do vídeo precisam do deploy. |
| 70 | Auditoria de segurança | **Atenção** | Sem backend sensível; headers preparados; verificação final depende da infraestrutura. |
| 71 | Domínio/SSL | **Atenção** | `drrealtyma.com` existe, porém o novo build ainda não foi implantado para validar SSL/redirects. |
| 72 | Site Quality Score final | **Aprovado** | Este documento registra status, evidências, pendências e bloqueadores. |

## Testes automáticos executados no pacote

- 13 arquivos HTML analisados.
- 0 erros estruturais no validador interno (lang, title, description, H1, canonical, IDs duplicados, labels e links locais).
- 0 links internos quebrados encontrados.
- Homes EN/PT-BR/ES confirmadas com hero `<video>` e JSON-LD válido.
- Rotas locais testadas via servidor HTTP: `/`, `/pt/`, `/es/`, Privacy nos três idiomas, `404.html`, `robots.txt` e `sitemap.xml` retornaram HTTP 200.
- CSS contém breakpoints para desktop/tablet/mobile e CTA fixo mobile.
- JS contém preservação de atribuição e eventos de conversão no `dataLayer`.

## Critério para READY FOR PRODUCTION

Alterar o status para `READY FOR PRODUCTION` somente depois de resolver os bloqueadores acima e repetir a auditoria no domínio final, sem falhas críticas e com as integrações reais confirmadas.
