# Vida Financeira – como gerar e instalar o APK

O APK é compilado pelo próprio GitHub (Actions), então você não precisa instalar nada no computador.

## 1. Subir no GitHub (pelo site)
1. Extraia o zip e entre na pasta.
2. No GitHub, crie um repositório novo (ex.: `vida-financeira`).
3. Clique em **uploading an existing file** e arraste TODO o conteúdo da pasta (inclusive a pasta `.github`, que pode estar oculta).
4. Clique em **Commit changes** (branch `main`).

### Se a pasta `.github` não subir
Pastas que começam com ponto costumam ficar ocultas. Faça assim:
1. No repositório: **Add file → Create new file**.
2. No nome, digite exatamente `.github/workflows/build-apk.yml` (as barras criam as pastas).
3. Abra o arquivo `workflow-copia/build-apk.yml` deste zip, copie o conteúdo e cole.
4. **Commit changes**.

## 2. Gerar o APK
- O build começa sozinho após o commit. Acompanhe na aba **Actions** (leva uns 5 a 10 minutos).
- Se não começar: **Actions → Gerar APK → Run workflow**.
- Se aparecer erro de permissão ao publicar: **Settings → Actions → General → Workflow permissions → Read and write permissions → Save**, e rode de novo.

## 3. Instalar no celular
1. No celular, abra o repositório no GitHub → **Releases** (lado direito) → baixe **VidaFinanceira.apk**.
2. Abra o arquivo. Se pedir, permita **instalar apps desconhecidos** para o navegador.
3. Se o Play Protect avisar, toque em **Instalar mesmo assim** (o app não vem da Play Store).

## Atualizações
Cada novo commit gera uma nova versão em Releases. A chave de assinatura é fixa (`debug.keystore`), então a nova versão instala por cima da antiga **sem apagar seus dados**.

## Importante
- Os dados ficam salvos só dentro do app no aparelho. Se desinstalar o app, eles se perdem.
- Para mudar o app, edite `www/index.html` no GitHub.
