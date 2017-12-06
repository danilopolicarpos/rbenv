#  rbenv

## O que é o rbenv ?

É um gerenciador de versões ruby,similar ao RVM, porém mais "limpo", construída por Sam Stephenson.

## Instalando rbenv

### > macOS

É recomendado instalar o rbenv com Homebrew
```
brew install rbenv      # instala o rbenv
```
Em seguida adicione em seu arquivo ~/.bash_profile a linha abaixo:
```
eval "$(rbenv init -)"
```
Para atualizar o rbenv digite o comando abaixo:
```
brew upgrade rbenv
```
Para remover o rbenv basta digitar o comando abaixo:
```
brew uninstall rbenv
```

### > Instalando versões do Ruby

Listar as versões disponíveis do Ruby
```
rbenv install -l
```
Instalar uma versão do ruby
```
rbenv install 2.3.0
```
Para remover uma versão do ruby basta digitar o comando abaixo:
```
rbenv uninstall 2.3.0
```

### > Shims

São executáveis leves que usa seu comando junto a rbenv, inserindo um diretório de Shims na frente do seu PATH.
```
~/.rbenv/shims:/usr/local/bin:/usr/bin:/bin
```

### > rbenv rehash

Após instalar uma versão do ruby execute o comando:
```
rbenv rehash                # instala shims para todos os executáveis Ruby (irb, gem,rake, ruby)
```
É através do processo rehashing, o rbenv mantém shims nesse diretório para coincidir com todos

os comandos do Ruby.

Como funciona:
```
- Pesquise PATH um arquivo executável chamado rails
- Encontre o nome rbenv chamado rails no início do seu PATH
- Execute o shims nomeado rails, que por sua vez passa o comando junto a rbenv
```

### > rbenv local

Define uma versão específica localmente, substituindo a versão global.
```
rbenv local 2.3.0       
```
```
rbenv local     # exibe a versão local
```
### > rbenv global

Define a versão global do ruby para ser usada em todos do shells.
```
rbenv global 2.3.1       
```
```
rbenv global     # exibe a versão global
```

### > rbenv which

Exibe o caminho completo para o executável que o rbenv invocará quando executar o comando fornecido.
```
rbenv which irb
/Users/Danilo.Policarpo/.rbenv/versions/2.3.0/bin/ruby  
```

### > rbenv whence

Lista todas as versões do ruby para o comando fornecidos
```
rbenv whence ruby
2.3.0
```
