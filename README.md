# Gerenciamento Escolar

Este é um pequeno projeto de demonstração de um sistema de gerenciamento escolar. Ele permite gerenciar alunos, professores, matérias, horários e muito mais. Abaixo, você encontrará instruções claras sobre como usar o programa.

## O que o aplicativo faz?

- **Gerencia alunos**: Controla faltas, presenças e notas.
- **Gerencia professores**: Organiza horários e disponibilidades.
- **Análise de dados**: Gera relatórios e análises sobre o desempenho escolar.

## Como usar o programa

### Classes

Para adicionar alunos, é necessário criar **classes**. As classes devem seguir um formato específico:

- **Formato**: Uma letra seguida de um número (ex: A1, B2).
- **Exemplo**: A1, B2, C3.

**Observação**: Não importa se você digita em maiúsculas ou minúsculas, o sistema sempre salvará em maiúsculas.

#### Exemplo de Formulário para Adicionar Classes:

| Nome da Classe |
|----------------|
| A1             |
| B2             |

**Para deletar uma classe**: Basta clicar na classe que deseja remover e apertar em "Deletar".

---

### Matérias

Para adicionar matérias:

- **Regras**: Apenas caracteres são permitidos. Números e símbolos (como @, _) não são aceitos.E priorize não colocar ~ ç ^ ` , pois isso pode dificultar ou gerar bugs

#### Exemplo de Formulário para Adicionar Matérias:

| Nome do Curso | ID do Curso |
|---------------|-------------|
| Geografia     | 1           |
| Matematica    | 2           |

---

### Professores

Para adicionar professores:

- **Requisito**: É necessário que as matérias já estejam cadastradas para que o professor possa ser associado a uma área de atuação.
- **Turnos**: O professor pode ser responsável por um ou mais turnos (Manhã, Tarde, Noite) ou ser classificado como "Indeterminado" ou "Nenhum".

#### Opções de Turno:

1. Manhã
2. Tarde
3. Noite
4. Indeterminado
5. Nenhum

**Observação**: Apenas professores de turnos específicos podem lançar notas para suas turmas. Professores com turno "Indeterminado" têm acesso a todas as turmas, mas só podem lançar notas relacionadas à sua matéria.

#### Exemplo de Tabela de Professores:

| ID do Professor | Nome           | CPF           | Matéria     | Número        | Email           | Empregado | Responsável pela Classe | Turno Responsável |
|-----------------|----------------|---------------|-------------|---------------|-----------------|-----------|-------------------------|-------------------|
| 1               | João da Silva  | 123.456.789-00| Matemática  | (11) 99999-9999| joao@email.com  | ✅         | A5                      | Manhã             |
| 2               | Maria Oliveira | 987.654.321-00| Português   | (21) 88888-8888| maria@email.com | ❌         | B6                      | Tarde             |

**Filtros**: Você pode filtrar professores por turno e status de emprego (empregado ou não).

**Para deletar um professor**: Ao deletar um professor, todos os horários associados a ele também serão removidos.

---

### Horários/Aulas

Você pode lançar horários de aulas para cada turma. Cada horário é associado a um turno, classe e data específica.

#### Exemplo de Tabela de Horários:

| id_horario | Turno | Inicia às | Termina às | Data       | Classe |
|------------|-------|-----------|------------|------------|--------|
| 1          | Manhã | 08:00     | 10:00      | 2024-10-27 | A1     |
| 2          | Tarde | 14:00     | 16:00      | 2024-10-27 | B4     |
| 3          | Noite | 19:00     | 21:00      | 2024-10-28 | C5     |

**Observação**: Professores podem ter horários para várias classes, mas só podem lançar notas para suas próprias matérias.

**Para deletar ou editar horários**: Basta selecionar o horário e clicar em "Deletar" ou "Editar".

---

### Alunos

Cada aluno é associado a uma classe e turno. O número de chamada é único para cada turma e turno.

#### Exemplo de Tabela de Alunos:

| id_aluno | Nome           | Dependência | Classe | Turno | Número de Chamada |
|----------|----------------|-------------|--------|-------|-------------------|
| 1        | Ana Silva      | ✅          | A6     | Manhã | 1                 |
| 2        | Bruno Oliveira | ✅          | A2     | Tarde | 2                 |
| 3        | Carla Rodrigues| ❌          | B4     | Manhã | 3                 |

**Para deletar um aluno**: Ao deletar um aluno, o número de chamada dos demais alunos da mesma turma e turno será atualizado.

**Detalhes do aluno**: Você pode ver quantas aulas o aluno faltou ou compareceu, e filtrar por mês ou matéria.

---

### Impressão

A funcionalidade de impressão permite gerar PDFs das tabelas. No entanto, é limitada e pode apresentar bugs se muitas colunas forem selecionadas.

#### Passos para imprimir:

1. Selecione as colunas que deseja imprimir.
2. Escolha o estilo e tamanho da fonte.
3. Defina o nome do arquivo PDF.
4. Clique em "Imprimir".

O arquivo será salvo em: `file:///C:/Users/NOME_USÚARIO/OneDrive/Documents/documento.pdf`.

**Para cancelar**: Basta clicar em "Cancelar" e você voltará à tela anterior.

---

## Observações Finais

- **Bugs conhecidos**: 
  - Ao mudar um aluno de turma ou turno, o número de chamada pode ser reiniciado.
  - A funcionalidade de impressão pode apresentar problemas com muitas colunas.
  - Ao fazer check-in de presença, valores podem ser duplicados se o processo for repetido.

Este projeto é uma demonstração e pode conter bugs. Sinta-se à vontade para contribuir ou reportar problemas!
OBS:ELE FUNCIONA LIVREMENTE NO VS CODE 2022 MAS APENAS COM A INSTALAÇÃO APRESENTA PROBLEMAS NÃO PRESENTES COMPILAÇÃO DE CÓDIGO,CONTÉM BUGS EM PARTE POR CONTA DISSO


**Uso livre**.
