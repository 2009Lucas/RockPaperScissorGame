
´´´java
package pptemingles;

import java.util.Scanner;

public class PPTemIngles {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
       int escolhaIA, escolhaJog, opcao, vitorias, derrotas, empates;
        Scanner ler = new Scanner(System.in);
        opcao = 1;
        escolhaJog = 0;
        vitorias = 0;
        derrotas = 0;
        empates = 0;

        while (opcao != 0) {

            System.out.println("0 - Exit");
            System.out.println("1 - Continue");
            System.out.println("CHOSE AN OPTION:");
            opcao = ler.nextInt();

            if (opcao != 0) {
                System.out.println("<==== Welcome at Rock, Paper, Scissor game! ====>");
                System.out.println("--OPTIONS--");
                System.out.println("0 - Rock");
                System.out.println("1 - Paper");
                System.out.println("2 - Scissor");
                System.out.println("Enter your play:");
                escolhaJog = ler.nextInt();

                escolhaIA = (int) (0 + Math.random() * 2);
                System.out.println("IA´s play:" + escolhaIA);

                switch (escolhaIA) {
                    case 0:
                        System.out.println("Rock");
                        break;
                    case 1:
                        System.out.println("Paper");
                        break;
                    case 2:
                        System.out.println("Scissor");
                        break;
                    default:
                        System.out.println("Invalid option!!");
                }

                if (escolhaJog == escolhaIA) {
                    System.out.println("Result: DRAW!");
                    empates++;
                } else if ((escolhaJog == 0 && escolhaIA == 2)
                        || (escolhaJog == 1 && escolhaIA == 0)
                        || (escolhaJog == 2 && escolhaIA == 1)) {
                    System.out.println("Result: YOU WON!!!!!!");
                    vitorias++;
                } else {
                    System.out.println("Result: YOU LOST :( ");
                    derrotas++;
                }
                } else {
                    System.out.println("THANKS FOR PLAY!");
                }

                System.out.println("Player´s chose:" + escolhaJog);
        }

                System.out.println("===== Scoreboard =====");
                System.out.println("VICTORIES: " + vitorias);
                System.out.println("DEFEATS: " + derrotas);
                System.out.println("DRAWS: " + empates);
    }
    }
