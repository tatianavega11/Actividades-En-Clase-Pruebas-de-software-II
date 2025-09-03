package tallerpruebas;

import java.util.LinkedList;
import java.util.Queue;
import java.util.Scanner;
import java.util.Stack;

public class TallerPruebas {
    public void ejercicio1() {
            Scanner in = new Scanner(System.in);
            int promt = 10;
            int suma = 0;
            int [] numeros = new int[10];
            for(int i = 0; i<numeros.length; i++){
                numeros[i] = in.nextInt();
            } 
            for(int j : numeros){ 
                suma += j;
            }
            int prom = suma / promt;
            System.out.println("la suma de los numeros del arreglo es: " + suma);
            System.out.println("el promedio de los numeros del arreglo es: " + prom);

     }
    
    
    public void ejercicio2(){
        Stack <Integer> pila = new Stack<>();
        pila.push(3);
        pila.push(4);
        pila.push(31);
        pila.push(24);
        pila.push(32);
        System.out.println("El contenido de la pila es:" + pila);

    
    
    
    
    }
    public void ejercicio3(){
        Queue<String> cola = new LinkedList<>();
        cola.add("Carlos");
        cola.add("tatiana");
        cola.add("Juan");
        cola.add("Maria");
        cola.add("victoria");
        for(String m : cola){
            System.out.println(m);
        }
        cola.poll();
        cola.poll();
        for(String m : cola){
            System.out.println(m);
        }
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        TallerPruebas tp = new TallerPruebas();
        int opcion;
 
        do {
            System.out.println("===== MENÚ PRINCIPAL =====");
            System.out.println("1. Manejo de arreglo");
            System.out.println("2. Manejo pila");
            System.out.println("3. manejo cola");
             System.out.println("4. Salir");
            opcion = scanner.nextInt();
 
            switch (opcion) {
                case 1:
                    tp.ejercicio1();
                    break;
                case 2:
                   tp.ejercicio2();
                    break;
                case 3:
                    tp.ejercicio3();
                    break;
                default:
                    System.out.println("DEBES ELEGIR UNA OPCION VALIDA");
            }
 
            System.out.println();
        } while (opcion != 4);
 
        scanner.close();
    }
 }
    

