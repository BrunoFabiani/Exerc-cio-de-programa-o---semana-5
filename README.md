# Exerc-cio-de-programa-o---semana-5
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

c) Imprime os números pares de 2 a 10.



______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

A) let carro = new Carro("Toyota");


**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

D) 12 (deu 2 mas eu coloquei o código certinho:
let resultado = 0;
for (let i = 10; i >= 0; i -= 2) {
    if (i === 4) {
        continue;
    }
    if (i === 6) {
        break;
    }
    resultado += 1;
}
console.log(resultado))

______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?

A) ![Uma imagem](assets/ex04_1.PNG)

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

A) ![Uma imagem](assets/ex05_1.PNG)

______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

A) "Olá, meu nome é João. Olá, meu nome é Maria."

______

# Questões dissertativas

**7)** Vamos criar um programa em JavaScript para entender classes, métodos e atributos!

class Animal {
    
    constructor (nome, idade) {
        this.nome = nome
        this.idade = idade
    }    
        descrever () {
            console.log (this.nome, this.idade)
        }
}

Luna = new Animal('Luna', '9 anos')
Luna.descrever();

Fifi = new Animal('Fiona', '1 ano e meio')
Fifi.descrever();



______

**8)** Nos últimos dias tivemos a oportunidade de ter contato com Programação Orientada a Objetos, e tivemos contato com o tema "herança". Herança é um princípio de orientação a objetos, que permite que classes compartilhem atributos e métodos. Ela é usada na intenção de reaproveitar código ou comportamento generalizado ou especializar operações ou atributos. Então vamos praticar esse conteúdo nessa questão.
Vamos criar um programa em JavaScript para entender classes, métodos, atributos e herança!

class Animal {
    
    constructor (nome, idade) {
        this.nome = nome
        this.idade = idade
    }    
        descrever () {
            console.log (this.nome, this.idade)
        }
}

Luna = new Animal('Luna', '9 anos')


class Gato extends Animal {
    constructor (nome, idade) {
        super(nome, idade) // chama o super do constructor 
    }
        descrever () {
        console.log (this.nome, this.idade)
        }
        miar () {
        console.log (this.nome +  " = miauuuuu")
        }
} 
Fifi = new Gato ('Fifi', '9 anos')


Fifi.descrever();
Luna.descrever();
Fifi.miar();


______

**9)** Vamos criar um programa em JavaScript para somar notas!

class SomadorDeNotas {
    
    constructor () {

        this.total = 0
        
    };

    somarNota(nota) {
        this.total += nota;
        console.log(this.total)
    }
}
Eduardo = new SomadorDeNotas ();

Eduardo.somarNota(5);
Eduardo.somarNota(6);



______

**10)** Imagine que você está criando um programa em JavaScript para uma escola. Neste programa, existem diferentes tipos de funcionários, cada um com suas próprias características. Considere as seguintes classes:

class Funcionario {
    
    constructor (nome, idade, salarioBase) {
        this.nome = nome
        this.idade = idade
        this.salarioBase = salarioBase //É a classe geral para todos funcionarios, cada um deveria ter um salariobase que deveria dar input para calacular
    };
}
class Professor extends Funcionario{
    constructor (nome, idade, salarioBase, disciplina, horasPorSemana) {
        super(nome, idade, salarioBase)
        this.disciplina = disciplina // Mat = 5, fisica = 4, biologia = 3, Linguas = 2, Educação fisica = 1, , cada matéria ganha diferente como pedido na instrução.
        
        this.horasPorSemana = horasPorSemana
        
    };
    calcularSalarioProf(){
        this.salario = (this.disciplina * this.horasPorSemana)* 10 + this.salarioBase //calcula o extra que o prof vai ganhar dependendo de sua profissão e adiciona ao sálario base
        console.log(this.nome, "ganha =", this.salario,"$")
    }
} 
Mateus = new Professor("mateus", 40, 2500, 5, 30)

Mateus.calcularSalarioProf();

