# Contribuir para o PHP Como Deve Ser

Gosta do _PHP Como Deve Ser_(http://phptherightway.com) e quer colaborar? Boa! Há muitas formas de ajudar.

Por favor, tire um momento para ler este documento, a fim de tornar o processo de contribuição fácil e eficaz para 
todos os envolvidos.

Seguir estas orientações significa que você respeita o tempo que os programadores gastam em gerenciar e desenvolver 
este projeto de código aberto. Em troca, eles podem ajuda-lo a abordar situações ou avaliar correções e funcionalidades.

## Usar o 'issue tracker'

O [issue tracker](https://github.com/codeguy/php-the-right-way/issues) é o canal preferido para alterações: erros 
ortográficos, alterações de texto, novos conteúdos e geralmente [submissão de pull requests](#pull-requests), mas 
respeite as seguintes restrições:

* Por favor **não** use o _issue tracker_ para solicitações suporte (use o [Stack Overflow](http://stackoverflow
.com/questions/tagged/php) ou o IRC).

* Por favor, **não** se desvie da questão. Mantenha a discussão sobre o tema e respeite as opiniões dos outros.


<a name="pull-requests"></a>
## Pull Requests

Os *Pull Requests* são uma ótima forma de adicionar novos conteúdos ao *PHP Como Deve Ser*, além de atualizar 
quaisquer problemas do navegador ou outras mudanças de estilo. Praticamente qualquer tipo de mudanças é aceite se for
 construtivo.

O seguinte processo contém a melhor maneira de incluir o seu trabalho neste projeto:

1. Fazer [Fork](http://help.github.com/fork-a-repo/) ao projeto, fazer um *clone* do *fork*, e configurar os *remotes*:

   ```bash
   # Fazer *clone* do *fork* do repositório no diretório atual
   git clone https://github.com/<your-username>/php-the-right-way.git
   # Navegue até ao diretório que acabou de criar
   cd php-the-right-way
   # Ligue o repositório original ao "upstream" remoto
   git remote add upstream https://github.com/codeguy/php-the-right-way.git
   ```

2. Se você fez *clone* há algum tempo, obtenha as últimas alterações do *upstream*:

   ```bash
   git checkout gh-pages
   git pull upstream gh-pages
   ```

3. Crie um novo _branch_ (fora do _branch_ principal de desenvolvimento do projeto) para conter a suas alterações ou 
correções:

   ```bash
   git checkout -b <topic-branch-name>
   ```

4. Instalar o [Jekyll](https://github.com/jekyll/jekyll/) gem e dependências para pré-visualizar localmente:

    ```bash
    # Install the needed gems through Bundler
    bundle install --path vendor/bundle
    # Run the local server
    bundle exec jekyll serve
    ```

5. Faça _commit_ das suas alterações em partes lógicas. Siga as diretrizes do artigo 
[git commit message guidelines](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
   de forma que o seu conteúdo seja _merged_ ao projeto principal. Utilize o Git 
   [interactive rebase](https://help.github.com/articles/interactive-rebase)
   para organizar os seus _commits_ antes de torná-los públicos.

6. Faça _merge_ (ou _rebase_) do _branch_ *upstream* no seu _branch_ de desenvolvimento:

   ```bash
   git pull [--rebase] upstream gh-pages
   ```

7. Faça _push_ do seu _branch_ para o seu _fork_:

   ```bash
   git push origin <topic-branch-name>
   ```

8. [Abrir um _Pull Request_](https://help.github.com/articles/using-pull-requests/)
    com um título e descrição claros.


## Acordo de Contribuição e Utilização

Ao enviar um _Pull Request_ para este repositório, você concorda em permitir que os proprietários do projeto 
licenciem o seu trabalho sob os termos da [Creative Commons Attribution-NonCommercial-ShareAlike
3.0 Unported License](http://creativecommons.org/licenses/by-nc-sa/3.0/).

O mesmo conteúdo e licença serão usados para todas as publicações do _PHP: Como Deve Ser_, incluindo - mas não 
limitando a:

* [phptherightway.com](http://phptherightway.com)
* Traduções do phptherightway.com
* [LeanPub: PHP The Right Way](https://leanpub.com/phptherightway/)
* Traduções do "LeanPub: PHP The Right Way"

Todo o conteúdo é, e sempre será, totalmente gratuito.

## Guia de estilo do contribuidor

1. Use a ortografia em inglês americano (*apenas para o repositório principal em inglês*)
2. Use quatro (4) espaços para indentar o texto; não use _tabs_
3. Não ultrapasse os 120 caracteres por linha
4. Exemplos de código devem seguir as recomendações do PSR-1 ou superior
5. Utilize o [GitHub Flavored Markdown](http://github.github.com/github-flavored-markdown/) para todo o conteúdo
6. Utilize URLs agnósticas ao idioma quando se referir a sites externos como o [php.net](http://php.net/urlhowto.php)
