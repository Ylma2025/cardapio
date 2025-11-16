# Cardápio Digital — Ylma Cakes

Arquivos neste repositório:
- `index.html` — página do cardápio (único arquivo, responsivo, imagens ilustrativas).
- `README.md` — instruções.

## Publicar no GitHub Pages (passo a passo)
1. Crie um repositório público no GitHub (ex.: `cardapio-ylma-cakes`).
2. Faça upload dos arquivos `index.html` e `README.md` na raiz do repositório.
   - Pelo site: Repositório → Add file → Upload files → Commit changes.
3. Vá em **Settings > Pages** (ou **Code and automation > Pages**).
4. Em **Build and deployment** / Source:
   - Escolha **Deploy from branch**.
   - Branch: **main** (ou `master`).
   - Folder: **root**.
5. Salve. Em alguns minutos o site estará disponível em:
   `https://<SEU_USUARIO>.github.io/<NOME_DO_REPO>/`

## Gerar QR Code
Após o site estar publicado, gere o QR apontando para:
`https://<SEU_USUARIO>.github.io/<NOME_DO_REPO>/`

Opções para gerar QR:
- Online: https://www.qr-code-generator.com/ (cole o link e baixe PNG).
- Local (Python):
```bash
pip install qrcode[pil]
python - <<'PY'
import qrcode
url = "https://<SEU_USUARIO>.github.io/<NOME_DO_REPO>/"
img = qrcode.make(url)
img.save("ylma_menu_qr.png")
print("QR salvo em ylma_menu_qr.png")
PY
