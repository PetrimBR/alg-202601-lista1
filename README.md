Projetos da faculdade

**NumerosCalculos.C é um projeto onde usamos bastante operações numéricas para fazer diversos calculos.**

1. Fazer um programa para receber um número inteiro de segundos do usuário e 
imprimir a quantidade correspondente em horas, minutos e segundos.

        void exercicio1() {
            int total, horas, minutos, segundos;
        
            printf("=== Exercício 1 ===\n");
            printf("Digite a quantidade de segundos: ");
            scanf("%d", &total);
        
            horas   = total / 3600;
            minutos = (total % 3600) / 60;
            segundos = total % 60;
        
            printf("%d segundo(s) = %d hora(s), %d minuto(s) e %d segundo(s)\n\n",
                   total, horas, minutos, segundos);
        }

2. Fazer um programa para ler um número do usuário e determinar se este número 
é par ou não par.

        void exercicio2() {
            int numero;
        
            printf("=== Exercício 2 ===\n");
            printf("Digite um número inteiro: ");
            scanf("%d", &numero);
        
            if (numero % 2 == 0)
                printf("%d é PAR\n\n", numero);
            else
                printf("%d é ÍMPAR\n\n", numero);
        }

3. Fazer um programa que recebe 3 valores não inteiros do usuário e mostra o 
maior deles, o menor deles e a média.

        void exercicio3() {
            float a, b, c, maior, menor, media;
        
            printf("=== Exercício 3 ===\n");
            printf("Digite o 1º valor: ");
            scanf("%f", &a);
            printf("Digite o 2º valor: ");
            scanf("%f", &b);
            printf("Digite o 3º valor: ");
            scanf("%f", &c);
        
            // Maior
            maior = a;
            if (b > maior) maior = b;
            if (c > maior) maior = c;
        
            // Menor
            menor = a;
            if (b < menor) menor = b;
            if (c < menor) menor = c;
        
            media = (a + b + c) / 3.0;
        
            printf("Maior: %.2f\n", maior);
            printf("Menor: %.2f\n", menor);
            printf("Média: %.2f\n\n", media);
        }

4. Fazer um programa que recebe um símbolo de operação do usuário (+, -, / ou *) 
e dois números reais. O programa deve retornar o resultado da operação recebida 
sobre estes dois números. 

        void exercicio4() {
            float a, b;
            char op;
        
            printf("=== Exercício 4 ===\n");
            printf("Digite o símbolo da operação (+, -, *, /): ");
            scanf(" %c", &op);
            printf("Digite o 1º número: ");
            scanf("%f", &a);
            printf("Digite o 2º número: ");
            scanf("%f", &b);
        
            switch (op) {
                case '+': printf("%.2f + %.2f = %.2f\n\n", a, b, a + b); break;
                case '-': printf("%.2f - %.2f = %.2f\n\n", a, b, a - b); break;
                case '*': printf("%.2f * %.2f = %.2f\n\n", a, b, a * b); break;
                case '/':
                    if (b == 0)
                        printf("Erro: divisão por zero!\n\n");
                    else
                        printf("%.2f / %.2f = %.2f\n\n", a, b, a / b);
                    break;
                default:
                    printf("Operação inválida!\n\n");
            }
        }

5. Fazer um programa para mostrar os 100 primeiros termos da série de Fibonacci.

        void exercicio5() {
            long long anterior = 0, atual = 1, proximo;
        
            printf("=== Exercício 5 ===\n");
            printf("100 primeiros termos de Fibonacci:\n");
        
            for (int i = 1; i <= 100; i++) {
                printf("%lld", anterior);
                if (i < 100) printf(", ");
                proximo  = anterior + atual;
                anterior = atual;
                atual    = proximo;
        
                if (i % 5 == 0) printf("\n"); // quebra de linha a cada 5 termos
            }
            printf("\n");
        }

6. Fazer um programa para mostrar todos os números perfeitos entre 1 e 100. 

        void exercicio6() {
            printf("=== Exercício 6 ===\n");
            printf("Números perfeitos entre 1 e 100:\n");
        
            for (int n = 1; n <= 100; n++) {
                int soma = 0;
                for (int d = 1; d < n; d++)
                    if (n % d == 0)
                        soma += d;
                if (soma == n)
                    printf("%d\n", n);
            }
            printf("\n");
        }

7. Fazer um programa para receber um número inteiro do usuário e determinar se 
este número é primo ou não.  

        void exercicio7() {
            int numero, primo = 1;
        
            printf("=== Exercício 7 ===\n");
            printf("Digite um número inteiro: ");
            scanf("%d", &numero);
        
            if (numero < 2) {
                primo = 0;
            } else {
                for (int i = 2; i <= (int)sqrt(numero); i++) {
                    if (numero % i == 0) {
                        primo = 0;
                        break;
                    }
                }
            }
        
            if (primo)
                printf("%d É primo\n\n", numero);
            else
                printf("%d NÃO é primo\n\n", numero);
        }

8. Crie um programa que construa a tabuada de 2 até 10. 
        
        void exercicio8() {
            printf("=== Exercício 8 ===\n");
            printf("Tabuada de 2 até 10:\n\n");
        
            for (int t = 2; t <= 10; t++) {
                printf("-- Tabuada do %d --\n", t);
                for (int i = 1; i <= 10; i++)
                    printf("%d x %d = %d\n", t, i, t * i);
                printf("\n");
            }
        }

9. Fazer um programa para mostrar a soma de todos os números de um dominó. 

        void exercicio9() {
            int soma = 0;
        
            printf("=== Exercício 9 ===\n");
            printf("Peças do dominó e suas somas:\n");
        
            for (int i = 0; i <= 6; i++) {
                for (int j = i; j <= 6; j++) {
                    printf("[%d|%d] ", i, j);
                    soma += i + j;
                }
                printf("\n");
            }
        
            printf("\nSoma total de todos os números do dominó: %d\n\n", soma);
        }

10. Fazer um programa no qual o usuário vai entrando sucessivamente com valores 
positivos. Quando o usuário entrar com um valor negativo o programa pára de 
pedir valores e calcula a média dos valores já fornecidos.

        void exercicio10() {
            float valor, soma = 0;
            int quantidade = 0;
        
            printf("=== Exercício 10 ===\n");
            printf("Digite valores positivos (negativo para encerrar):\n");
        
            while (1) {
                printf("Valor: ");
                scanf("%f", &valor);
        
                if (valor < 0) break;
        
                soma += valor;
                quantidade++;
            }
        
            if (quantidade == 0)
                printf("Nenhum valor positivo foi fornecido.\n\n");
            else
                printf("\nQuantidade de valores: %d\nSoma: %.2f\nMédia: %.2f\n\n",
                       quantidade, soma, soma / quantidade);
        }

Para finaliza o código caso coloque todos os exercícios no mesmo arquivo se ultiliza essa função abaixo para chamar a main

    int main() {
        exercicio1();
        exercicio2();
        exercicio3();
        exercicio4();
        exercicio5();
        exercicio6();
        exercicio7();
        exercicio8();
        exercicio9();
        exercicio10();
        return 0;
    }
