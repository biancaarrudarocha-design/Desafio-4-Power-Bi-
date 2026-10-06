# Desafio-4-Power-Bi-
Desafio 4 Power Bi dio.me 

Estrutura Visual do Esquema em Estrela
                     +-----------------------+
                     |    Dim_Professor      |
                     +-----------------------+
                     | SK_Professor (PK)     |
                     | idProfessor           |
                     | Nome_Professor        |
                     | Estatuto_Coordenador  |
                     +-----------+-----------+
                                 |
                                 |
+-----------------------+        |        +-----------------------+
|    Dim_Disciplina     |        |        |      Dim_Curso        |
+-----------------------+        |        +-----------------------+
| SK_Disciplina (PK)    |        |        | SK_Curso (PK)         |
| idDisciplina          |        |        | idCurso               |
| Nome_Disciplina       |        |        | Nome_Curso            |
| Pre_Requisitos        |        |        +-----------+-----------+
+-----------+-----------+        |                    |
            |                    |                    |
            |        +-----------v-----------+        |
            +------->| Fato_Ministracao_Ensino |<------+
                     +-----------------------+
                     | SK_Professor (FK)     |
                     | SK_Disciplina (FK)    |
                     | SK_Curso (FK)         |
                     | SK_Departamento (FK)  |
                     | SK_Data (FK)          |
                     |-----------------------|
                     | Carga_Horaria         |
                     | Quantidade_Disciplinas|
                     | Quantidade_Turmas     |
                     +-----------^-----------+
                                 |
                                 |
+-----------------------+        |        +-----------------------+
|    Dim_Departamento   |        |        |       Dim_Data        |
+-----------------------+        |        +-----------------------+
| SK_Departamento (PK)  |        |        | SK_Data (PK)          |
| idDepartamento        |        |        | Data_Completa         |
| Nome_Departamento     |<-------+------->| Ano / Semestre / Mês  |
| Campus                |                 +-----------------------+
+-----------------------+

