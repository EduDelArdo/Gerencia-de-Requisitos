# Especificação de Requisitos do Sistema (ERS/SRS)

## Descrição Geral do Sistema
O sistema será responsável por gerenciar o acervo de livros de uma biblioteca,
permitindo o cadastro, consulta, empréstimo e devolução de exemplares. Além disso,
fornecerá funcionalidades para gerenciar usuários (alunos, professores e
funcionários), controlar prazos de devolução e aplicar notificações de atraso.

---

## Requisitos Gerais

### Requisitos Funcionais (RF)
| ID | Descrição | Prioridade |
|----|------------|-----------|
| RF01 | O sistema deve permitir o cadastro de novos livros no acervo. |Essencial|
| RF02 | O sistema deve permitir o empréstimo de livros a usuários cadastrados. |Essencial |
| RF03 | O sistema deve permitir a devolução de livros emprestados. | Essencial |
| RF04 | O sistema deve permitir o cadastro de novos usuários. | Essencial |
| RF05 | O sistema deve permitir a pesquisa de livros portítulo, autorou categoria. | Importante |

### Requisitos Não Funcionais (RNF)
| ID | Descrição | Prioridade |
|----|------------|-----------|
| RNF01 | O sistema deve ser acessível via navegador web em qualquer dispositivo com internet. | Essencial |
| RNF02 | O sistema deve responder às ações do usuário em no máximo 3 segundos. | Essencial |
| RNF03 | O sistema deve armazenar todos os dados de forma segura e protegida. | Essencial |
| RNF04 | O sistema deve possuir interface intuitiva e de fácil navegação. | Essencial |
| RNF05 | O sistema deve permitir até 100 usuários conectados simultaneamente. | Importante |

### Regras de Negócio (RN)
| ID | Descrição | Prioridade |
|----|------------| -----------|
| RN01 | Apenas usuários cadastrados podem realizar empréstimos de livros. | Essencial |
| RN02 | Cada usuário pode emprestar até 5 livros simultaneamente. | Essencial | Essencial |
| RN03 | Livros devem ser devolvidos até a data de vencimento | Essencial | Essencial |
| RN04 | Será cobrada uma multa diária por atraso na devolução dos livros | Essencial | Essencial |
| RN05 | O sistema deve manter um registro atualizado do estoque de livros disponíveis | Essencial | Essencial |
---

## Diagramas UML

### Diagrama de Casos de Uso
![Diagrama de Casos de Uso](docs/casos_de_uso.jpg)

### Diagrama de Sequência
![Diagrama de Sequência](docs/diagrama_sequencia.png)

### Diagrama de Atividades
![Diagrama de Atividades](docs/diagrama_atividades.png)

---

## Arquitetura do Sistema
O sistema adota o estilo arquitetural **MVC (Model–View–Controller)**, separando responsabilidades entre:
- **Model:** lógica e acesso a dados.  
- **View:** interface e interação com o usuário.  
- **Controller:** coordenação entre as camadas.

- ![Arquiteura do Sistema](docs/arquiterura.png)