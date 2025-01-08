Projeto Modelagem do zero- Narrativa encontra-se dentro de uma prestação de serviço em uma Oficina Mecânica.

A partir da Descrição solicitada temos:

Clientes levam seus veículos para conserto ou revisão.
Cada veículo é atendido por uma equipe de mecânicos, que:
Identifica os serviços necessários.
Preenche a OS com a data de entrega e o valor total.
O valor da OS é composto por:
Serviços, cujo custo é calculado a partir de uma tabela de mão de obra.
Peças, cujos valores são adicionados à OS.
Após autorização do cliente, os serviços são executados pela mesma equipe que os avaliou.
Mecânicos possuem dados como nome, endereço, especialidade e código de identificação.
A OS possui número, data de emissão, valor, status e data de conclusão.

Metodologia:
Todos os atributos foram criados segundo a descrição, para fazer o link dos relacionametos, segui alguns pontos:
Um Cliente pode ter mais de um veiculo, e este veiculo poder ser um carro, moto etc.. então temos um intância pra veiculos.
Em seguida foi relacionado um veiculo com a equipe mecânica, onde cada veiculo pode estar somente com uma equipe mecânica.
A equipe mecânica e formada por varios mecânicos, assim gerando nossa equipe que faz um solicitação de uma OS, nessa parte em questão
tive uma pequena duvida em questão de "Uma equipe mecânica seria ideial fazer mais de uma ordem de serviço, já que a ordem de serviço possui mais de um serviço em OS?"
então ficou como se a equipe pudesse fazer mais de um OS para o veiculo mesmo com esta questão. Como já mencionado a OS possui um ou mais tipo de serviço
onde foi criado uma instancia para isso, isso igualmente para peças, podemos ter quantas peças quiser solicitada pelo equipe, oque gera um relacionamento de solicitação de peças
quantidade e o valor total das peças solicitadas.

Modelo Relacional

Cliente (1:N) Veículo: Um cliente pode possuir vários veículos.
Veículo (1:1) Equipe mecânica: Um Veículo e apenas direcionada a um equipe mecânica.
Equipe de Mecânico (1:N) Ordem de Serviço: A equipe de mecânicos pode solicitar mais de uma OS.
Equipe de Mecânico (1:N) mecânicos: A equipe mecânica e formada por mais de um mecânico.
Ordem de Serviço (N:M) Peças: Uma OS pode estar relacionada com mais de um peça, e um peça pode estar em mais de uma OS.
Ordem de Serviço (N:M) Serviço:Uma OS pode conter mais de um tipo de serviço, e um serviço pode estar em mais de uma OS.
