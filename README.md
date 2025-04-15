# Desafio-5.0

# Questao 1
1. Escreva um algoritmo que leia 30 valores e conte quantos números digitados
são pares, impares e nulos.

 int cn, n, cPar, cImpar, cNulos;
        Scanner ler = new Scanner(System.in);

        cn = 1;
        cPar = 0;
        cImpar = 0;
        cNulos = 0;
        while (cn <= 30) {
            System.out.println("Digite um numero");
            n = ler.nextInt();
            if (n == 0) {
                cNulos++;
            } else if (n % 2 == 0) {
                cPar++;
            } else {
                cImpar++;
            }
            cn++;
        }
        System.out.println("Quantos nulos:" + cNulos);
        System.out.println("Quantos pares:" + cPar);
        System.out.println("Quantos impares" + cImpar);
    }

}

# Questao 2
2. Escreva um algoritmo que gere o números de 1000 a 1999 e escreva aqueles
que, divididos por 11, dão resto igual a 5.

 int numero;
        numero = 1000;

        do {
            if (numero % 11 == 5) {
                System.out.println(numero);
            }
            numero++;
        } while (numero <= 1999);

# Questao 3
3. Escrever um algoritmo que lê 10 valores, um de cada vez, e conta quantos deles
estão no intervalo [10,20] e quantos deles estão fora do intervalo, escrevendo
estas informações.

 int c, numero, ce, cf;
        Scanner ler = new Scanner(System.in);
        c = 1;
        ce = 0;
        cf = 0;
        while (c <= 10) {
            System.out.println("Informe um numero");
            numero = ler.nextInt();
            if (numero >= 10 && numero <= 20) {
                ce++;
            } else {
                cf++;
            }
            c++;
        }
        System.out.println("Entre 10 e 20 tem" + ce);
        System.out.println("Fora o intervalo tem" + cf);

    }

}

 # Questao 4
4. Chico tem 1,50 metro e cresce 2 centímetros por ano, enquanto Zé tem 1,10
metro e cresce 3 centímetros por ano. Construa um algoritmo que calcule e
imprima quantos anos serão necessários para que Zé seja maior que Chico.

 int chico, ze, anos;
        chico = 150;
        ze = 110;
        anos = 0;
        while (chico >= ze) {
            chico = chico + 2;
            ze=ze+3;
            anos++;System.out.println("ze: " +ze+ " chico: " +chico );
        } 
        System.out.println(" Ze levou " +anos+ " anos para ser maior que chico ");
        
    }

}
# Questao 5

5. Escrever um algoritmo que leia uma quantidade desconhecida de números e
conte quantos deles estão nos seguintes intervalos: [0,25], [26,50], [51,75] e
[76,100]. A entrada de dados deve terminar quando for lido um número
negativo.

int numero, cont025, cont2650, cont5175, cont76100;
    Scanner ler = new Scanner (System.in);
    
    cont025 = 0;
    cont2650 = 0;
    cont5175 = 0;
    cont76100 = 0;
    numero = 0;
    
    while ( numero >= 0) {
        System.out.println("Digite um número: ");
        numero = ler.nextInt();
        if ( numero >= 0 && numero <= 25) {
            cont025++;
        } else if ( numero >= 26 && numero <= 50 ) {
            cont2650++;
        } else if ( numero >= 51 && numero <= 75) {
            cont5175++;
        } else if ( numero >= 76 && numero <= 100) {
            cont76100++;
        } else {
            System.out.println("Intervalo não contabilizado apenas de 0 a 100");
        }
        System.out.println("[0,25]: "+cont025+" [26,50]: "+cont2650+" [51,75]: "+cont5175+" [76,100]: "+cont76100);
