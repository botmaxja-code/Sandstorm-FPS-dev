# Sandstorm-FPS-dev

A war game in development inspired by Arma Reforger.

Jogo FPS de guerra que roda 100% no navegador (Three.js r128 + assets 3D/áudio
embutidos). Tudo está no arquivo único `sandstorm_fps_v81.html` — sem backend,
sem dependências externas, sem build.

## Jogar localmente

Por causa do chat de voz (`getUserMedia`), o navegador exige **HTTPS ou
localhost**. Abra o arquivo por um servidor local:

```bash
python3 -m http.server 8000
# depois acesse http://localhost:8000/sandstorm_fps_v81.html
```

Controles: mouse (clique na tela para travar o ponteiro), teclado — pressione
`K` para ver a lista de controles.

## Deploy no Render (Static Site)

O repositório já inclui um `render.yaml` (Blueprint) configurado como site
estático. O Render serve HTTPS automático (necessário para o chat de voz) e
aplica gzip/brotli, reduzindo bastante o tráfego do arquivo.

1. No [dashboard do Render](https://dashboard.render.com), clique em
   **New → Blueprint**.
2. Conecte este repositório e selecione a branch desejada.
3. O Render detecta o `render.yaml` e cria um **Static Site** chamado
   `sandstorm-fps`.
4. Clique em **Apply**. Ao terminar, o jogo fica disponível na URL
   `https://sandstorm-fps.onrender.com` (a rota `/` serve o jogo diretamente).

Não há passo de build — o deploy apenas publica o HTML.

## Licença

Apache License 2.0 — ver `LICENSE`.

### Créditos de modelos 3D

- M1A1 Abrams — Muhamad Mirza Arrafi (CC BY 4.0)
- T-55AM2 (USSR) — 42manako (CC BY-NC 4.0, uso não comercial)
