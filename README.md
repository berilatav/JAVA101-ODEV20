Program to calculate combination with Java

Kombinasyon formülü
C(n,r) = n! / (r! * (n-r)!)

import java.util.Scanner;
public class Odev20 {
    public static void main(String[] args) {

        int N, r, NtoR, factN = 1, factNtoR = 1, factR = 1, result;

        Scanner input = new Scanner(System.in);
        System.out.println("Enter the number of elements of the set(N) :"); // Kümenin eleman sayısını giriniz.
        N = input.nextInt();

        System.out.println("Enter the number of combinations of the set(r) :"); // Kümenin kombinasyon sayısını giriniz.
        r = input.nextInt();

        // (n-r)! = işlemi için totalNtoR
        NtoR = N-r;

        for (int i = N; i > 0; i--){    // N faktöriyel hesaplanması

            factN = factN * i;
        }

        for (int j = NtoR; j > 0; j--) {     //  (n-r)! faktöriyel hesaplanması

            factNtoR = factNtoR * j;
        }

        for (int k = r; k > 0; k--){       // r faktöriyel hesaplanması

            factR = factR * k;
        }

        System.out.println("N! factorial result = "+ factN);  // N Faktöriyel hesabı
        System.out.println("NtoR! factorial result = "+ factNtoR);  // (n-r) Faktöriyel hesabı
        System.out.println("r! factorial result = "+ factR );  // r Faktöriyel hesabı

        result = factN / (factNtoR * factR);
        System.out.println("The result of the combination of the number " + N + " with the number " + r + " = " + result ); // N + " sayısının " + r + " sayısı ile
        kombinasyonunun sonucunun hesaplanması.


    }
}
