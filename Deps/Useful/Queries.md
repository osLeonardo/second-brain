#### Hisórico de Consultas CPF
> SELECT data_cadastro, documento, situacao, razao_social, versao_mix
> FROM public.historico_consultas
> WHERE CHAR_LENGTH(documento) = 11;

#### Hisórico de Consultas CNPJ
> SELECT data_cadastro, documento, situacao, razao_social, versao_mix
> FROM public.historico_consultas
> WHERE CHAR_LENGTH(documento) = 14;