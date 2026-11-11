# Tasks do site Arrua

## Hospedagem
- [ ] Migrar do Netlify para o Vercel (plano Hobby, grátis). Motivo: o Netlify grátis só deixa ~20 publicações por mês e travou em 01/09; desde então o que estava no ar era a versão de 31/08 (o ramo `curriculo-dev-hub`, que nem existe mais). Na Vercel o site divide a cota com o site do casamento, e sobra: o casamento usou 108 MB de 100 GB em 30 dias.
  - [x] `.vercelignore` com `luiz.html`, os `.md` e o `_redirects`. Ele substitui o `_redirects`, que só funciona no Netlify. ✅ 10/11
  - [x] Projeto `arrualuiz` na Vercel (conta ArruaDEV), ligado ao `master`: cada push no `master` publica. ✅ 10/11
  - [x] Testar o endereço novo (https://arrualuiz.vercel.app): as páginas abrem com o `master` e `luiz.html`, os `.md` e o `_redirects` dão "não encontrado". ✅ 10/11
  - [x] A home estava quebrada desde o merge de 01/09 (22261bd, "Merge branch 'master' into curriculo-dev-hub"): ele juntou a home de janeiro com a de agosto e ficaram dois cabeçalhos, a coluna do meio vazia e um relógio parado. Como a Netlify travou no mesmo dia, nunca foi pro ar e ninguém viu. Voltei a home do fim do ramo (923fdba, com os ajustes de escala de 31/08) mais o link "Sobre mim" do menu. ✅ 10/11
  - [ ] Atualizar o link do site no LinkedIn, no GitHub (selo no `arrualuiz/README.md`) e no currículo.
  - [ ] Depois de 28/11 (quando os créditos do Netlify voltam): trocar o site do Netlify por um redirecionamento para o endereço novo e, quando nada mais apontar pra lá, apagar o site no Netlify e o arquivo `_redirects`.
  - [ ] Depois de migrar: os itens abaixo que citam Netlify Functions viram Vercel Functions (pasta `api/`), e o login fica com o Supabase Auth.

## Base e navegação
- [x] Padronizar menu de `index.html`, `news.html`, `sobre.html` e `curriculo.html`.
- [x] Corrigir estrutura do `index.html` para manter `header`, menu e conteúdo dentro do `body`.
- [x] Ajustar o dashboard inicial para manter colunas lado a lado com proporção mais consistente.
- [x] Ajustar dashboard inicial para caber melhor em monitor 1440x900 sem depender de zoom 80%.
- [x] Adicionar timestamp no cabeçalho das páginas principais.
- [x] Separar hora no centro e data no canto direito do cabeçalho.
- [x] Refinar responsividade da tela inicial e do Dashboard / News para monitor menor.
- [x] Atualizar seção de links da página principal com registros, formulários, dashboards e links pessoais.
- [ ] Revisar links fáceis do dashboard (`Links` e `Atalhos`) e separar o que será público do que vai para área logada.

## Páginas
- [x] `bia.html`: manter como está por enquanto.
- [x] `curriculo.html`: versão nova atualizada com dados consolidados, selo Zenvia e textos expansíveis.
- [x] `curriculo.html`: aumentar respiro entre blocos e renomear textos de candidatura para `Inscrições`.
- [x] `curriculo.html`: revisar acentos e usar nomes formais das universidades.
- [x] `sobre.html`: virou página "Sobre mim" com traços de personalidade/qualidades (complementa o `curriculo.html`, que fica só com dados profissionais). Voltou pro menu público em `index.html`, `news.html` e `curriculo.html`.
- [x] `luiz.html`: manter no git, mas tirar do menu público e bloquear acesso direto no Netlify.
- [ ] `teste.html`: revisar o conteúdo e decidir se vira página privada, rascunho ou descarte.

## APIs e dados
- [ ] Trocar NewsAPI direta no front por Netlify Functions para proteger chaves e reduzir problemas de CORS.
- [ ] Definir fonte de notícias/tokens para Coritiba e Santos.
- [ ] Criar card/calendário CSS com próximos jogos de Coritiba e Santos.
- [ ] Criar módulo de moedas/currencies: USD, EUR e cripto, preferencialmente via função serverless.

## Área logada
- [ ] Escolher modelo de autenticação: Netlify Identity, Supabase Auth ou login simples via Netlify Function.
- [ ] Criar uma página privada para links pessoais, chaves, rotinas e painéis que não devem aparecer para recrutador.
- [ ] Remover do público links sensíveis como senhas, planilhas pessoais e diário.
