# doc


### REGISTRO HEADER DE ARQUIVO

Cabeçalho do Arquivo.

| ID   | Campo                                      | Dê    | Até   | Tam   | Decimal | Formato | Padrão | Descrição |
| ---  | ---                                        | ---:  | ---:  | ---:  | ---   | ---   | ---     | ---     |
| 01.0 | Código da Empresa                          | 1     | 3     | 3     | -     | N     |         | GNR.001 |
| 02.0 | Lote de Serviço                            | 4     | 7     | 4     | -     | N     | 0000    | GNR.002 |
| 03.0 | Tipo de Registro                           | 8     | 8     | 1     | -     | N     | 0       | GNR.003 |
| 04.0 | Uso Exclusivo Netunna                      | 9     | 17    | 9     | -     | A     | Brancos | GNR.004 |
| 05.0 | Tipo de Inscrição da Empresa               | 18    | 18    | 1     | -     | N     |         | GNR.005 |
| 06.0 | Número de Inscrição da Empresa             | 19    | 32    | 14    | -     | N     |         | GNR.006 |
| 07.0 | Nome da Empresa                            | 33    | 72    | 40    | -     | A     |         | GNR.007 |
| 08.0 | Nome da Adquirente                         | 73    | 112   | 40    | -     | A     |         | GNR.008 |
| 09.0 | Código de Remessa ou de Retorno            | 113   | 113   | 1     | -     | N     |         | GNR.009 |
| 10.0 | Data de Geração do Arquivo                 | 114   | 121   | 8     | -     | A     |         | GNR.010 |
| 11.0 | Hora de Geração do Arquivo                 | 122   | 127   | 6     | -     | N     |         | GNR.011 |
| 12.0 | Número Sequencial do Arquivo (NSA)         | 128   | 134   | 7     | -     | N     |         | GNR.012 |
| 13.0 | Número da Versão do Leiaute do Arquivo     | 135   | 139   | 5     | -     | N     |         | GNR.013 |
| 14.0 | Uso Reservado para a Empresa               | 140   | 179   | 40    | -     | A     |         | GNR.014 |
| 15.0 | Uso Exclusivo Netunna                      | 180   | 300   | 121   | -     | A     | Brancos | GNR.004 |

Cabeçalho do Lote.

| ID   | Campo                                      | Dê    | Até   | Tam   | Decimal | Formato | Padrão | Descrição |
| ---  | ---                                        | ---:  | ---:  | ---:  | ---   | ---   | ---     | ---     |
| 01.0 | Código da Empresa                          | 1     | 3     | 3     | -     | N     |         | GNR.001 |
| 02.0 | Lote de Serviço                            | 4     | 7     | 4     | -     | N     | 0000    | GNR.002 |
| 03.0 | Tipo de Registro                           | 8     | 8     | 1     | -     | N     | 0       | GNR.003 |
| 04.0 | Uso Exclusivo Netunna                      | 9     | 17    | 9     | -     | A     | Brancos | GNR.004 |
| 05.0 | Tipo de Inscrição da Empresa               | 18    | 18    | 1     | -     | N     |         | GNR.005 |
| 06.0 | Número de Inscrição da Empresa             | 19    | 32    | 14    | -     | N     |         | GNR.006 |
| 07.0 | Nome da Empresa                            | 33    | 72    | 40    | -     | A     |         | GNR.007 |
| 08.0 | Nome da Adquirente                         | 73    | 112   | 40    | -     | A     |         | GNR.008 |
| 09.0 | Código de Remessa ou de Retorno            | 113   | 113   | 1     | -     | N     |         | GNR.009 |
| 10.0 | Data de Geração do Arquivo                 | 114   | 121   | 8     | -     | A     |         | GNR.010 |
| 11.0 | Hora de Geração do Arquivo                 | 122   | 127   | 6     | -     | N     |         | GNR.011 |
| 12.0 | Número Sequencial do Arquivo (NSA)         | 128   | 134   | 7     | -     | N     |         | GNR.012 |
| 13.0 | Número da Versão do Leiaute do Arquivo     | 135   | 139   | 5     | -     | N     |         | GNR.013 |
| 14.0 | Uso Reservado para a Empresa               | 140   | 179   | 40    | -     | A     |         | GNR.014 |
| 15.0 | Uso Exclusivo Netunna                      | 180   | 300   | 121   | -     | A     | Brancos | GNR.004 |
