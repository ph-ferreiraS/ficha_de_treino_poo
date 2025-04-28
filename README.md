# 🏋️ Sistema de Gerenciamento para Personal Trainers

Sistema Java para gerenciar avaliações físicas, cadastro de alunos e geração de treinos personalizados. Desenvolvido para otimizar o trabalho de profissionais de educação física.

---

## 🚀 **Funcionalidades**
- **Cadastro de Alunos**: 
  - Tipos específicos: `Aluno Regular`, `Atleta` e `Aluno Idoso`.
  - Atributos personalizados por categoria (ex: pressão arterial para idosos, offseason para atletas).
- **Avaliações Físicas**:
  - Registro de peso, medidas corporais e percentual de gordura.
  - Histórico de avaliações por aluno.
- **Gestão de Treinos**:
  - Geração automática de treinos baseados no IMC.
  - Personalização de exercícios e duração média.
- **Login e Registro de Personal Trainers**:
  - Autenticação segura com email e senha.
- **Operações CRUD**:
  - Adicionar, remover, editar e favoritar alunos.
  - Edição em cascata para subclasses (ex: ajustar gramas de carboidrato para atletas).

---

## ⚙️ **Tecnologias Utilizadas**
- **Java**: Linguagem principal do projeto.
- **POO**: Herança (`AlunoIdoso` e `Atleta` extendem `Aluno`), encapsulamento e polimorfismo.
- **Bibliotecas**:
  - `java.util.ArrayList`: Para listas dinâmicas de alunos e avaliações.
  - `java.util.UUID`: Geração de IDs únicos para alunos e personais.
- **Console Interativo**: Menu intuitivo com `Scanner` para entrada de dados.

---

## 📂 **Estrutura do Projeto**
```plaintext
trabalhopoo_personaltrainer/
├── Aluno.java              # Classe base para todos os alunos
├── AlunoIdoso.java         # Subclasse com atributos de saúde para idosos
├── Atleta.java             # Subclasse com métricas específicas para atletas
├── AvaliacaoFisica.java    # Registro de avaliações físicas
├── Personal.java           # Classe para gerenciar personal trainers
├── TreinoDoDia.java        # Geração de treinos personalizados
├── Main.java               # Sistema interativo com menus e lógica principal
└── produtos.csv            # Base de dados de produtos (não utilizado neste projeto)

---

```
## 🎯 **Exemplos de Uso**

### 1. Cadastro de Atleta
```java
Atleta atleta = new Atleta(
    "Carlos",         // Nome
    1.85,             // Altura (metros)
    "M",              // Sexo
    true,             // Favorito
    28,               // Idade
    75.5,             // Peso (kg)
    22.1,             // IMC
    15.0,             // GC (% gordura corporal)
    2000,             // ME (metabolismo energético)
    1800,             // MB (metabolismo basal)
    2.5,              // GV (gasto calórico)
    new String[]{"Segunda", "Quarta"}, // Dias disponíveis
    "Treino Pesado",  // Tipo de treino
    true,             // Offseason (fora de temporada)
    false,            // Precontest (pré-competição)
    300,              // Gramas de carboidrato/dia
    4                 // Litros de água/dia
);
```
### 2. Geração de Treino Baseado no IMC
```java
if (imc < 18.5) {
    treinoDoDia.adicionarTipo("Ganho de Massa");
    treinoDoDia.adicionarExercicio("Supino");
    treinoDoDia.adicionarExercicio("Agachamento");
    treinoDoDia.setDuracaoMedia(90); // 90 minutos
    System.out.println("Treino para ganho de massa gerado!");
}
```

---

### 🔍 **Explicação**:
- **Cadastro de Atleta**: Demonstra a criação de um objeto `Atleta` com parâmetros específicos:
  - `new String[]{"Segunda", "Quarta"}`: Dias de treino como array.
  - `true/false`: Flags para offseason e pré-competição.
  
- **Geração de Treino**: Lógica condicional que:
  - Adiciona exercícios baseados no IMC.
  - Define duração do treino automaticamente.
```

👥 Contribuidores

    Gabriel Ribeiro Filice Chayb

    Ítalo Nunes Tillmann de Abreu

    Leandro Elias Fontes Carrijo

    Leandro Silva Pina de Campos

    Pedro Henrique Ferreira Simões
