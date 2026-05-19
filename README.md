import java.util.Scanner;
import java.util.Random;

public class Main {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        Random random = new Random();

        boolean motorLigado = false;
        boolean embreagem = true;

        System.out.println("  escreva embreagem para pressionar e prosseguir para os procedimentos de ligar o carro ");
        String resposta1 = input.nextLine();
        if (resposta1.equalsIgnoreCase("embreagem")){
            System.out.println("embreagem pressionada");
        } else{
            System.out.println("pressione a embreagem para iniciar o motor");
        }

        System.out.println("Deseja ligar o motor? (sim/não)");
        String resposta = input.nextLine();
        if (resposta.equalsIgnoreCase("sim")){
            motorLigado = true;
            System.out.println("Motor inicializado com sucesso");
        } else{
            System.out.println("Seu motor permanecerá desligado , tente novamente iniciar seguindo os protocolos de segurança");
        return;
        }
        

        int oil = random.nextInt(9000)+800;
        System.out.println("o nivel de oléo é " + oil);


        int falha = random.nextInt(10);

        if (falha == 0) {
            System.out.println("Motor falhou!");
        }

        if (oil >= 9000){
            System.out.println("Motor quebrou");
        }
        else if (oil >=8000){
            System.out.println("nivel do oléo superior ao necessario , verifique para que nao haja danos ao motor ");
        }
        else if (oil >= 3500 && oil <= 5000){
            System.out.println("oléo abaixo do nivel recomendado");
        }
        else if (oil >= 5001 && oil <= 7999){
            System.out.println("Nivel de oléo recomendado ");
        }
       for (int marcha = 1 ; marcha <=5; marcha ++){
           if (marcha == 1){
               System.out.println("Carro saindo em primeira marcha");
           } else {
               System.out.println("Deseja trocar a marcha "+ marcha );
           }
       }
    }
}
