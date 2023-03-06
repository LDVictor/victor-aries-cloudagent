# Anotações

Para instalar os Ledgers no exemplo Alice/Faber, foi necessário instalar o Ubuntu 18.04, seguir o guia de instalação (https://github.com/LDVictor/victor-aries-cloudagent/blob/main/demo/README.md) e instalar todas as extensões via pip 3.

Para executar o exemplo, é necessário a seguinte adaptação:

 - Executando Faber

$ cd victor-aries-cloudagent/demo/
$ LEDGER_URL=http://localhost:9000 DEFAULT_POSTGRES=true python3 -m runners.faber --port 8020

 - Executando Alice
$ cd victor-aries-cloudagent/demo/
$ LEDGER_URL=http://localhost:9000 DEFAULT_POSTGRES=true python3 -m runners.alice --port 8030