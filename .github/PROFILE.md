# Manutenção do perfil

## Conteúdo e imagens

- `README.md`: versão principal em português.
- `README.en.md`: versão em inglês; manter as duas versões em sincronia.
- `assets/*.svg`: banner e capas vetoriais dos projetos. São ilustrações, não capturas das interfaces.
- O endereço do portfólio é `https://joaopedrofernandes.com.br`. A indicação “em construção” deve ser removida nas duas versões quando o site estiver disponível.

## Cobrinha das contribuições

O workflow `.github/workflows/snake.yml` usa Platane/snk para gerar a animação com o calendário real de contribuições de `sistemout123`. As imagens têm versões clara e escura e são publicadas na branch `output`.

O workflow executa:

- No primeiro push para `main` que inclua o workflow ou alterações nos READMEs.
- Diariamente, às 09:17 UTC (06:17 em Fortaleza), sujeito à fila do GitHub Actions.
- Manualmente, em **Actions → Atualizar cobrinha de contribuições → Run workflow**.

As imagens do README ficam disponíveis após a primeira execução bem-sucedida. O workflow usa o `GITHUB_TOKEN` automático com `contents: write`; não é necessário criar um token pessoal, configurar a VPS ou habilitar o GitHub Pages.

Se a animação não aparecer, confira a execução em Actions e a existência de `github-snake.svg` e `github-snake-dark.svg` na branch `output`. Em repositórios públicos sem atividade por 60 dias, o GitHub pode desabilitar workflows agendados; nesse caso, reative o workflow em Actions.

As ações estão fixadas por SHA. Ao atualizar suas versões, confira a documentação de [Platane/snk](https://github.com/Platane/snk) e [ghaction-github-pages](https://github.com/crazy-max/ghaction-github-pages).
