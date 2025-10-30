# Roleta Holagri (Jan/2026 → Jan/2027)

Projeto estático (HTML único) para sortear meses entre jan/2026 e jan/2027.
Não precisa de backend, roda em qualquer navegador.

## Como executar localmente
1. Baixe este pacote e extraia.
2. Dê duplo clique em `index.html` (ou sirva com um servidor estático, ex: `python -m http.server 8080` e acesse `http://localhost:8080`).

## Deploy rápido (estático)
### GitHub Pages
1. Crie um repositório e envie `index.html`.
2. No GitHub, abra **Settings → Pages** e selecione **Deploy from a branch** (branch `main`, pasta `/root`).
3. Acesse a URL indicada.

### Netlify
1. Acesse app.netlify.com → **Add new site** → **Deploy manually** e arraste `index.html`.
2. Ou conecte seu repositório Git e selecione build **(nenhum build, é estático)**.

### Vercel
1. Importar repositório → **Framework Preset: Other** → **Build Command: (vazio)** → **Output: /**.
2. Ou **Deploy Manual** enviando `index.html`.

### Firebase Hosting
1. `npm i -g firebase-tools`
2. `firebase login`
3. `firebase init hosting` (selecionar pasta do projeto; arquivo público: `.`)
4. `firebase deploy`

### Amazon S3 (site estático)
1. Crie um bucket público, ative **Static website hosting**.
2. Faça upload de `index.html`.
3. Defina `index.html` como **Index document**.

## Personalização
- Troque cores no `<style>` (variáveis `--accent`, `--accent-2`, etc).
- Edite o logotipo central em `drawWheel()` (texto `'HO L A G R I'`).
- Para travar “sem repetição” por padrão, já está como `allowRepeats = false`.

## Licença
Uso livre para Holagri.
