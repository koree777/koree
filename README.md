import java.util.Scanner;
import java.util.Random;

public class Main {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        Random random = new Random();

        boolean motorLigado = false;
        boolean embreagem = true;

        System.out.println("Deseja ligar o motor? (sim/não)");
        String resposta = input.nextLine();

        if (resposta.equalsIgnoreCase("sim")){
            motorLigado = true;
            System.out.println("Motor inicializado com sucesso");
        } else{
            System.out.println("Seu motor permanecerá desligado , tente novamente inicialo seguindo os protocolos de segurança");
        return;
        }
        if (embreagem){
            System.out.println("Embreagem pressionada com sucesso");
        } else {
            System.out.println("Pressione a embreagem para prosseguir com a inicialização do motor");
        }



        int rpm = random.nextInt(9000)+800;
        System.out.println("seu rpm é " + rpm);


        int falha = random.nextInt(10);

        if (falha == 0) {
            System.out.println("Motor falhou!");
        }

        if (rpm >= 9000){
            System.out.println("Motor quebrou");
        }
        else if (rpm >=8000){
            System.out.println("dano no motor");
        }
        else if (rpm >= 3500 && rpm <= 5000){
            System.out.println("Troque a marcha");
        }
        else if (rpm >= 5001 && rpm <= 7999){
            System.out.println("troque a marcha");
        }
       for (int marcha = 1 ; marcha <=5; marcha ++){
           if (marcha == 1){
               System.out.println("Carro saindo em primeira marcha");
           } else {
               System.out.println("Deseja trocar a marcha ?"+ marcha);
           }
       }
    }
}
