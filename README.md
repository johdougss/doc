# doc


### REGISTRO HEADER DE ARQUIVO


O Arquivo de troca de informações entre a Empresa e o TEIACARD é composto
de um registro header de arquivo, um ou mais lotes de Serviços e um registro
trailer de arquivo, conforme ilustra a figura abaixo:

![image](https://github.com/johnathansantos/doc/blob/master/composicao-arquivo.png)

Com a estrutura apresentada, um único arquivo pode conter vários lotes de
Serviços distintos. Este procedimento, que permite com que a Empresa e o
TEIACARD consolidem em um só arquivo todas as informações que desejam
trocar entre si, deve ser previamente acordado entre cada Empresa e o
TEIACARD.


**Lote de Serviço**: Um lote de Serviço é composto de um registro header de lote, um ou mais registros detalhe, e um registro trailer de lote.

> Um Lote de Serviço só pode conter um único tipo de Serviço

Os registros `HEADER (1)` e `TRAILER (3)` de `LOTE` e os de `DETALHE (2)` são
compostos de campos fixos, comuns a todos os tipos de SERVIÇO, e campos
específicos, padrões para cada um dos tipos de Serviço.

**Registros de Detalhe** : Um registro de detalhe é composto de um ou mais
segmentos, dependendo do tipo de Serviço.

1. Cabeçalho do Arquivo.

| ID   | Campo                                      | Dê    | Até   | Qnt.  | Decimal | Formato | Padrão | Descrição |
| ---  | ---                                        | ---:  | ---:  | ---:  | ---:  | :---: | ---     | ---     |
| 01.0 | Código da Empresa                          | 1     | 3     | 3     | -     | N     |         | [GNR.001](#GNR.001) |
| 02.0 | Lote de Serviço                            | 4     | 7     | 4     | -     | N     | 0000    | [GNR.002](#GNR.002) |
| 03.0 | Tipo de Registro                           | 8     | 8     | 1     | -     | N     | 0       | [GNR.003](#GNR.003) |
| 04.0 | Uso Exclusivo Netunna                      | 9     | 17    | 9     | -     | A     |         | [GNR.004](#GNR.004) |
| 05.0 | Tipo de Inscrição da Empresa               | 18    | 18    | 1     | -     | N     |         | [GNR.005](#GNR.005) |
| 06.0 | Número de Inscrição da Empresa             | 19    | 32    | 14    | -     | N     |         | [GNR.006](#GNR.006) |
| 07.0 | Nome da Empresa                            | 33    | 72    | 40    | -     | A     |         | [GNR.007](#GNR.007) |
| 08.0 | Nome da Adquirente                         | 73    | 112   | 40    | -     | A     |         | [GNR.008](#GNR.008) |
| 09.0 | Código de Remessa ou de Retorno            | 113   | 113   | 1     | -     | N     |         | [GNR.009](#GNR.009) |
| 10.0 | Data de Geração do Arquivo                 | 114   | 121   | 8     | -     | A     |         | [GNR.010](#GNR.010) |
| 11.0 | Hora de Geração do Arquivo                 | 122   | 127   | 6     | -     | N     |         | [GNR.011](#GNR.011) |
| 12.0 | Número Sequencial do Arquivo (NSA)         | 128   | 134   | 7     | -     | N     |         | [GNR.012](#GNR.012) |
| 13.0 | Número da Versão do Leiaute do Arquivo     | 135   | 139   | 5     | -     | N     |         | [GNR.013](#GNR.013) |
| 14.0 | Uso Reservado para a Empresa               | 140   | 179   | 40    | -     | A     |         | [GNR.014](#GNR.014) |
| 15.0 | Uso Exclusivo Netunna                      | 180   | 300   | 121   | -     | A     |         | [GNR.004](#GNR.004) |

2. Rodapé do Arquivo.

| ID   | Campo                                      | Dê    | Até   | Qnt.  | Decimal | Formato | Padrão | Descrição |
| ---  | ---                                        | ---:  | ---:  | ---:  | ---:  | :---: | ---     | ---     |
| 01.9 | Código da Empresa                          | 1     | 3     | 3     | -     | N     |         | [GNR.001](#GNR.001) |
| 02.9 | Lote de Serviço                            | 4     | 7     | 4     | -     | N     | 9999    | [GNR.002](#GNR.002) |
| 03.9 | Tipo de Registro                           | 8     | 8     | 1     | -     | N     | 9       | [GNR.003](#GNR.003) |
| 04.9 | Uso Exclusivo Netunna                      | 9     | 17    | 9     | -     | A     |         | [GNR.004](#GNR.004) |
| 05.9 | Quantidade de Lotes do Arquivo             | 18    | 23    | 6     | -     | N     |         | [GNR.015](#GNR.015) |
| 06.9 | Quantidade de Registros do Arquivo         | 24    | 29    | 6     | -     | N     |         | [GNR.016](#GNR.016) |
| 07.9 | Uso Exclusivo Netunna                      | 30    | 300   | 271   | -     | A     |         | [GNR.004](#GNR.004) |

2. Segmento V

| ID   | Campo                                      | Dê    | Até   | Qnt.  | Decimal | Formato | Padrão | Descrição |
| ---  | ---                                        | ---:  | ---:  | ---:  | ---:  | :---: | ---     | ---     |
| 01.9 | Código da Empresa                          | 1     | 3     | 3     | -     | N     |         | [GNR.001](#GNR.001) |
| 02.9 | Lote de Serviço                            | 4     | 7     | 4     | -     | N     | 9999    | [GNR.002](#GNR.002) |
| 03.9 | Tipo de Registro                           | 8     | 8     | 1     | -     | N     | 9       | [GNR.003](#GNR.003) |
| 04.9 | Uso Exclusivo Netunna                      | 9     | 17    | 9     | -     | A     |         | [GNR.004](#GNR.004) |
| 05.9 | Quantidade de Lotes do Arquivo             | 18    | 23    | 6     | -     | N     |         | [GNR.015](#GNR.015) |
| 06.9 | Quantidade de Registros do Arquivo         | 24    | 29    | 6     | -     | N     |         | [GNR.016](#GNR.016) |
| 07.9 | Uso Exclusivo Netunna                      | 30    | 300   | 271   | -     | A     |         | [GNR.004](#GNR.004) |

3. Descrição dos campos

| ID   | Nome | Descrição | 
| ---  | ---  | ---  |
| <a id="GNR.001">GNR.001</a> | Código da Empresa | Código que identifica a empresa no TEiACARD. Quando exista um  conjunto de empresas iniciar com código `001` e assim por diante consecutivamente. | 
| <a id="GNR.002">GNR.002</a> | Lote de Serviço | <p>Número sequencial para identificar univocamente um lote de serviço. Criado e controlado pelo responsável pela geração magnética dos dados contidos no arquivo.</p><p>Preencher com `0001` para o primeiro lote do arquivo. Para os demais: número do lote anterior acrescido de 1. O número não poderá ser repetido dentro do arquivo. </p> <p>Se registro for Header do Arquivo preencher com `0000`</p><p>Se registro for Trailer do Arquivo preencher com `9999`</p> | 
| <a id="GNR.012">GNR.012</a> | Número sequencial do arquivo (NSA) | Número sequencial adotado e controlado pelo responsável pela geração do arquivo para ordenar a disposição dos arquivos encaminhados. Evoluir um número sequencial a cada header de arquivo | 
| <a id="GNR.031">GNR.031</a> | Código da Bandeira | <p>Código que identifica a Bandeira do Cartão de Crédito ou de Débito utilizado para a realização da venda.</p><p>Ver [Tabela I](#TabelaI).</p>  | 


4. <a id="TabelaI">Tabela I - Bandeiras</a>

| ID   | Nome | 
| ---:  | ---  |
| 001 | VISA | 
| 002 | MASTERCARD | 
| 003 | AMERICAN EXPRESS | 
| 004 | HIPERCARD | 
| 005 | DINERS | 
| 006 | ELO | 
| 007 | AGIPLAN | 
| 008 | BANESCARD | 
| 009 | CABAL | 
| 010 | CREDSYSTEM | 
| 011 | ESPLANADA | 
| 012 | CREDZ | 
| 013 | SOROCRED | 
| 014 | HIPER | 
| 015 | DISCOVER | 
| 016 | AURORA | 
| 017 | COOPERCRED | 
| 018 | SICRED | 
| 019 | AVISTA | 
| 020 | MAIS! | 
| 021 | UNIONPAY | 
| 022 | ALELO | 
| 023 | GOODCARD | 
| 024 | JCB | 
| 025 | SODEXO | 
| 026 | BONUS CBA | 
| 027 | SAPORE | 
| 028 | POLICARD | 
| 029 | VEROCHEQUE | 
| 030 | GREENCARD | 
| 031 | VALECARD | 

