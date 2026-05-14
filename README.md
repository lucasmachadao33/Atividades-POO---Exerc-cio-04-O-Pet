4-
public class Pet {

    // Atributos
    String nome;
    String especie;
    String raca;
    int idade;
    double peso;

    // Método para apresentar o pet
    void apresentar() {

        System.out.println(
            "Olá! Meu nome é " + nome +
            ", sou um " + especie +
            " da raça " + raca + "."
        );

        System.out.println("Tenho " + idade + " anos e peso " + peso + " kg.");
    }

    // Método para aniversário
    void aniversario() {

        idade++;

        System.out.println(
            nome + " fez aniversário e agora tem " + idade + " anos!"
        );
    }

    // Método para avaliar peso
    void avaliarPeso(double pesoIdeal) {

        if (peso < pesoIdeal) {
            System.out.println(
                nome + " está abaixo do peso ideal (" + pesoIdeal + " kg)."
            );

        } else if (peso > pesoIdeal) {
            System.out.println(
                nome + " está acima do peso ideal (" + pesoIdeal + " kg)."
            );

        } else {
            System.out.println(
                nome + " está no peso ideal!"
            );
        }
    }

    // Método principal
    public static void main(String[] args) {

        Pet pet = new Pet();

        pet.nome = "Rex";
        pet.especie = "cachorro";
        pet.raca = "Labrador";
        pet.idade = 3;
        pet.peso = 28.5;

        pet.apresentar();

        pet.avaliarPeso(30.0);
    }
}
