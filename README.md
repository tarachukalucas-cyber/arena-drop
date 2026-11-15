# ARENA DROP

Protótipo 3D multiplayer de Battle Royale para navegador. Não há bots: o servidor só inicia uma partida quando existem pelo menos dois jogadores humanos conectados.

## Arquivos
- index.html: cliente 3D Three.js, menu, movimentação e caixas.
- server.js: servidor multiplayer WebSocket Node.js.
- render.yaml: configuração inicial para hospedar o servidor no Render.
- .github/workflows/pages.yml: publicação automática no GitHub Pages.

## Publicar o servidor multiplayer
1. Importe este repositório no Render como Web Service.
2. O Render pode detectar render.yaml; use npm install e npm start.
3. Após o deploy, copie o endereço HTTPS do serviço e converta para WebSocket: https://nome.onrender.com vira wss://nome.onrender.com.
4. Cole essa URL no campo de servidor do menu do jogo.

## Publicar o site
No GitHub, abra Settings > Pages e selecione GitHub Actions como fonte. O workflow publica a raiz do repositório após um push. Endereço esperado: https://tarachukalucas-cyber.github.io/arena-drop/

## Controles
WASD para andar, mouse para mirar, clique para disparar, E para coletar caixas, Espaço para pular e Shift para correr.

## Limitações
Esta é uma base experimental, não uma versão comercial pronta. O multiplayer usa WebSocket, mas ainda precisa de validação autoritativa de movimento e tiros, autenticação, gerenciamento de partidas e testes de carga. O sistema de amigos busca jogadores online e envia avisos, sem lista persistente. Ainda faltam paraquedas animado, zona segura, inventário completo, áudio e matchmaking avançado. O servidor gratuito pode hibernar quando inativo.