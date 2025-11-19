🎓 Atividade de POO

👨‍💻 Aluno: Washington Lyniker

📦 O que é POO?

A Programação Orientada a Objeto é um modelo que buscar usar exemplos do mundo real para a criação de códigos, usando objetos e classes.

🚗 Exemplo: A Classe Carro
Uma classe Carro teria os seguintes atributos:

Marca

Modelo

Cor

Quilometragem

💡 Por que ela surgiu?

Surgiu para lidar com a complexidade crescente de sistemas que o paradigma procedural tornava difíceis de manter e evoluir.

A POO facilita a modelagem de domínios reais, promove reutilização (via herança/composição), modularidade (encapsulamento) e evolução mais segura do código, reduzindo acoplamento e melhorando organização.

🏛️ Os Quatro Pilares da POO

1- Abstração

2- Encapsulamento

3- Herança

4- Polimorfismo

1. 👻 Abstração

Abstração: Simplificando o Complexo

Abstração envolve simplificar sistemas complexos, focando apenas nos detalhes essenciais. Usarei o exemplo de um carro, assim como usei acima: você não precisa entender a complexidade do motor para dirigir um carro. Você interage com o carro através de uma interface simples (volante, pedais, câmbio), abstraindo os detalhes internos do motor e outros sistemas complexos.

2. 💊 Encapsulamento

Encapsulamento é um conceito importante na POO em Java. Ele envolve o agrupamento de dados (atributos) e os métodos que operam esses dados em uma única unidade, uma classe.

O encapsulamento ajuda a proteger os dados internos de uma classe, restringindo o acesso direto a eles e permitindo que sejam acessados ou modificados apenas por meio de métodos públicos (getters e setters).

public class Carro {
    private String cor;
    private String modelo;
    private String marca;
    private int quilometragem;

    public Carro(String cor, String modelo, String marca) {
        this.cor = cor;
        this.modelo = modelo;
        this.marca = marca;
        this.quilometragem = 0;
    }

    public void acelerar() {
        System.out.println("O carro está acelerando.");
    }

    public void frear() {
        System.out.println("O carro está freando.");
    }

    public void virar(String direcao) {
        System.out.println("O carro está virando para " + direcao + ".");
    }

    public int getQuilometragem() {
        return quilometragem;
    }

    public void setQuilometragem(int quilometragem) {
        if (quilometragem >= 0) {
            this.quilometragem = quilometragem;
        } else {
            System.out.println("A quilometragem não pode ser negativa.");
        }
    }
}

No exemplo acima, a classe Carro encapsula os atributos cor, modelo, marca e quilometragem. 
Os métodos getQuilometragem e setQuilometragem fornecem acesso controlado à quilometragem, 
garantindo que ela não possa ser definida como um valor negativo
 e protegendo a integridade dos dados.

3. 🧬 Herança

Herança é como a genética na programação. 
Você pode criar uma nova classe baseada em uma classe existente, 
herdando seus atributos e métodos. Isso economiza tempo e promove a reutilização de código.

Para não termos que repetir o mesmo código em várias classes, 
podemos fazer outras classes herdarem de uma classe principal.

Java

public class CarroEsportivo extends Carro {
    private boolean turbo;

    public CarroEsportivo(String cor, String modelo, String marca, boolean turbo) {
        super(cor, modelo, marca); 
        this.turbo = turbo;
    }

    public void ativarTurbo() {
        System.out.println("Turbo ativado!");
    }
}

No exemplo acima, a classe CarroEsportivo herda da classe Carro. 
Isso significa que CarroEsportivo tem todos os atributos e métodos de Carro, 
além de seu próprio atributo turbo e método ativarTurbo().

Podemos ver isso pelo extends que indica que a classe CarroEsportivo está estendendo (herdando) da classe Carro. 
Em C# usamos : (dois pontos) e o nome da classe que queremos herdar.

4. 🎭 Polimorfismo

   
Polimorfismo é a capacidade de um objeto se comportar de diferentes maneiras dependendo do contexto. 
Em POO, isso geralmente significa que uma classe pode ter métodos com o mesmo nome, 
mas comportamentos diferentes.

Polimorfismo permite que você use a mesma interface (método) para representar diferentes tipos de objetos. 
É como usar a mesma chave para diferentes fechaduras.

Java

public class Carro {
    public void acelerar() {
        System.out.println("Este carro está acelerando.");
    }
}

public class CarroEsportivo extends Carro {
    @Override // Sobrescrevendo o método da classe mãe
    public void acelerar() {
        System.out.println("Este carro esportivo está acelerando rapidamente!");
    }
}

public class ExemploPolimorfismo {
    public static void main(String[] args) {
        Carro meuCarro = new Carro();
        Carro carroEsportivo = new CarroEsportivo();

        meuCarro.acelerar();      
        carroEsportivo.acelerar(); 
    }
}

No exemplo acima, tanto a classe Carro quanto CarroEsportivo têm um método acelerar(). 
No entanto, quando chamamos acelerar() em um objeto CarroEsportivo, 
ele executa o comportamento específico definido na classe CarroEsportivo,
 demonstrando o polimorfismo.

🏁 Conclusão

Na verdade, o POO é uma das coisas mais importantes na programação. 
Como prova disso, todo bootcamp que eu já fiz, independente da linguagem, POO sempre está presente. 
Java, C#, não importa a linguagem, o POO sempre estará lá.

Aprender POO é essencial para qualquer desenvolvedor que queira criar software.

📚 Referências

https://www.dio.me/articles/entenda-facilmente-programacao-orientada-a-objeto-poo

NotebookLM

Google Gemini (para decorar o markdown)

Eu mesmo S2.
