import java.util.Scanner;
import java.util.Random;

public class Main {

    public static void main(String[] args) throws InterruptedException {



        Scanner input = new Scanner(System.in);
        Random random = new Random();

        boolean motorLigado = false;

        System.out.println("Pressione push para iniciar os procedimentos do carro");
        String resposta1 = input.nextLine();

        if (resposta1.equalsIgnoreCase("push")) {
            System.out.println("Embreagem pressionada");
        } else {
            System.out.println("Pressione a embreagem para iniciar o motor");
        }

        System.out.println("Deseja ligar o motor? (sim/não)");
        String resposta = input.nextLine();

        if (resposta.equalsIgnoreCase("sim")) {
            motorLigado = true;
            System.out.println("Motor inicializado com sucesso");
        } else {
            System.out.println("Motor desligado");
            return;
        }

        new projeto();

        int oil = random.nextInt(10) + 1;

        System.out.println("O nível de óleo é " + oil + " litros");

        int falha = random.nextInt(10);

        if (falha == 0) {
            System.out.println("Motor falhou!");
        }

        if (oil >= 9) {
            System.out.println("Motor quebrou");
        } else if (oil >= 8) {
            System.out.println("Nível de óleo superior ao necessário");
        } else if (oil >= 3 && oil <= 5) {
            System.out.println("Óleo abaixo do nível recomendado");
        } else if (oil >= 6 && oil <= 7) {
            System.out.println("Nível de óleo recomendado");
        }

        int combustivel = random.nextInt(60) + 10;

        System.out.println("Seu nível de combustível é " + combustivel + " litros");

        if (combustivel <= 10) {
            System.out.println("Combustível muito baixo");
        } else if (combustivel <= 20) {
            System.out.println("Combustível na reserva");
        } else if (combustivel <= 30) {
            System.out.println("Tanque em 1/4");
        } else if (combustivel <= 50) {
            System.out.println("Tanque em 3/4");
        } else {
            System.out.println("Tanque cheio");
        }

        System.out.println("Diga 'Olá Mercedes' para acessar a assistente virtual");
        String resposta2 = input.nextLine();

        if (resposta2.equalsIgnoreCase("olá mercedes")) {
            System.out.println("Olá Raidan, como posso ajudar hoje?");
        } else {
            System.out.println("Voz não reconhecida");
        }

        System.out.println("Para abaixar os vidros aperte 1");
        int resposta3 = input.nextInt();

        if (resposta3 == 1) {
            System.out.println("Vidros abaixados");
        }

        input.nextLine();

        System.out.println("Deseja ativar o modo direção automática? (sim/não)");
        String resposta4 = input.nextLine();

        if (resposta4.equalsIgnoreCase("sim")) {
            System.out.println("Modo de direção automática ligado");
        } else {
            System.out.println("Modo de direção automática desligado");
        }

        input.close();
    }
}
