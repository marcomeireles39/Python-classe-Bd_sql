# Python classe Bd_sql

__Classe para criar e manipular banco de dados sqlite__

Como usar:

Primeiro você importa a classe

    from Bd import Bd_sql

Depois crie o objeto

    obj_ini = Bd_sql(nome banco de dados' , 'nome da tabela')

Insere o indice inclua no metodo para criar o banco de dados

    obj_ini.Criar_bd(indice)

Agora inserir os dados na tabela

    obj_ini.Incluir_dados(dados)

Caso você queira modificar algum dado usa-se o codigo abaixo

    obj_ini.Modificar(ca_valor, condicao)

Ou apagar um ou varios valores

    obj_ini.Apaga(condicao)

Ou mostrar o conteúdo do banco de dados

    obj_ini.Mostrar()

Ou se preferir criar sua propria pesquisa, ter maior autonomia

    obj_ini.Sql_Command()

Caso queiram apagar alguma tabela usar o codigo

    obj_ini.Apaga_Tabela(tabela):


Abaixo temos um exemplo de utilização da classe , no exemplo temos a criação da criação
do banco de dados, da tabela bem como modificacao e exclusão da tabela

    from Bd import Bd_sql

    nomebd = "banco_de_dados.db"
    nometabela = "pessoas"

    indice = "nome text, idade integer, telefone text, ecivil text"
    dados = "'Fulano de tal',39,'9999-9999','Solteiro'"

    obj_ini = Bd_sql(nomebd, nometabela)
    obj_ini.Criar_bd(indice)
    obj_ini.Incluir_dados(dados)

    obj_ini.Mostrar()

    obj_ini.Modificar('idade = 39', "ecivil = 'Solteiro'")

    obj_ini.Mostrar()

    obj_ini.Apaga('idade = 39')

    obj_ini.Mostrar()

    obj_ini.Apaga_Tabela(nometabela)
