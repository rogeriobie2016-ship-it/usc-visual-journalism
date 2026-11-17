# HANDOFF · USC guest lecture deck → GitHub Pages

Para o Claude Code. Leia tudo antes de começar. A aula começa em menos de 1h: **deploy primeiro, edições depois, redeploy a cada bloco pronto.**

## Contexto
- Rogério Bié dá hoje (17/11/2026) uma aula convidada na turma de Visual Journalism do Eric Resendiz (USC Annenberg). Tema: "What's next in visual journalism? VR, GoPro, AR, 360, drones."
- Esta pasta é o deck pronto: `index.html` (HTML único, sem build), `img/` (fotos), `qr/` (QR codes pré-gerados).
- Navegação: setas, N = notas do apresentador (em PT, atributo `data-notes` de cada `<section>`, itens separados por `|`), H = esconde controles, F = tela cheia. Passos de revelação: classe `f` + `data-s="0..n"`.
- Regras fixas: **nunca usar travessão (em dash) em nada**; conteúdo dos slides em inglês; notas em português. Todo fato novo precisa de fonte verificada (abra a página, não confie em memória). Máximo de ~15 slides (pedido do Eric).
- Ética: o build WebXR do SSZ é interno (vozes sem release). Só screenshots, nunca link pro build.

## Passo 1 · Deploy imediato (5 min)
1. `git init`, adicionar `.nojekyll` vazio, commit.
2. `gh repo create rogeriobie2016-ship-it/usc-visual-journalism --public --source=. --push`
3. Ativar Pages na branch `main`, pasta raiz: `gh api -X POST repos/rogeriobie2016-ship-it/usc-visual-journalism/pages -f "source[branch]=main" -f "source[path]=/"`
4. Esperar o build e abrir a URL. Como a conta tem domínio próprio (rogeriobie.site) no site de usuário, o deck deve abrir em `https://rogeriobie.site/usc-visual-journalism/` (o github.io redireciona). Confirmar e me passar a URL final.
5. Testar no navegador: setas, QR visíveis, imagens carregando.

## Passo 2 · Edições combinadas por voz (nesta ordem de prioridade)

### A. Abertura divertida (slide 1)
- Trocar o QR principal do splat de Out of the Ashes (LA fires é pesado pra abrir) pelo **Quasar Flight**: `https://rogeriobie2016-ship-it.github.io/quasar-lab-site/flight.html` (QR já existe: `qr/36ffbb0b.png`).
- Legenda do QR: algo como "Phones out. Scan this. Fly around a black hole." Nota: perguntar "Where are you right now?" e depois: "You just learned physics by flying it, not by reading it. That's what immersive storytelling can do."
- Âncora da aula continua: "Who holds the camera?" (abertura, slide Kayapó, fechamento).

### B. Linha do tempo (slide 4): tecnologia muda, a história é o que move
Reescrever como arco "da maravilha ao storytelling", verificando cada item com fonte e link no slide:
- **1838 · Stereoscope** (Charles Wheatstone): duas imagens, uma por olho, o cérebro cria profundidade. Todo headset de VR ainda funciona assim. View-Master como descendente (verificar ano).
- **1896 · L'Arrivée d'un train en gare de La Ciotat** (irmãos Lumière). A lenda diz que o público correu da sala; historiadores consideram isso em grande parte mito. Usar como pergunta: "The legend says people ran. Why do we keep telling that story?" (liga com o tema reconstrução/ética).
- **2012 · Snow Fall** (The New York Times, John Branch): marco do jornalismo interativo; verificar o Pulitzer (2013, Feature Writing).
- **2012 · Hunger in Los Angeles** (Nonny de la Peña, Sundance).
- **2015 · The Displaced** (NYT VR, Cardboards enviados a assinantes) e **Clouds Over Sidra** (ONU, Chris Milk e Gabo Arora).
- **2017/2021 · Sam Wolson**: We Who Remain e Reeducated (manter os links atuais).
- **2026 · Out of the Ashes** (Special Jury Prize, Venice Immersive) e hoje: smart glasses, splats no celular.
- Mensagem do slide: a tecnologia sempre teve medo e deslumbramento em volta; no fim é sempre bom storytelling. Equilibrar tecnologia x potencial narrativo.
- Se ficar denso, dividir em dois slides e compensar cortando em outro lugar.

### C. Slide 8 vira "Real projects" (curtos, para ouvir e sentir, 1 min cada)
Cards com imagem/miniatura, ano, quem fez, prêmio verificado e link:
1. **Clouds Over Sidra** (UN, 2015): usado em campanhas de arrecadação da ONU.
2. **Notes on Blindness** (2016): VR feita dos diários de áudio de um homem perdendo a visão. O momento "really listening".
3. **The Displaced** (NYT, 2015).
4. **Hunger in Los Angeles** (2012), ligação pessoal com a Nonny.
5. **Uma campanha de marca/publicidade** premiada em AR/VR (pesquisar um vencedor real de Cannes Lions ou similar; IKEA Place é opção se não achar prêmio, sem inventar prêmio).
- Manter a faixa de fotos do trabalho do Rogério (Reality Looks Back, LAPL, SIGGRAPH, Pages of Prophecy, Children of the Wind).
- Os QR de demos (Pages of Prophecy, splat, Quasar) vão para o FIM da aula como "hands-on, optional", não no meio.

### D. Novo bloco: o mercado além do jornalismo (encaixar sem passar de ~15 slides; sugestão: fundir com o slide 9 "Creators")
Verificar números e links:
- Música e games: Travis Scott "Astronomical" no Fortnite (2020), Ariana Grande "Rift Tour" (2021), Sphere em Las Vegas aberta pelo U2 (2023).
- Estúdios: Atlas V (Paris: Gloomy Eyes, Battlescar), Felix & Paul (Space Explorers: The Infinite, filmado em parte na ISS), Apple Vision Pro com conteúdo imersivo de shows e esportes.
- Distribuição: festivais (Venice Immersive, Tribeca, SXSW, IDFA DocLab) → lojas (Meta Quest, Apple) → instalações itinerantes (location-based).
- Frase: "The tech is cheap and everywhere. People who can tell a real story with it are rare. That's you."

### E. Slide 14 vira plano completo de próximos passos ("starter guide")
- **Try this week:** Scaniverse no celular, fazer um splat no campus.
- **Hackathons:** SensAI (XR + AI, incluindo LA em 2026: verificar data), LA Hacks, ACM at USC. MIT Reality Hack continua.
- **Events in LA:** Infinity Festival 2026 já aconteceu (12 a 15/11) → "watch for 2027"; AWE USA em Long Beach (verificar data 2027). **Scout House / BuildFest House showcase:** PERGUNTAR ao Rogério link e data antes de publicar.
- **Funding (verificar cada data na página oficial):**
  - Games for Change Student Challenge 2027: deadline 29/03/2027, 11:59 PM PT.
  - Play4Change 2027 Award: deadline 31/12/2026, entrada gratuita, entrega em Bolonha 23 a 25/04/2027.
  - Unity for Humanity: Rogério acha que é por volta de março; confirmar.
  - Epic MegaGrants: projetos maiores, inclusive educação; confirmar se é rolling.
  - Manter Peabody, Webby, Qld XR e o QR do tracker.
  - Link "It Takes a Movie..." (algo sobre impacto no mundo): PERGUNTAR o link exato ao Rogério.
- **Mensagem:** "A lot of people use this tech just because it's new. What's missing is good stories. That's your superpower as journalists."
- **Team up:** "Bring me your stories. Let's build them together." com email (rogeriobie2016@gmail.com) e QR do portfólio.

### F. Pendências que dependem do Rogério
- Link do FEELS LIKE (Scenery): colar em `FEELS_LIKE_URL` no topo do `<script>`.
- Links da Scout House / BuildFest House showcase e do "It Takes a Movie".

## Passo 3 · Fechamento
- Atualizar os `data-notes` dos slides alterados (PT, curtos, com tempo).
- Rodar uma checagem: zero travessões (`grep -c '—' index.html` deve dar 0), todos os links abrem, imagens carregam.
- Commit e push a cada bloco (A, B, C...) para o site ficar sempre apresentável.
- Criar um `ASSETS.md` curto listando qual imagem está em qual slide, para o Rogério trocar fotos fácil (substituir o arquivo em `img/` com o mesmo nome).
- No fim, me passe: URL final, o que mudou, e o que ficou pendente.
