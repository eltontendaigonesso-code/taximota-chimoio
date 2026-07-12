# TáxiMota Chimoio — versão PWA

Isto é um app instalável de verdade: depois de publicado, os utilizadores
abrem o link uma vez, tocam em "Instalar" e o TáxiMota fica no ecrã inicial
do telemóvel como qualquer outro app — e funciona **offline** depois da
primeira visita (os contactos e bairros ficam guardados no telemóvel).

## Ficheiros (todos na mesma pasta, sem subpastas)
- `index.html` — o aplicativo todo
- `manifest.json` — diz ao telemóvel como instalar o app (nome, ícone, cor)
- `service-worker.js` — permite funcionar sem internet depois da 1ª visita
- `icon-192.png` e `icon-512.png` — ícone do app

## Publicar pelo telemóvel (sem computador) — GitHub Pages

1. Abre https://github.com no navegador do telemóvel e cria uma conta grátis
   (se ainda não tiveres)
2. Toca no `+` no canto superior → "New repository"
3. Dá um nome (ex: `taximota-chimoio`) → marca "Public" → "Create repository"
4. Dentro do repositório, toca em "Add file" → "Upload files"
5. Toca em "choose your files" e seleciona os 5 ficheiros desta pasta
   (`index.html`, `manifest.json`, `service-worker.js`, `icon-192.png`,
   `icon-512.png`) — podes selecionar vários de uma vez
6. Desce e toca em "Commit changes"
7. Vai a "Settings" (nas abas do repositório) → "Pages" (menu lateral)
8. Em "Branch", escolhe `main` e a pasta `/ (root)` → "Save"
9. Espera 1-2 minutos e actualiza a página — vai aparecer um link tipo
   `https://teu-utilizador.github.io/taximota-chimoio/`
10. Esse é o link para partilhares no WhatsApp

## Publicar num computador (mais simples, se tiveres acesso a um)

1. Vai a https://app.netlify.com/drop
2. Arrasta esta pasta inteira para a página
3. Recebes um link em segundos

## Como testar se ficou instalável
1. Abre o link publicado no telemóvel (Chrome no Android, Safari no iPhone)
2. Android: deve aparecer uma barra "Instalar app" — ou menu ⋮ → "Instalar app"
3. iPhone: toca no botão de partilhar → "Adicionar ao ecrã principal"
4. Depois de instalado, desliga o Wi-Fi/dados e abre o app — os bairros e
   contactos já guardados continuam a aparecer

## Limitações a saber
- **Não há servidor central.** Cada telemóvel guarda os seus próprios dados
  (localStorage). Se um taxista se inscreve no telemóvel dele, esse contacto
  só aparece nesse aparelho — não é automaticamente partilhado com todos.
  Para todos verem os mesmos dados, o próximo passo é ligar isto a uma base
  de dados real (Firebase ou Supabase), gratuita para começar.
- **Coordenadas dos bairros** continuam aproximadas — confirma-as no Google
  Maps antes de divulgar amplamente.
