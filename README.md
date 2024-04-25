# PowerBI-DIO-Desafio-2
Repositorio do DESAFIO 2 do Curso de PowerBi da DIO

# Foram realizados ajustes nos Scripts de cração do Schema e carga dos dados no Azure MySQL
# AJUSTES DOS SCRIPTS: 
Havia FK invertida de employee com department. O modelo checava se a department existia no employee e não o contrario
- foreign key (Mgr_ssn) references employee(Ssn)

Tive retirar dois valores de duas colunas da tabela de employee passando para null devido a auto relacionamento sem referencia (Super_ss)
- insert into employee values ('Jennifer', 'S', 'Wallace', 987654321, '1941-06-20', '291-Berry-Bellaire-TX', 'F', 43000, NULL, 4);
- insert into employee values ('Franklin', 'T', 'Wong', 333445555, '1955-12-08', '638-Voss-Houston-TX', 'M', 40000, NULL, 5),

Tive que retirar esse registro da tabela Works_on pois ele tinha FK e não ligava a ninguem (EMPLOYEE)
- (888665555, 20, 0.0);

# Resolucao do desafio no arquivo DOC anexo com prints
Obs. Usei o padrão de duplicar as consultas a Cada transforação significativa dos dados, para preservar a resolução de cada item proposto
