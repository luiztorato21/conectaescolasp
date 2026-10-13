# Conecta Escola SP — protótipo navegável

Protótipo estático baseado no PRD. Dados demonstrativos e decisões ficam no `localStorage` do navegador; não há integração com a SED, autenticação ou persistência no servidor.

## Rodar localmente

```bash
npm install
npm run dev
```

## Vercel

Importe este diretório como projeto na Vercel. O `vercel.json` já define o build Vite e a pasta `dist`. Também é possível executar `npm run build` para verificar o pacote.

Use o seletor **Visão Professor / Visão Diretor** no topo para percorrer os dois fluxos demonstrativos. O botão **Reiniciar demonstração** limpa apenas os dados deste protótipo no navegador.
