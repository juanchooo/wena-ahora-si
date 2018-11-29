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
                System.out.println("introduzca su nombre para crear cuenta: ");
                 //Creación de un objeto Scanner
                String nombre2 = name.nextLine ();
                System.out.println("nombre de producto: ");
                String nombre = name.nextLine ();
                System.out.println("precio: ");
                int precio = name.nextInt ();
                articulos.add(nombre);                
            }
            if (entradaTeclado==2){
                System.out.println(articulos.size());
                if(articulos.size()>0){
                    System.out.println("introduzca su nombre para crear cuenta: ");
                    String nombre2 = name.nextLine ();
                    int largo=articulos.size();
                    int i=0;
                    System.out.println("productos");
                    while (i<largo){
                        System.out.println(i+"  "+articulos.get(i));
                        i=i+1;
                    }
                    System.out.println("escriba el indice del producto a comprar");
                    int comprarr = name.nextInt ();
                    Random random = new Random();
                    int x = random.nextInt(100) + 1;
                    if(x<50){
                        articulos.remove(comprarr);
                        System.out.println("compradooooo!!!!!!");
                    }
                    else{
                        System.out.println("lo sentimos, un millonario compro el articulo");
                    }                    
                }
                else{
                    System.out.println("no hay articulos para comprar");
                }
            }
            if (entradaTeclado==3){
              if (articulos.size()!=0){
                int largo=articulos.size();
                int i=0;
                System.out.println("productos");
                while (i<largo){
                    System.out.println(i+"  "+articulos.get(i));
                    i=i+1;
                }  
              }
            }
        }   
    }
}
