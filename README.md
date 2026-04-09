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

3. Fazer um programa para ler um número do usuário e determinar se este número 
é par ou não par. 

4. Fazer um programa que recebe 3 valores não inteiros do usuário e mostra o 
maior deles, o menor deles e a média. 

5. Fazer um programa que recebe um símbolo de operação do usuário (+, -, / ou *) 
e dois números reais. O programa deve retornar o resultado da operação recebida 
sobre estes dois números. 

6. Fazer um programa para mostrar os 100 primeiros termos da série de Fibonacci. 

7. Fazer um programa para mostrar todos os números perfeitos entre 1 e 100.  

8. Fazer um programa para receber um número inteiro do usuário e determinar se 
este número é primo ou não. 

9. Crie um programa que construa a tabuada de 2 até 10. 

10. Fazer um programa para mostrar a soma de todos os números de um dominó. 

11. Fazer um programa no qual o usuário vai entrando sucessivamente com valores 
positivos. Quando o usuário entrar com um valor negativo o programa pára de 
pedir valores e calcula a média dos valores já fornecidos.
