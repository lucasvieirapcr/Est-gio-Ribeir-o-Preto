# Estagio-Ribeirao-Preto
Respostas da segunda parte do processo seletivo




1)RESPOSTA: dentro do loop, K é incrementado em 1 a cada iteração e o valor de K é adicionado a SOMA. Então quando K atingir 13, a condição K < INDICE será falsa e o loop terminará.Portanto, ao final do processamento, o valor da variável SOMA será 91.


2)
import java.util.Scanner;
public class Fibonacci {

    public static boolean isFibonacci(int num) {
        if (num == 0 || num == 1) {
            return true;
        }

        int a = 0, b = 1;
        while (b <= num) {
            if (b == num) {
                return true;
            }
            int temp = b;
            b = a + b;
            a = temp;
        }
        return false;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Informe um número para verificar se pertence à sequência de Fibonacci: ");
        int num = scanner.nextInt();

        if (isFibonacci(num)) {
            System.out.println("O número " + num + " pertence à sequência de Fibonacci.");
        } else {
            System.out.println("O número " + num + " NÃO pertence à sequência de Fibonacci.");
        }

        scanner.close();
    }
}



3)
a) 1, 3, 5, 7, _9_

b) 2, 4, 8, 16, 32, 64, _128_

c) 0, 1, 4, 9, 16, 25, 36, _49_

d) 4, 16, 36, 64, _100_

e) 1, 1, 2, 3, 5, 8, _13_

f) 2,10, 12, 16, 17, 18, 19, _20_



4)RESPOSTA: Na primeira visita eu ligaria um dos interruptores e aguardaria alguns minutos, na segunda visita eu desligaria o interruptor que eu havia ligado anteriormente e consideraria essas possibilidades:

Primeira: Se a lâmpada estiver acesa, você sabe que o interruptor que você ligou e desligou novamente controla essa lâmpada.
Segunda: Se a lâmpada estiver desligada, e a outra estiver acesa, você sabe que o interruptor que você deixou ligado controla a lâmpada acesa.
Terceira: Se a lâmpada estiver desligada, e a outra também estiver desligada, você sabe que o interruptor que você deixou desligado controla a lâmpada que permaneceu desligada durante todo o processo.

Dessa forma, você consegue determinar qual interruptor controla cada lâmpada usando apenas duas visitas à sala das lâmpadas.
 

5)
import java.util.Scanner;

public class Invertendo {

    public static String inverterString(String str) {
        char[] caracteres = str.toCharArray();
        int inicio = 0;
        int fim = caracteres.length - 1;


        while (fim > inicio) {
            char temp = caracteres[inicio];
            caracteres[inicio] = caracteres[fim];
            caracteres[fim] = temp;
            inicio++;
            fim--;
        }

        return new String(caracteres);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite uma string para inverter: ");
        String entrada = scanner.nextLine();

       
        String invertida = inverterString(entrada);
        System.out.println("String invertida: " + invertida);

        scanner.close();
    }
}



