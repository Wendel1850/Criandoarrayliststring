# Criandoarrayliststring
import java.util.ArrayList;
import java.util.Scanner;

public class TesteArrayList {
    public static void main(String[] args) {
        // Crie um ArrayList de String (lista1)
        ArrayList<String> lista1 = new ArrayList<>();
        ArrayList<String> lista2 = new ArrayList<>();

        // Adicione 5 Strings informadas pelo usuário
        Scanner scanner = new Scanner(System.in);
        for (int i = 0; i < 5; i++) {
            System.out.print("Digite uma String (" + (i + 1) + "/5): ");
            String input = scanner.nextLine();
            lista1.add(input);
        }

        // Percorra a lista verificando se o usuário digitou alguma String com menos de 3 caracteres
        for (String str : lista1) {
            if (str.length() < 3) {
                lista2.add(str);
            }
        }

        // Utilizando o método removeAll, remova todos os elementos da primeira lista que existam na segunda lista
        lista1.removeAll(lista2);

        // No final imprima a quantidade de Strings da lista1 e da lista2
        System.out.println("Quantidade de Strings na lista1: " + lista1.size());
        System.out.println("Quantidade de Strings na lista2: " + lista2.size());
    }
}
