# Instituto Floratti, site piloto

Protótipo funcional para apresentação comercial. Abre direto no navegador (clique duplo em `index.html`), sem servidor e sem internet: a fonte está embutida.

## Arquivos

```
index.html        site institucional
glow-fit.html     landing do Protocolo Glow Fit
frames/           96 frames da flor (scroll-scrubbing do hero)
fonts/            Manrope embutida (.woff2)
logo-icon.png     símbolo da marca, fundo transparente
logo-full.png     logo completo (símbolo + wordmark)
icon-*.png        símbolo tintado por área de especialidade
espaco-*.jpg      fotos reais do espaço (recepção, espera, consultórios, sala de exames)
glow-hero.jpg     imagem ilustrativa no topo do Protocolo Glow Fit
```

## Para subir no ar

Serve como site estático em qualquer lugar: GitHub Pages, Vercel, Netlify. É só enviar a pasta inteira, `index.html` precisa estar na raiz.

## O que trocar antes de publicar

1. **Equipe**, a lista está com 8 profissionais; ajustar conforme quem está ativo. Cada um usa um `icon-*.png` conforme a área.
2. **Endereço e horário**, conferir no rodapé (`index.html`, seção `.dados`).

As fotos do espaço (`espaco-1.jpg` a `espaco-5.jpg`) já são fotos reais da clínica: recepção, sala de espera, dois consultórios e a sala de exames de imagem. Se quiser trocar alguma, o carrossel aceita qualquer proporção (recorte automático via `object-fit:cover`).

## Pontos de decisão que ficaram documentados

**Texto do hero.** As duas frases ("Tudo o que se cuida…" / "…sempre floresce") aparecem retas e centralizadas sobre a flor, em Manrope Light branca, com uma leve sombra escura por trás para garantir contraste (a foto é bem clara). A primeira entra suave logo no início do scroll, enquanto a flor ainda é um botão; ela se dissolve por completo antes da segunda começar a entrar (sem sobreposição das duas), e a segunda permanece até o fim. Sem `prefers-reduced-motion`, mostra direto o estado final (flor aberta + segunda frase).

**Banner do Glow Fit (home) e hero da página do protocolo.** Em vez de foto solta num quadro ao lado do texto, a imagem da modelo é o próprio fundo do banner/hero, com um gradiente escuro por cima (mais forte do lado do texto, dissolvendo para revelar a foto) — texto e imagem formam uma peça só, no mesmo tom escuro/dourado do Glow Fit. A imagem (`glow-hero.jpg`) é reaproveitada nos dois lugares.

**Vídeo da flor.** O hero usa 96 frames extraídos de um vídeo em 1920×1080 (peônia pêssego/nude).

**Hero no celular.** A faixa da flor ocupa a tela inteira (igual ao desktop, sem sobrar vão vazio antes da próxima seção), com um recorte mais fechado (`object-fit:cover` em altura cheia) que aproxima a textura das pétalas, e uma leve dissolvida na base para a transição.

**Cores dos cards.** O card "Cuidado estético" usa um malva escurecido (`#6B5B5B`) em vez do malva da marca (`#998888`): no tom original o texto ficava com contraste 2.54, abaixo do mínimo legível. Mesma lógica nos demais cards coloridos.

**Avaliações do Google.** Só a nota agregada (5,0 · 138) com link para a ficha pública. Não há pull automático de avaliações individuais: o Google não deixa escolher quais aparecem, e destacar depoimento de paciente na página da médica esbarra na Resolução CFM 2.336/2023.

**Glow Fit.** O texto foi reescrito em linguagem de acompanhamento e processo, sem promessa de resultado, com menção explícita à supervisão médica dos procedimentos. Há uma seção "o que esperar e o que não prometemos". Recomendo validação jurídica antes de publicar.

## Acessibilidade e responsivo

Respeita `prefers-reduced-motion` (sem scrubbing para quem desativou animações), tem foco visível por teclado, e o hero tem tratamento próprio no mobile, ocupando a tela cheia.
