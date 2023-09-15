package com.mycompany.lab1tecnicas;

import java.util.ArrayList;
import java.util.List;

/**
 *
 * @author Emmanuel Castillo G, Numar Alexis Zapata Z.
 */
public class Lab1Tecnicas {
    
    record dataRegion (String nombreRegion,float consumoXRegion,int poblacionRegion){}
    
    public static void main(String[] args) {
       
       List  <dataRegion> data = new ArrayList<>();
       data.add( new dataRegion("Caribe",35500600F,10700000));
       data.add( new dataRegion("Andina",150000000F, 37068593));
       data.add( new dataRegion("Orinoquía",20000000F, 2000000));
       data.add( new dataRegion("Amazonía",5000000F, 1243730));
       data.add( new dataRegion("Insular",1000000F, 200000));
       data.add( new dataRegion("Pacífica",10000000F, 1500000));
       
       //1. Mostrar el nombre de todas las regiones.
       double sumaConsumo = 0;
       int sumaPoblacion = 0;
       System.out.println("Las regiones de Colombia son: ");
       System.out.println();
       for (var dataRegion : data ) {
           System.out.println(dataRegion.nombreRegion);
           sumaConsumo += dataRegion.consumoXRegion;
           sumaPoblacion += dataRegion.poblacionRegion;
       }
        System.out.println();
        System.out.print("El consumo nacional por regiones es: "+sumaConsumo);
        System.out.println();
        System.out.print("La población nacional es: "+sumaPoblacion);
        System.out.println();
        
        // 2. Mostrar el consumo promedio por persona nacional
        int promedioPersona;
        promedioPersona = (int) sumaConsumo / sumaPoblacion;
        System.out.print("El consumo por persona a nivel nacional es: "+promedioPersona+" Lt.");
        System.out.println();
        
        // 3. Hallar la región con menos acceso al agua potable. 
        double aux = 999999999;
        String menosAcceso = "";
        for (var dataRegion : data ) {
            if (dataRegion.consumoXRegion < aux){
                aux = dataRegion.consumoXRegion;
                menosAcceso = dataRegion.nombreRegion;
            }
        }
        System.out.println("La región con menos acceso al agua potable es: "+menosAcceso);
        
        //4. Mostrar el consumo por persona de cada región
        float consumoXPersona, menorConsumo = 999999999, mayorConsumo = 0;
        String menorconsuRegion = "",mayorconsuRegion = "";
        for (var dataRegion : data ){
            consumoXPersona = dataRegion.consumoXRegion/dataRegion.poblacionRegion();
            System.out.println("En la region "+dataRegion.nombreRegion+" se consume: "+consumoXPersona+" Lt por persona.");
            System.out.println();
        // 5. Hallar La region que menos agua potable consume por persona
            if (consumoXPersona < menorConsumo){
                menorConsumo = consumoXPersona;
                menorconsuRegion = dataRegion.nombreRegion;
            }
        // 6. Hallar La region que mas agua potable consume por persona
            if (consumoXPersona > mayorConsumo){
                mayorConsumo = consumoXPersona;
                mayorconsuRegion = dataRegion.nombreRegion;
            }
        }
        System.out.println("La region que menos agua potable consume por persona es: "+menorconsuRegion);
        System.out.println();
        System.out.println("La region que mas agua potable consume por persona es: "+mayorconsuRegion);
    }
}
