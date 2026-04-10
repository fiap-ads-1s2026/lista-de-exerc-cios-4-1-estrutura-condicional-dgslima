[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/PLoS-VBd)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23510392&assignment_repo_type=AssignmentRepo)
# Lista 4 - Algoritmos Python com Validacoes

##  Sumario
- [Descricao](#descricao)
- [Como Utilizar](#como-utilizar)
- [Avaliacao Automatica](#avaliacao-automatica)
- [Exercicios Implementados](#exercicios-implementados)
  - [Exercicio 1 - Media Aritmetica](#exercicio-1---media-aritmetica)
  - [Exercicio 2 - Analise de Credito](#exercicio-2---analise-de-credito)
  - [Exercicio 3 - Desempenho Academico](#exercicio-3---desempenho-academico)
  - [Exercicio 4 - Calculadora Interativa](#exercicio-4---calculadora-interativa)
  - [Exercicio 5 - Verificacao Previdenciaria](#exercicio-5---verificacao-previdenciaria)
  - [Exercicio 6 - Calculadora de IMC](#exercicio-6---calculadora-de-imc)
  - [Exercicio 7 - Categoria de Nadador](#exercicio-7---categoria-de-nadador)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Requisitos de Implementacao](#requisitos-de-implementacao)
- [Execucao Individual](#execucao-individual)

---

##  Descricao

Este projeto contem **7 algoritmos em Python** focados em:

-  **Validacao robusta de dados de entrada**
-  **Calculos matematicos e logicos**
-  **Estruturas condicionais complexas**
-  **Interface amigavel com o usuario**
-  **Tratamento de erros e excecoes**

Cada exercicio foi implementado seguindo boas praticas de programacao, com classes organizadas e metodos bem definidos.

---

##  Como Utilizar

### Execucao do Programa Principal
```bash
python app.py
```

### Avaliacao Automatica
```bash
python scripts/grade_python.py ex1
python scripts/grade.sh ex1
no terminal do GitBash poderá utilizar esse comando: bash .grading/grade.py ex1
```

Modos validos: `ex1`, `ex2`, `ex3`, `ex4`, `ex5`, `ex6`, `ex7`.

### Execucao Individual por Exercicio
```bash
python exercicio1.py  # Executa apenas o Exercicio 1
python exercicio2.py  # Executa apenas o Exercicio 2
# ... e assim por diante
```

---

##  Avaliacao Automatica

O autograder simula entradas e valida as saidas dos metodos:

- `Exercicio1.calcular_media_notas()`
- `Exercicio2.analisar_credito()`
- `Exercicio3.calcular_desempenho_academico()`
- `Exercicio4.menu_calculadora()`
- `Exercicio5.verificar_aposentadoria()`
- `Exercicio6.calcular_imc()`
- `Exercicio7.categorizar_nadador()`

---

##  Exercicios Implementados

### Exercicio 1 - Media Aritmetica

** Enunciado:**
Crie um algoritmo que receba duas notas escolares e calcule a media aritmetica entre elas. E necessario validar os dados de entrada, aceitando apenas valores no intervalo de 0.0 a 10.0. Se qualquer uma das notas estiver fora dessa faixa, exiba uma mensagem de erro e encerre a execucao imediatamente.

** Resultado Esperado:**
```
Digite a primeira nota (0.0 a 10.0): 8.5
Digite a segunda nota (0.0 a 10.0): 7.2
Nota 1: 8.5
Nota 2: 7.2
Media aritmetica: 7.9
```

** Caso de Erro:**
```
Digite a primeira nota (0.0 a 10.0): 12.0
Digite a segunda nota (0.0 a 10.0): 8.5
ERRO: As notas devem estar no intervalo de 0.0 a 10.0
```

---

### Exercicio 2 - Analise de Credito

** Enunciado:**
Crie um algoritmo que analise a viabilidade de um credito financeiro. O sistema deve receber o salario bruto do colaborador e o valor mensal da parcela desejada. Aplique a regra de comprometimento de renda: se a prestacao exceder 20% do salario, informe que a solicitacao foi negada. Caso o valor esteja dentro do limite, confirme a aprovacao.

** Resultado Esperado - Aprovado:**
```
Digite o salario bruto (R$): 5000.00
Digite o valor mensal da parcela desejada (R$): 800.00
Salario bruto: R$ 5000.00
Valor da parcela: R$ 800.00
Comprometimento de renda: 16.0%

SOLICITACAO APROVADA: O valor esta dentro do limite permitido
```

** Resultado Esperado - Negado:**
```
Digite o salario bruto (R$): 3000.00
Digite o valor mensal da parcela desejada (R$): 800.00
Salario bruto: R$ 3000.00
Valor da parcela: R$ 800.00
Comprometimento de renda: 26.7%

SOLICITACAO NEGADA: A prestacao excede 20% do salario
```

---

### Exercicio 3 - Desempenho Academico

** Enunciado:**
Crie um algoritmo que calcule o desempenho academico que receba as notas de tres avaliacoes. O calculo deve seguir a regra de media ponderada, onde as duas primeiras notas possuem peso 1 e a terceira possui peso 2. Apos o processamento, o programa deve exibir a media final e o status do estudante: "Aprovado" para medias iguais ou superiores a 6.0, e "Reprovado" para valores inferiores.

** Resultado Esperado - Aprovado:**
```
Digite a nota da primeira avaliacao (peso 1): 7.0
Digite a nota da segunda avaliacao (peso 1): 6.5
Digite a nota da terceira avaliacao (peso 2): 8.5

Notas das avaliacoes:
1 avaliacao (peso 1): 7.0
2 avaliacao (peso 1): 6.5
3 avaliacao (peso 2): 8.5

Media final: 7.6
Status: APROVADO
```

** Resultado Esperado - Reprovado:**
```
Digite a nota da primeira avaliacao (peso 1): 4.0
Digite a nota da segunda avaliacao (peso 1): 5.0
Digite a nota da terceira avaliacao (peso 2): 6.0

Notas das avaliacoes:
1 avaliacao (peso 1): 4.0
2 avaliacao (peso 1): 5.0
3 avaliacao (peso 2): 6.0

Media final: 5.2
Status: REPROVADO
```

---

### Exercicio 4 - Calculadora Interativa

** Enunciado:**
Crie um algoritmo que apresente um menu interativo com as quatro operacoes aritmeticas fundamentais: adicao, subtracao, divisao e multiplicacao. O sistema deve capturar a escolha do usuario e, em seguida, solicitar dois operandos numericos para processar o calculo correspondente e exibir o quociente, produto, soma ou diferenca resultante.

** Resultado Esperado:**
```
=== CALCULADORA ====
1. Adicao
2. Subtracao
3. Multiplicacao
4. Divisao
5. Sair

Escolha uma opcao (1-5): 1
Digite o primeiro numero: 15.5
Digite o segundo numero: 8.2

Resultado: 15.5 + 8.2 = 23.7
```

** Tratamento de Divisao por Zero:**
```
Escolha uma opcao (1-5): 4
Digite o primeiro numero: 10
Digite o segundo numero: 0

ERRO: Divisao por zero nao e permitida!
```

---

### Exercicio 5 - Verificacao Previdenciaria

** Enunciado:**
Crie um algoritmo que realiza a verificacao previdenciaria, no qual receba a idade cronologica e o tempo de contribuicao (servico) de um colaborador. O algoritmo deve validar o direito a aposentadoria com base nos seguintes criterios alternativos:

- **Criterio por Idade:** Minimo de 65 anos
- **Criterio por Tempo:** Minimo de 30 anos de servico  
- **Criterio Misto:** Minimo de 60 anos de idade combinados com 25 anos de servico

O programa deve emitir um parecer final informando se o trabalhador esta apto ou nao para o beneficio.

** Resultado Esperado - Apto:**
```
Digite a idade cronologica (anos): 62
Digite o tempo de contribuicao (anos): 27

Dados do colaborador:
Idade: 62 anos
Tempo de contribuicao: 27 anos

Analise dos criterios:
 Criterio por Idade (65 anos):  NAO ATENDE
 Criterio por Tempo (30 anos):  NAO ATENDE
 Criterio Misto (60 anos + 25 anos servico):  ATENDE

PARECER: O trabalhador ESTA APTO para aposentadoria
```

** Resultado Esperado - Nao Apto:**
```
Digite a idade cronologica (anos): 58
Digite o tempo de contribuicao (anos): 20

Dados do colaborador:
Idade: 58 anos
Tempo de contribuicao: 20 anos

Analise dos criterios:
 Criterio por Idade (65 anos):  NAO ATENDE
 Criterio por Tempo (30 anos):  NAO ATENDE
 Criterio Misto (60 anos + 25 anos servico):  NAO ATENDE

 PARECER: O trabalhador NAO ESTA APTO para aposentadoria

Para se aposentar, e necessario atender pelo menos um dos criterios:
 Completar 7 anos (criterio idade)
 Contribuir por mais 10 anos (criterio tempo)
 Ou atingir 2 anos de idade e 5 anos de contribuicao (criterio misto)
```

---

### Exercicio 6 - Calculadora de IMC

** Enunciado:**
Crie um algoritmo que peca o peso (kg) e a altura (m) de uma pessoa. Calcule o Indice de Massa Corporal (IMC) e informe se a pessoa esta no peso ideal. (IMC = peso/altura^2)

** Tabela de Apoio - Classificacao do IMC (OMS):**

| Faixa de IMC | Classificacao |
| --- | --- |
| Menor que 18.5 | Abaixo do peso |
| De 18.5 a 24.9 | Peso normal |
| De 25.0 a 29.9 | Sobrepeso |
| 30.0 ou mais | Obesidade |

** Resultado Esperado - Peso Ideal:**
```
Digite o peso em kg: 70.5
Digite a altura em metros: 1.75

Dados informados:
Peso: 70.5 kg
Altura: 1.75 m

Indice de Massa Corporal (IMC): 23.0
Classificacao: Peso normal
Status: ESTA no peso ideal 

Referencia OMS - Peso ideal: IMC entre 18,5 e 24,9
```

** Resultado Esperado - Fora do Peso Ideal:**
```
Digite o peso em kg: 95.0
Digite a altura em metros: 1.70

Dados informados:
Peso: 95.0 kg
Altura: 1.70 m

Indice de Massa Corporal (IMC): 32.9
Classificacao: Obesidade
Status: NAO esta no peso ideal

Referencia OMS - Peso ideal: IMC entre 18,5 e 24,9
```

---

### Exercicio 7 - Categoria de Nadador

** Enunciado:**
Crie um algoritmo que solicite a idade de um nadador e imprima sua categoria seguindo a lista abaixo:

- **Infantil:** 5 a 10 anos
- **Juvenil:** 11 a 17 anos
- **Senior:** 18 anos ou mais
- Se a idade for inferior a 5 anos, informe que o atleta nao possui categoria definida

** Resultado Esperado - Infantil:**
```
Digite a idade do nadador: 8

Idade informada: 8 anos
Categoria: INFANTIL
Faixa etaria: 5 a 10 anos
```

** Resultado Esperado - Juvenil:**
```
Digite a idade do nadador: 15

Idade informada: 15 anos
Categoria: JUVENIL
Faixa etaria: 11 a 17 anos
```

** Resultado Esperado - Senior:**
```
Digite a idade do nadador: 25

Idade informada: 25 anos
Categoria: SENIOR
Faixa etaria: 18 anos ou mais
```

** Idade Insuficiente:**
```
Digite a idade do nadador: 3

Idade informada: 3 anos
Categoria: O atleta nao possui categoria definida
Motivo: Idade inferior a 5 anos
```

---

##  Estrutura do Projeto

```
lista4-python/
 app.py                    # Menu principal interativo
 exercicio1.py            # Media aritmetica de notas
 exercicio2.py            # Analise de credito financeiro
 exercicio3.py            # Desempenho academico
 exercicio4.py            # Calculadora interativa
 exercicio5.py            # Verificacao previdenciaria
 exercicio6.py            # Calculadora de IMC
 exercicio7.py            # Categoria de nadador
 README.md                # Este arquivo
 scripts/                 # Scripts de avaliacao
     grade_python.py
     grade.sh


## Requisitos de implementacao
- Use Python 3.6 ou superior
- Mantenha a estrutura de classes
- Use `input()` para entrada de dados
- Use `print()` para saida de dados
- Mantenha os nomes dos metodos esperados pelo autograder
