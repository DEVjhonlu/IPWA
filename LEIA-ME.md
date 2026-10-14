# DOOM Online - APK e PWA

## Opcao 1: Instalar como app direto do navegador (PWA)
1. Hospede a pasta `www` em HTTPS (Netlify, Vercel ou GitHub Pages).
2. Abra o link no Chrome do celular > menu > **Instalar app / Adicionar a tela inicial**.

## Opcao 2: Gerar APK pelo PWABuilder (sem instalar nada)
Com o site no ar, va em https://www.pwabuilder.com, cole o link e escolha **Package for stores > Android**.

## Opcao 3: APK com Capacitor + Android Studio
Precisa de Node.js 18+ e Android Studio.
```bash
npm install
npx cap add android
npx cap sync
npx cap open android
```
No Android Studio: **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
Saida: `android/app/build/outputs/apk/debug/app-debug.apk`.
Troque o `appId` em `capacitor.config.json` pelo seu pacote antes de publicar.

## Observacoes
- O jogo e o DOOM shareware via js-dos e precisa de internet.
- Contas ficam salvas so no aparelho. Para login online real, use Firebase ou Supabase.
