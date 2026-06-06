# TrabalhoEDVERSIONFINAL Sistema de Contratação de Docente

Sistema desenvolvido com JavaFX para gerenciar o processo de contratação temporária de docentes em uma faculdade.

---

## 📌 Funcionalidades

### 🔧 CRUD Completo
- **Cursos**: Cadastrar, buscar, atualizar e remover cursos  
- **Disciplinas**: Gerenciar disciplinas vinculadas a cursos  
- **Professores**: Cadastrar professores com pontuação  
- **Inscrições**: Gerenciar inscrições em processos seletivos  

### 🔍 Consultas Especiais
- **Consulta de Inscritos**: Lista professores inscritos em uma disciplina, ordenados por pontuação (QuickSort)  
- **Processos Abertos**: Exibe todas as disciplinas com processos abertos usando HashTable  

---

## 📁 Estrutura do Projeto

```text
/contratacao-docente
├── csv/
│   ├── disciplinas.csv
│   ├── cursos.csv
│   ├── professores.csv
│   └── inscricoes.csv
│
├── doc/
│   └── diagrama.png
│
├── lib/
│   ├── Lista.Java
│   ├── ListaSimples.Java
│   └── HashTable.Java
│
├── src/
│   ├── application/
│   │   └── MainApp.java
│   │
│   ├── controller/
│   │   ├── CursoController.java
│   │   ├── DisciplinaController.java
│   │   ├── ProfessorController.java
│   │   └── InscricaoController.java
│   │
│   ├── persistence/
│   │   ├── CursoRepository.java
│   │   ├── DisciplinaRepository.java
│   │   ├── ProfessorRepository.java
│   │   └── InscricaoRepository.java
│   │
│   ├── model/
│   │   ├── Curso.java
│   │   ├── Disciplina.java
│   │   ├── Professor.java
│   │   └── Inscricao.java
│   │
│   ├── view/
│   │   ├── CursoView.java
│   │   ├── DisciplinaView.java
│   │   ├── ProfessorView.java
│   │   ├── InscricaoView.java
│   │   ├── ConsultaInscritos.java
│   │   └── ConsultaProcessosAbertos.java
│   │
│   └── util/
│       └── QuickSort.java
```

---

## 🧩 Regras de Negócio

1. Apenas professores cadastrados podem fazer inscrições  
2. Ao remover uma disciplina, todas as inscrições relacionadas são excluídas  
3. Operações de atualização e remoção usam listas encadeadas  
4. Consultas (buscar) usam filas populadas dos arquivos CSV  
5. Arquivos CSV não ficam com linhas vazias após operações  

---

## 📚 Estruturas de Dados Utilizadas

- ListaSimples  
- Fila
- QuickSort  
- HashTable  
