
# Estágio 2024 Target Sistemas - Teste

## 1ª Questão
**Observe o trecho de código abaixo:**
```
int INDICE = 13, SOMA = 0, K = 0;

enquanto K < INDICE faça {

    K = K + 1;

    SOMA = SOMA + K;

}

imprimir(SOMA);
```
**Ao final do processamento, qual será o valor da variável SOMA?**

R: 78

## 2ª Questão
**Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.**

**IMPORTANTE:**

**Esse número pode ser informado através de qualquer entrada de sua preferência ou pode ser previamente definido no código**

```
public class Main {

    public static void main(String[] args){
        int num = 50; // número de entrada abaixo, a ser verificado na sequência
        int fib1 = 0, fib2 = 1, fib3 = 1;
        boolean pertence = false;

        System.out.printf("Sequência: %d, %d, %d", fib1, fib2, fib3);

        do {
            if(num == 0 || num == 1) {
                pertence = true;
                break;
            }

            fib1 = fib2;
            fib2 = fib3;
            fib3 = fib1 + fib2;

            System.out.print(", " + fib3);

            if(num == fib3) {
                pertence = true;
                break;
            }
        } while(fib3 < num);

        if(pertence) {
            System.out.printf("%nO número %d pertence a sequência de Fibonnaci", num);
        }
        else {
            System.out.printf("%nO número %d não pertence a sequência de Fibonnaci", num);
        }
    }

}
```

## 3ª Questão
**Descubra a lógica e complete o próximo elemento:**

**a) 1, 3, 5, 7,** _9_

**b) 2, 4, 8, 16, 32, 64,** _128_

**c) 0, 1, 4, 9, 16, 25, 36,** _49_

**d) 4, 16, 36, 64,** _100_

**e) 1, 1, 2, 3, 5, 8,** _13_

**f) 2, 10, 12, 16, 17, 18, 19,** _20_

## 4ª Questão
**Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em uma sala diferente. Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada.**

**Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada?**

R: A cada ida, iria acionar interruptor e, na volta, marcar neste a qual lâmpada refere-se. Por eliminação, após as 2 idas, o interruptor que eu não acionei, seria referente a única lâmpada que não acendeu.

## 5ª Questão
**Escreva um programa que inverta os caracteres de um string.**

**IMPORTANTE:**

**a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código**

**b) Evite usar funções prontas, como, por exemplo, reverse**

```
public class Main {

    public static void main(String[] args) {
        String string = "Target Sistemas"; // string de entrada, a ser invertida
        String stringInvertida = "";

        for(int i = string.length() - 1; i >= 0; i--) {
            stringInvertida += string.charAt(i);
        }

        System.out.println("String: " + string);
        System.out.println("String invertida: " + stringInvertida);
    }

}
```
