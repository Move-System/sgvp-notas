# Notas de Versão — SGVP

Página pública com o histórico de atualizações do **SGVP — Sistema de Gestão de Votação e Plenário**.

🔗 <https://move-system.github.io/sgvp-notas/>

É a versão voltada às câmaras: descreve o que mudou em linguagem de uso, sem números de card, nomes de câmara ou detalhe técnico. O registro interno continua nos *releases* de `sgvp-backend-api` e `sgvp-online`.

## Como publicar uma versão nova

1. Duplique o primeiro `<article class="release">` do `index.html` e preencha com a versão nova, no topo da lista.
2. No artigo que deixou de ser o mais recente, remova `<span class="selo">Versão vigente</span>` — só a versão do topo leva o selo.
3. Acrescente a entrada no índice (`nav.indice`), também no topo.
4. Atualize, no cabeçalho, o número de edições e a data de "Atualizado em".
5. `git commit` e `git push` na `main`. O GitHub Pages publica sozinho em cerca de um minuto.

### Convenções do conteúdo

- **Três grupos por versão**, nesta ordem: Novidades, Melhorias, Correções. Um grupo sem itens é omitido.
- O contador ao lado do título do grupo (`.conta`) precisa bater com o número de `<li>` do grupo.
- A **ficha** traz as duas numerações reais da entrega: `Painel` é a tag do `sgvp-online`, `Serviço` é a do `sgvp-backend-api`.
- Correções são escritas pelo **sintoma que a câmara via**, no passado — "Botão de registrar presença não respondia ao toque" —, nunca pela causa técnica.
- Sem nomes de câmara: a página é indexável, e associar um cliente a uma falha não convém.

## Estrutura

Uma página só, sem dependências além das fontes do Google. Todo o CSS e o JS estão no próprio `index.html`, e os temas claro e escuro saem dos tokens no `:root`.
