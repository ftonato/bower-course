#Bower Course

[Bower](http://bower.io/) é um gerenciador de pacotes para a web criado pela equipe do Twitter.

**Atenção:** Toda e qualquer informação descrita nesse repositório tem como intuíto auxiliar na orientação do aprendizado da ferramenta, mas não é a documentação oficial e pode conter falhas e/ou estar desatualizado. Para evitar quaisquer problemas leia sempre a [documentação oficial](http://bower.io/docs/api/).

## Instalação
Bower é um utilitário de linha de comando e pode ser instalado através do npm.

```shell
$ npm install -g bower
```

## Configuração
O Bower, assim como a grande maioria dos gerenciadores de pacotes, é configurado através de um arquivo `.json`, chamado `bower.json`, responsável por armazenar algumas informações básicas do projeto, dependências instaladas e suas respectivas versões.

O arquivo pode ser criado manualmente ou através do comando `bower init`. Ao utilizar o comando para criar o arquivo de configuração, o próprio Bower já irá sugerir algumas informações básicas para o projeto.
Vale lembrar que se não forem alteradas as informações do arquivo durante a criação do mesmo, o Bower irá adicionar algumas informações padrões, mas que posteriormente poderão ser alteradas.

## Buscando pacotes
Através do comando `bower search <name>` é possível buscar por novos pacotes a serem adicionados as nossas dependências.
O comando irá retornar uma lista de pacotes que contenham o termo `<name>` pesquisado.

## Buscando informações dos pacotes
Na grande maioria das vezes um projeto terá mais de uma versão, e é através do comando `bower info <name>` que iremos descobrir quais as versões disponíveis de um pacote específico.

## Instalando pacotes
A instalação de um pacote o fará disponível para o uso dentro do nosso projeto. O comando de instalação possuí algumas variações que dependem do propósito da instalação, todavia o comando padrão para instalação é `bower install <name>#<target>`. Vale lembrar que `<target>` no comando de instalação de pacotes diz respeito a versão da dependência que será instalada.

**Atenção:** O fato de instalar um pacote não significa que estaremos mantendo-o disponível junto com o projeto. Para que isso também aconteça há algumas *opções* que precisam ser adicionados ao nosso comando de instalação, vamos conhecê-los:
* `--save`: Salva as dependências principais do projeto.
* `--save-dev`: Salva as dependências para o ambiente de desenvolvimento.

**Nota 01:** O comando `bower install` quando escrito dessa forma apenas baixa todas as dependências do projeto que estão armazenadas dentro do arquivo `bower.json`, enquanto o comando `bower install --production` baixa apenas as dependências de produção, armazenadas no mesmo arquivo.

**Nota 02:** Todas as dependências ficam armazenadas dentro de uma pasta chamada de `bower_components`. É possível alterar o nome da pasta padrão de dependências, para isso leia a [documentação original](http://bower.io/docs/config/#bowerrc-specification) e entenda como proceder.

**Nota 03:** Existem mais algumas *opções* que podem ser úteis para a instalação, veja como na [documentação oficial](http://bower.io/docs/api/#install-options).

## Removendo pacotes
Sempre que algum pacote não mais for utilizado, podemos removê-lo do nosso projeto através do comando `bower uninstall <name>`. Esse comando também aceita as *opções* utilizados na instalação, sendo eles `--save` e `--save-dev` com o propósito inverso, que seria remover do arquivo de configuração `bower.json`.

## Atualizando pacotes
Eventualmente precisaremos atualizar nossos pacotes e antes que isso aconteça podemos utilizar o comando `bower list` para visualizar quais pacotes temos como dependências, quais suas versões e quais são as últimas versões disponíveis para as nossas dependências.

Depois que listarmos e descobrirmos as informações necessárias, podemos atualizar nossas dependências com o seguinte comando `bower update <name>`.
O update seguirá claramente aquilo que estiver documentado no arquivo `bower.json` por isso é essencial que a versão da sua dependência tenha sido configurada corretamente, se alguma dúvida surgir leia a [documentação oficial da instalação](http://bower.io/docs/api/#install) para melhor compreensão.

**Atenção:** É importante saber com qual especificação de versão as suas dependências trabalham, isso facilitará na hora da atualização.

**Nota 01:** Seguem algumas explicações básicas de como funcionam as documentações das **versões** para atualizações das dependências.

Versão | Validações de update
------ | ------
1.1.10    | É aceito apenas a 1.1.10
~1.1.10   | É aceito a 1.1.28, mas não é aceito 1.2.6
^1.1.10   | É aceito a 1.5.3, mas não é aceito 2.0.0
>1.1.10   | É aceito qualquer versão maior a 1.1.10
>=1.1.10  | É aceito qualquer versão maior ou igual a 1.1.10
<1.1.10   | É aceito qualquer versão menor a 1.1.10
<=1.1.10  | É aceito qualquer versão menor ou igual a 1.1.10
latest    | É aceito qualquer versão menor ou igual a 1.1.10

## Como ajudar?
Você quer contribuir para melhorar esse material? Incrível! Há alguns passos que você pode seguir para contribuir, veja abaixo.

* Abra uma [nova issue](https://github.com/ftonato/bower-course/issues/new) para relatar quais possíveis erros ou propor novos recursos.
* Envie um pull request com sua sugestão/correção.

## Licença
Código licenciado sob uma [MIT-style License](https://github.com/ftonato/bower-course/blob/master/LICENSE).
