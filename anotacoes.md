# Anotações

Para instalar os Ledgers no exemplo Alice/Faber, foi necessário instalar o Ubuntu 18.04, seguir o guia de instalação (https://github.com/LDVictor/victor-aries-cloudagent/blob/main/demo/README.md) e instalar todas as extensões via pip 3.

Para executar o exemplo, é necessário a seguinte adaptação:

 - Executando VON Network:

$ cd von-network/
$ ./manage start --logs

 - Instalando extensões necessárias:

$ pip3 install multidict typing_extensions attr yarl async_timeout idna_ssl attrs charset_normalizer aiosignal qrcode asyncpg "prompt-toolkit<3.0.0" pygments aries-askar

$ python3 -m pip install aiohttp

 - Executando Faber

$ cd victor-aries-cloudagent/demo/
$ LEDGER_URL=http://localhost:9000 DEFAULT_POSTGRES=true python3 -m runners.faber --port 8020

 - Executando Alice
$ cd victor-aries-cloudagent/demo/
$ LEDGER_URL=http://localhost:9000 DEFAULT_POSTGRES=true python3 -m runners.alice --port 8030
