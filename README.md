# Utilizando "*checks*" [![Build Status](https://travis-ci.org/avellar-devops/travis-setup.svg?branch=master)](https://travis-ci.org/avellar-devops/travis-setup)

Para desfrutar de build checks, utilizaremos o [Travis CI](https://travis-ci.org/account/repositories).

## Configurando o Travis CI

Primeiro, deve-se associar uma conta do GitHub ao Travis. Em seguida, pode-se adicionar repositórios para serem testados:

![homepage do Travis CI](https://i.imgur.com/z7iq6Qr.png?1)

A configuração do Travis em cada repositório se dá pelo arquivo [`.travis.yml`](https://github.com/avellar-devops/travis-setup/blob/master/.travis.yml). O tutorial pode ser lido [aqui](https://docs.travis-ci.com/user/tutorial/).

Com um arquivo de configuração pronto, o Travis irá automaticamente executar os "*checks*" em commits e pull requests:

![screenshot de checks incompletos](https://i.imgur.com/rGNlMbe.png?1)

O progresso dos builds pode ser visualizado clicando em "Detalhes" / "Details":

![screenshot do progresso dos builds](https://i.imgur.com/mY94ScK.png?1)

Assim que os testes forem todos executados, o status do pull request será atualizado automaticamente indicando o estado.

![screenshot de sucesso](https://i.imgur.com/LIs6hlq.png?1)

Após um push, haverá novamente um check para o commit que realiza o push:

![screenshot de push](https://i.imgur.com/QVTUs7r.png?1)

## Uso

O processo é inteiramente automático após a configuração inicial. Só é necessário atualizar o arquivo `.travis.yml` sempre que houver necessidade de modificar o processo de build / teste.

Para evitar um build sem necessidade (como por exemplo, em um commit que só modifica um arquivo `.md`, utiliza-se `[skip ci]` na mensagem de commit.

## TODO

- [ ] Estudar mais a fundo o arquivo de configuração `.travis.yml` (para utilização de outras linguagens e ambientes, como NodeJS)
