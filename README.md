package javaapplication32;

import java.util.ArrayList;
import java.util.Random;
import java.util.Scanner;

/**
 *
 * @author Juan Andres
 */
public class JavaApplication32 {

    /**
     * @param args the command line arguments
     */
    
    public static void main(String[] args) {
        ArrayList<String> articulos = new ArrayList<String>();
        Scanner name = new Scanner (System.in);
        while (true){
            System.out.println("que desea hacer");
            System.out.println("1: vendedor - 2:comprador  -  3:observador");
            Scanner entradaEscaner = new Scanner (System.in);
            int entradaTeclado = entradaEscaner.nextInt ();
            if (entradaTeclado==1){
                
            }
            if (entradaTeclado==2){

            }
            if (entradaTeclado==3){

            }
        }   
    }
}
