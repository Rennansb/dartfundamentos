# Dart_fundamentos
Seguiremos a trilha do Dart de forma rapida e descomplicada!


O objetivo desta parte é dominar os conceitos fundamentais da linguagem Dart. Esses conceitos serão essenciais para criar aplicações Flutter eficientes. Vou dividir cada tópico em partes, explicando e mostrando exemplos práticos que você poderá executar no dartpad.dev.

## 1 Tipos de Dados em Dart

Dart possui diversos tipos de dados, como:

**int**: Números inteiros.

**double**: Números de ponto flutuante.

**String**: Texto.

**bool**: Booleano (verdadeiro ou falso).

**List**: Lista de elementos (array).

**Map**: Estrutura chave-valor.

**Set**: Conjunto de valores únicos.

Exemplos Práticos:


```
void main() {
  int idade = 25;
  double altura = 1.75;
  String nome = "Rennan";
  bool programador = true;

  print("Meu nome é $nome, tenho $idade anos e $altura metros de altura.");
  print("Eu sou programador? $programador");
}
```

## Exemplo 1.1: Listas, Mapas e Conjuntos

```
void main() {
  // Lista
  List<String> frutas = ["Maçã", "Banana", "Laranja"];
  print("Frutas: $frutas");

  // Mapa
  Map<String, int> estoque = {"Maçã": 10, "Banana": 5, "Laranja": 20};
  print("Estoque: $estoque");

  // Conjunto
  Set<int> numeros = {1, 2, 3, 3, 4}; // 3 é duplicado e será ignorado
  print("Números únicos: $numeros");
}
```

## 1.2 Controle de Fluxo (If, Else, Switch)

O controle de fluxo em Dart permite que você tome decisões com base em condições.

Exemplo 1.2.1: Uso de If e Else

```
Exemplos Práticos:

void main() {
  int idade = 18;
  if (idade >= 18) {
    print("Você é maior de idade.");
  } else {
    print("Você é menor de idade.");
  }
}
```

Exemplo 1.2.2: Uso de Switch Case
```
void main() {
  String diaDaSemana = "terça";
  switch (diaDaSemana) {
    case "segunda":
      print("Hoje é segunda-feira.");
      break;
    case "terça":
      print("Hoje é terça-feira.");
      break;
    case "quarta":
      print("Hoje é quarta-feira.");
      break;
    default:
      print("Dia não reconhecido.");
  }
}
```



Vamos prosseguir com Funções e Estruturas de Controle. Entender como usar funções e criar estruturas de controle eficazes é essencial para escrever código organizado e reutilizável em Dart.

## 2. Funções em Dart

As funções são blocos de código que executam tarefas específicas e podem ser reutilizadas em diferentes partes de um programa. Em Dart, você pode definir funções que retornam valores ou apenas executam ações.

Sintaxe Básica de Funções
```
tipoRetorno nomeDaFuncao(parâmetros) {
  // Bloco de código
  return valor;
}
```

## Exemplos Práticos:
Exemplo 2.1: Função que Retorna um Valor
```
// Função que soma dois números e retorna o resultado
int soma(int a, int b) {
  return a + b;
}

void main() {
  int resultado = soma(5, 10);
  print("O resultado da soma é: $resultado");
}
```

Descrição: A função soma recebe dois parâmetros, calcula a soma e retorna o resultado.

Exemplo 2: Função sem Retorno (void)
```
// Função que imprime uma mensagem
void mostrarMensagem(String mensagem) {
  print("Mensagem: $mensagem");
}

void main() {
  mostrarMensagem("Olá, bem-vindo ao Dart!");
}
```

Descrição: A função _mostrarMensagem_ não retorna nenhum valor, apenas imprime uma mensagem.

## 2.2 Estruturas de Controle (Loops)

Os loops permitem repetir um bloco de código várias vezes. Em Dart, os loops mais comuns são for, while e do-while.

Exemplos Práticos:
Exemplo 1: Loop For
```
void main() {
  for (int i = 0; i < 5; i++) {
    print("O valor de i é: $i");
  }
}
```

Descrição: O loop for repete o bloco de código 5 vezes, incrementando i a cada iteração.

Exemplo 2: Loop While
```
void main() {
  int contador = 0;
  while (contador < 3) {
    print("Contador: $contador");
    contador++;
  }
}
```

Descrição: O loop while executa enquanto a condição contador < 3 for verdadeira.

Exemplo 3: Loop Do-While
```
void main() {
  int numero = 0;
  do {
    print("Número: $numero");
    numero++;
  } while (numero < 3);
}
```
Descrição: O loop do-while garante que o bloco de código seja executado pelo menos uma vez antes de verificar a condição.

## 3 Classes e Objetos em Dart

Dart é uma linguagem totalmente orientada a objetos, o que significa que tudo é um objeto. Uma classe é como um molde ou modelo a partir do qual objetos são criados. Objetos são instâncias de classes que contêm atributos (propriedades) e métodos (funções).

Criando Classes
```
class Pessoa {
  // Atributos
  String nome;
  int idade;

  // Construtor
  Pessoa(this.nome, this.idade);

  // Método
  void apresentar() {
    print("Olá, meu nome é $nome e eu tenho $idade anos.");
  }
}
```

Descrição: A classe Pessoa tem dois atributos, nome e idade, um construtor que inicializa esses atributos, e um método apresentar() que imprime uma mensagem.

Exemplos Práticos:
Exemplo 1: Criando e Usando Objetos
```
void main() {
  Pessoa pessoa1 = Pessoa("Rennan", 25);
  pessoa1.apresentar();
}
```

Resultado: O código cria um objeto pessoa1 da classe Pessoa e chama o método apresentar().

Exemplo 2: Classes com Métodos Personalizados
```
class Carro {
  String marca;
  int ano;

  // Construtor
  Carro(this.marca, this.ano);

  // Método
  void detalhes() {
    print("Este é um $marca fabricado em $ano.");
  }
}

void main() {
  Carro carro1 = Carro("Toyota", 2020);
  carro1.detalhes();

  Carro carro2 = Carro("Honda", 2018);
  carro2.detalhes();
}

```

Descrição: A classe Carro tem atributos marca e ano, e o método detalhes() exibe as informações do carro. Criamos dois objetos, carro1 e carro2, e chamamos o método detalhes().

## 3.1 Construtores Nomeados

Dart permite criar construtores nomeados, que são úteis quando você precisa de múltiplas maneiras de inicializar um objeto.

Exemplo: Construtores Nomeados
```
class Animal {
  String nome;
  int idade;

  // Construtor padrão
  Animal(this.nome, this.idade);

  // Construtor nomeado
  Animal.filhote(this.nome) {
    idade = 0; // Define a idade como 0
  }

  void info() {
    print("Animal: $nome, Idade: $idade anos.");
  }
}

void main() {
  Animal animal1 = Animal("Leão", 3);
  animal1.info();

  Animal animal2 = Animal.filhote("Elefante");
  animal2.info();
}
```

Descrição: Animal.filhote é um construtor nomeado que define a idade como 0 para filhotes.
