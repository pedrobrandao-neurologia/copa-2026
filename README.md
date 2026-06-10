# Copa 2026 · Painel

Painel não-oficial para acompanhar a Copa do Mundo FIFA 2026 (EUA · Canadá · México). Aplicativo HTML standalone, sem servidor e sem dependências de build: é um único arquivo `index.html`.

## Recursos

- **Tabelas de grupos ao vivo** com critérios oficiais de desempate.
- **Feed automático de resultados** via API pública (não-oficial) da ESPN (`fifa.world`), com placares ao vivo durante os jogos. Atualiza sozinho a cada 90s na janela do torneio.
- **Chaveamento do mata-mata** preenchido automaticamente conforme a classificação, incluindo decisão por pênaltis.
- **Simulador de cenários**: projeta o mata-mata "se a fase de grupos terminasse hoje" e marca cada seleção como classificada / só via melhor 3º / eliminada (cálculo matemático exato).
- **Modo "meu time"**: siga seleções, com destaque nos jogos e notificações de gol e fim de partida.
- **Compartilhar** tabela do grupo e próximos jogos (Web Share API / WhatsApp).
- **PWA**: pode ser instalado na tela de início (Adicionar à tela de início) e abre em tela cheia.
- Resultados editáveis manualmente e salvos no dispositivo (localStorage).

## Como funciona

Tudo roda no navegador. Os placares vêm do feed da ESPN por `fetch` direto (CORS liberado, sem chave de API). Como a ESPN é uma fonte não-oficial, o app sempre permite edição manual e tem um fallback de busca via IA que só funciona quando o arquivo é aberto dentro do Claude.

## Publicar no GitHub Pages

1. Crie um repositório novo e envie estes arquivos (`index.html`, `.nojekyll`, `README.md`) para a branch `main`.
2. Em **Settings → Pages**, escolha **Source: Deploy from a branch**, branch `main`, pasta `/ (root)` e salve.
3. Em ~1 minuto o site fica disponível em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`.

## Licença

Uso livre. Dados do sorteio e tabela oficial da FIFA; placares fornecidos pela ESPN (fonte não-oficial).
