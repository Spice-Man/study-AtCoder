# study-AtCoder
import java.util.*;
import java.lang.*;
 
 
public class Main {
    public static void main(String[] args) {
       Scanner scan = new Scanner(System.in);
       int movekoma = 0;
       int N = scan.nextInt();
       int koma[] = new int[N];
      
       for(int i = 0; i < N; i++){
         koma[i] = scan.nextInt();
       }
       
       int M = scan.nextInt();
       int susumu[] = new int[M];
      
       for(int j = 0; j < M; j++){
         susumu[j] = scan.nextInt();
       }
       
       out: for(int k = 0; k < M; k++){
         movekoma = koma[susumu[k]-1] + 1;
         for(int t = 0; t < N; t++){
           if(movekoma == koma[t]){
             continue out;
           }
         }
         if (movekoma <= 2019){
           koma[susumu[k]-1] = movekoma;
         }
       }
       for(int m = 0; m < N; m++){
         System.out.println(koma[m]);
       }
    }
}
