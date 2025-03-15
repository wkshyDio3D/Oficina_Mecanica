# Oficina_Mecanica
Desafio db_oficina Mecanica Baseado no modelo Do diagrama.


-- Entrega de desafio oficina DIO ---

CREATE TABLE Clientes (
  idCliente INT AUTO_INCREMENT primary key,
  C_FNome VARCHAR(15),
  C_MNome VARCHAR(10),
  C_LNome VARCHAR(20),
  Cpf_Cnpj char(15),
  Data_Naicimento DATE,
  Endereco VARCHAR(45),
  Referencia VARCHAR(45),
  Bairro VARCHAR(45),
  Cidade VARCHAR(45),
  Cep CHAR(10),
  Fone char(11),
  E_mail VARCHAR(45),
  constraint unique_cpf_cnpj_cliente unique (cpf_cnpj)
  );
    alter table clientes auto_increment=1;
-- ---------------------------------------------------------------------------------------------
insert into clientes values (0,'luiza',   'W','vailatt',3682358000,'1984-03-26','voss-houston-TX 3667','Prox Max', 'Nyw York', 'Cidade das Flouer', 228766564, 96456719, 'luiWvai@ofimec.com'); 
                    
insert into clientes values (0,'Scarlet',  'S','chase',3682358001,'1984-03-26','voss-houston-TX 3667','Prox Max', 'Nyw York', 'Cidade das Flouer', 228766564, 975643567, 'ScarSCha@ofimec.com');
insert into clientes values (0,'carol',  'O','Pimenta',6533467577,'1996-03-16','Av-houston-TX 767',' Farm ', 'Center', 'Texas', 22275764, 947562465, 'CarOPim@ofimec.com'); 
insert into clientes values (0, 'Flanklin','S', 'Wong',0049753578, '1976-07-17', '631-Fondren-Spring-TX', 'Prox fax', 'Carangola', 'Cidade das Flores', 22854365, 956743755, 'FlaSWon@ofimec.com');
insert into clientes values (0, 'Alicia','J','Zelaia',368748368,'1994-03-26','731-voss-houston-TX', 'Prox fax', 'Carangola', 'Cidade das Flores', 22854365, 957632746, 'AliJZel@ofimec.com'),
							(0, 'Jenifer','T','cox',286369427,'1927-08-01','7831-Ricen-york-TX', 'Prox fax', 'Carangola', 'Cidade das Flores', 22854365, 974274591, 'JenTCox@ofimec.com'),
							(0, 'Ramesh','H','Jabbar',146858959,'1958-01-12','331-Fondren-houston-TX', 'Prox fax', 'Carangola', 'Cidade das Flores', 22854365, 925381638, 'RamHJab@ofimec.com'),
							(0, 'Joyce','K','Smith',135457954,'1932-09-28','7731-Dallas-miame-TX', 'Prox fax', 'Carangola', 'Cidade das Flores', 22854365, 997416542, 'JoykSmi@ofimec.com'),
							(0, 'Pier','R','Wallace',123582589,'1928-02-15','7391-Fondren-houston-TX', 'Prox fax', 'Carangola', 'Cidade das Flores', 22854365, 986417559, 'PirRWal@ofimec.com'),
							(0, 'ahmad','B','Smith',934656789,'1958-07-27','431-texas-fire-TX', 'Prox fax', 'Carangola', 'Cidade das Flores', 22854365, 973662515, 'AhmBSmi@ofimec.com'),
							(0, 'james','N','Borg',123459369,'1928-03-13','8731-stone-houston-TX', 'Prox fax', 'Carangola', 'Cidade das Flores', 22854365, 914636389, 'JamNBor@ofimec.com');                
  
-- ---------------------------------------------------------------------------------------------
  create table EquipeMecanicos(
  idMecanico INT AUTO_INCREMENT primary key,
  M_FNome VARCHAR(15),
  M_MNome VARCHAR(10),
  M_LNome VARCHAR(15),
  Cpf_Cnpj char(18),
  Data_Naicimento DATE,
  Endereco VARCHAR(45),
  Referencia VARCHAR(45),
  Bairro VARCHAR(45),
  Cidade VARCHAR(45),
  Cep CHAR(10),
  Fone char(15),
  E_mail VARCHAR(45),
  Especialidade VARCHAR(45),
  constraint unique_cpf_cnpj_Mecanico unique (cpf_cnpj)
  );
 alter table EquipeMecanicos auto_increment=1;

-- ---------------------------------------------------------------------------------------------
insert into EquipeMecanicos values (0,  'Manoell',   'W', 'Vladmir', 3875493756,    '1975-08-23', 'Rua dos Mec-TX 465', 'Prox padaria', 'Nyw York', 'Maritinga', 7465326585, 376547383, 'ManWVla@ofimec.com', 'Mecanico'); 
insert into EquipeMecanicos values (0,  'Carlos',   'Y', 'Sonza', 8347452734,    '185-06-17', 'Av do Chock-TX 465', 'Farmacia', 'Myame', 'qualquer', 7364878445, 784635477, 'CarYSon@ofimec.com', 'Eletricista');    insert into EquipeMecanicos values (0,  'Josuel',   'B', 'Gomes', 345757866,    '2001-04-26', 'Rua Funil-TX 465', 'shoping', 'Sntos', 'hdhdhjj', 36859649, 54728437464, 'JosBGom@ofimec.com', 'Funileiro'); 
insert into EquipeMecanicos values (0,  'Antonio',   'A', 'Esperanza', 576375885,    '1986-01-15', 'Travessa Das Tintas-TX 465', 'Bootafogo', 'Nyw York', 'Maritinga', 254754754, 57362357, 'AntAEsp@ofimec.com', 'Pintor'); 
insert into EquipeMecanicos values (0,  'Pedro',   'U', 'Vostre', 3876746574,    '1975-12-27', 'Rua da borracha-TX 465', 'Chaveiro', 'Olaria', 'myame', 4647848536, 466474843, 'PedUVos@ofimec.com', 'Borracheiro'); 
insert into EquipeMecanicos values (0,  'Kaleo',   'P', 'Michall', 84467474878,    '1975-09-25', 'Beco suisa-TX 465', 'Mercado', 'copa', 'rio', 312453636, 8546546674, 'KalPMic@ofimec.com', 'Mecanico'); 
 
-- ---------------------------------------------------------------------------------------------

CREATE TABLE TipoServico(
  IdTipoServico INT AUTO_INCREMENT primary key,
   id_Cliente int,
  Status_Serviço enum('Concerto','Manutencao', 'Revisao', 'Pintura', 'Eletrica', 'Hidraulica', 'Pneus', 'Funilaria', 'Nao Definido' ) DEFAULT 'Nao Definido'
  );

  -- ---------------------------------------------------------------------------------------------
	insert into TipoServico values (  0,  10,    'Eletrica' );
	insert into TipoServico values (  0,  8,    'Revisao' );
	insert into TipoServico values (  0,  6,   'Pneus' );
	insert into TipoServico values (  0,  4,  'Concerto' ); 
    insert into TipoServico values (  0,  2,   'Nao Definido' );

-- ---------------------------------------------------------------------------------------------

  CREATE TABLE VeiculoClientes (
	idVeiculo INT AUTO_INCREMENT primary key,
    idCliente int, 
    C_Nnome VARCHAR(15),
	marca varchar(20) not null,
	Modelo varchar(20) not null,
	Ano DATE,
	Placa varchar (10) not null unique
    );
    
    insert into VeiculoClientes values (0);
    
 -- ---------------------------------------------------------------------------------------------
 insert into VeiculoClientes values (0, 1,    'luiza',  'Fort',  'ExtremeX',     '2013-08-01',   'xml325x3');
 insert into VeiculoClientes values (0, 2,   'Scarlet', 'Fiax',     'Strad',     '2017-06-21',   'dgy345hj'),
									(0,  4,   'Flanklin', 'BnW',    '4p4',     '2014-04-26',   'xef764bh'),
									(0,  6,  'Jenifer',  'Gypy',  'maxPower',     '2011-08-21',   'hgd984nh'),
									(0,   8,  'Joyce',    'MdM',   'rx1',   '2018-03-17',   'udj478gn');
 insert into VeiculoClientes values (0, 10,  'ahmad', 'Ranger',  'Extreme X3',     '2023-05-11',   'a3x696xor');                                    
 

-- ---------------------------------------------------------------------------------------------

    create table OS_OrdemServico(
    idOS_OrdemServiço INT AUTO_INCREMENT primary key,
    idAvaliacao_Serviço INT,
    Numero_OS char(5),
    Emissão Date,
    Seviço_Executado varchar(45),
    Valor_Peças DECIMAL(10,2),  -- 10 digitos no total,sendo 2 digitos apos a virgula.
    Valor_MaoObra DECIMAL(10,2),
    Custo_Total DECIMAL(10,2),
    idTabela_peças_MaoObra  INT,
    Status_Serviço enum('Em Processamento','Nao Aprovado', 'Iniciado', 'Em Andamento', 'Finalizado' ) DEFAULT 'Em Processamento',
    Conclusão Date
    );
   
   -- ---------------------------------------------------------------------------------------------
insert into OS_OrdemServico values (   0,   0,   123, '2024-09-13',  'pintura',      450.00,       2500.00,     3040.00,    null,   'Finalizado', '2024-09-18' );
insert into OS_OrdemServico values (  0,   1,   126, '2024-09-14',  'eletrica',      550.00,       1500.00,     2050.00,   null,   'Finalizado', '2024-09-19' ),
								   (  0,  2,  129, '2024-09-15',  'pneus',      1250.00,       1700.00,     2950.00,   null,   'Em Processamento', '2024-09-20' ),
								   (  0,   3,  132, '2024-09-16',  'Funilaria',      750.00,       2500.00,     3250.00,    null,   'Em Andamento', '2024-09-21' ),
								   (   0,  4,  135, '2024-09-17',  'pintura',      650.00,       2500.00,     3150.00,   null,   'Nao Aprovado', '2024-09-22' );
  
-- ---------------------------------------------------------------------------------------------
   
  CREATE TABLE Avaliação_Execução_Serviço(
  idAvaliação_Serviço INT AUTO_INCREMENT primary key,
  idVeiculo INT,
  Mecanica VARCHAR(45),
  Eletrica VARCHAR(45),
  Hidraulica VARCHAR(45),
  Refrigeracao VARCHAR(45),
  Pintura VARCHAR(45),
  Funilaria VARCHAR(45),
  Troca_Pneus VARCHAR(45),
  Balanceamento VARCHAR(45),
  Cambagem VARCHAR(45),
  Lubrificacao VARCHAR(45),
  Troca_oleo VARCHAR(45)
  );
 
-- ---------------------------------------------------------------------------------------------
select * from Avaliação_Execução_Serviço;	# idAvaliação_Serviço, idVeiculo,   Mecanica,     Eletrica, Hidraulica, Refrigeracao, Pintura, Funilaria, Troca_Pneus, Balanceamento, Cambagem, Lubrificacao, Troca_oleo
insert into Avaliação_Execução_Serviço values (      0,                1,     'Finalizada',               null,           null,         null,    'Em Execusao',      null,      'Pneus Trocados',          'Bal Finalizada',     null,        null,     'Olheo Trocado');

insert into Avaliação_Execução_Serviço values (      0,                2,       'Execucao', 'Elet.Finalizada' ,       'HidraConcertada',         'Troca de Gas',    'Em Execusao',      'Finalizada',     'Em Execusao',          'Bal Executada',     'Camb. Filalizada',        'Lub Finalizada',     'Olheo Trocado');
insert into Avaliação_Execução_Serviço values (      0,                3,     'Finalizada',        'HidraConcertada,       ',         null,    'Em Execusao',      null,      'Pneus Trocados',          'Bal em Execucao',     null,        null,     'Olheo Trocado');

insert into Avaliação_Execução_Serviço values (      0,                4,       'Iniciada',               null,       'Hidr. Iniciada',         null,    'Em Execusao',      null,      null,          'Bal Iniciada',     null,        null,     'Olheo Trocado');
insert into Avaliação_Execução_Serviço values (      0,                5,     'Finalizada',               null,       'HidraConcertada',         null,    'Em Execusao',      null,      'Pneus Trocados',          'Cambagen Executada',     null,        null,     'Olheo Trocado');

-- ---------------------------------------------------------------------------------------------

  create table Tabela_Peças_MaoObra(
    idTabela_Peças_MaoObra INT AUTO_INCREMENT primary key,
    idCliente int,
    idVeiculo INT,
    idMecanico int,
    PeçasUtilizadas VARCHAR(255),
    NomeMecanico VARCHAR(45),
    OS_Ordem_Serviço_idOS_Ordem_Serviço INT,
    OS_Ordem_Serviço_Avaliacao_Serviço_idAvaliação_Serviço INT,
    OS_Ordem_Serviço_Tabela_Peças_MaoObra_idTabela_Peças_MaoObra INT
  );

-- ---------------------------------------------------------------------------------------------
insert into Tabela_Peças_MaoObra values (   0,    6,   2,  1, 'motor de arranque', 'Carlos',  3,  1,  null);
insert into Tabela_Peças_MaoObra values (   0,    5,   5,  1, 'pneus',     'Pedro',   3,  1,  null);
insert into Tabela_Peças_MaoObra values (  0,    3,  4,  1, 'Tintas',    'josuel',   2,  1,  null);
insert into Tabela_Peças_MaoObra values (  0,  2,   2,  1, 'Pecas cambagem',    'Pedro',    5,  1,  null);
insert into Tabela_Peças_MaoObra values (  0,  1,  2,  1, 'Bateria ',    'Carlos',   1,  1,  null);


-- ---------------------------------------------------------------------------------------------

  create table Equipe_Serviço(
    idEquipe_Serviço INT AUTO_INCREMENT primary key,
    idMecanico int,
    idVeiculo INT,
    Nome_Mecanico VARCHAR(45),
    Endereço_mecanco VARCHAR(45),
    Especialidade VARCHAR(45),
    Avaliação_Execução_Serviço_idAvaliação_Serviço int
  );
 
-- ---------------------------------------------------------------------------------------------
insert into Equipe_Serviço values (0, 3, 2, 'Manoell',  'Rua dos Mec-TX 465','mecanico', 5  );

insert into Equipe_Serviço values (0, 6, 3, 'carlos',  'Av do Chock-TX 465','Eletricista', 8  );
insert into Equipe_Serviço values (0, 7, 4, 'Antonio',  'Travessa Das Tintas','Pintor', 7  );
insert into Equipe_Serviço values (0, 8, 5, 'Pedro',  'Rua da borracha-TX 465','Borracheiro', 9  );
insert into Equipe_Serviço values (0, 10, 6, 'Josuel',  'Beco suisa-TX 465','mecanico', 3  );
      

-- ---------------------------------------------------------------------------------------------

  create table Pagamentos(
    idPagamento int primary key,
    Custo_Total DECIMAL(10,2),
    TipoPagamento  enum('Pix', 'Boleto', 'Dinheiro', 'Cartao Debito','Cartao Credito', 'Dois Cartoes'),
    Pix varchar(255),
    Data_Validade Date,
    limit_Available float,
    Cliente_idCliente int, 
    Cliente_Avaliação_Serviço_idAvaliacao_Serviço int,
    Avaliação_Execução_Serviço_idAvaliação_Serviço INT
    );

-- ---------------------------------------------------------------------------------------------
insert into Pagamentos values ( 0,     3050.68,            'Pix', 'luiWvai@ofimec.com',          null,    null,     1,    null,    null );
  
insert into Pagamentos values ( 2,     3050.68,            'Pix', 'CarOPim@ofimec.com',          null,    null,     2,    null,    null );  
insert into Pagamentos values ( 3,     3050.68,         'Boleto',                 null,  '2025-03-10',    null,     5,    null,    null );  
insert into Pagamentos values ( 4,     3050.68,       'Dinheiro',                 null,          null,    null,     7,    null,    null );
insert into Pagamentos values ( 5,     3050.68,  'Cartao Debito',                 null,          null,    null,     9,    null,    null );
insert into Pagamentos values ( 5,     3050.68, 'Cartao Credito',                 null,          null,    null,     9,    null,    null );
insert into Pagamentos values ( 7,     3050.68, 'Cartao Credito',                 null,          null,    null,     3,    null,    null );
  
-- ---------------------------------------------------------------------------------------------

    create table CardPayments(
	Id_Cartao int auto_increment primary key,
        id_Cliente int,
        CardName varchar(20),
        CardNumbers char(16),
        CardDate DATE,
        validKey char(3)
	);
    -- --------------------------------------------------------------------------------------------
    insert into CardPayments values  (0,          9,   'Pier Wallace', 375898753475,  '2025-12-28', 369 );
insert into CardPayments values  (0,          2,  'Scarlet chase', 476321856368,  '2025-08-28', 596 );
insert into CardPayments values  (0,          3,  'carol Pimenta', 592768327593,  '2025-05-28', 328 );
    
    -- --------------------------------------------------------------------------------------------
-- conjunto de consultas SQL que atendem aos requisitos:

-- Recuperação simples com SELECT sql
SELECT * FROM Clientes;

-- Filtro com WHERE 

SELECT * FROM Clientes WHERE Cidade = 'Cidade das Flores';

-- Criação de expressões para gerar atributos derivados
-- Exemplo: Calcular a idade dos clientes com base na data de nascimento.

SELECT idCliente, C_Nnome, C_Snome, 
       TIMESTAMPDIFF(YEAR, Data_Naicimento, CURDATE()) AS Idade 
FROM Clientes;

-- Ordenação dos dados com ORDER BY

SELECT * FROM Clientes ORDER BY C_Nnome ASC;


-- Condição dos filtros aos grupos com HAVING
-- Exemplo: Quantidade de clientes por cidade, filtrando as cidades que têm mais de 2 clientes.

SELECT Cidade, COUNT(*) AS TotalClientes 
FROM Clientes 
GROUP BY Cidade 
HAVING COUNT(*) > 2;


-- Junção entre tabelas (JOIN) para fornecer perspectivas mais complexas
-- Exemplo: Exibir informações do cliente e do veículo associado.

SELECT c.idCliente, c.C_Nnome, v.marca, v.Modelo, v.Ano, v.Placa
FROM Clientes c
JOIN VeiculoClientes v ON c.idCliente = v.idCliente;
