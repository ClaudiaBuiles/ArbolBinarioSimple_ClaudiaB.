# Proyecto: Árbol Binario en Java

## Estudiante
- **Claudia Builes**

##  Objetivos
Desarrollar un programa en **Java** que implemente un **árbol binario simple**, permitiendo:
- Insertar números en el árbol.
- Mostrar el recorrido *inorden*.
- Buscar un número dentro del árbol.
El propósito es comprender la estructura y funcionamiento de los árboles binarios, reforzando habilidades en programación y estructuras de datos.

## ¿Qué es un Árbol Binario?
Un **árbol binario** es una estructura de datos jerárquica donde cada nodo tiene como máximo **dos hijos**: uno izquierdo y uno derecho.  
Se utiliza para organizar y buscar información de forma eficiente.

## Implementación
El programa fue desarrollado en **Java** utilizando una clase `Nodo` para los elementos del árbol y una clase `ArbolBinario` con los métodos:
- `insertar(int valor)`
- `inorden()`
- `buscar(int valor)`

También incluye un **menú en consola** para interactuar con el usuario.

## 🧪 Ejemplo de Ejecución en Consola

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/de7a6187-2221-4659-adfb-2a2830602aad" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/707c0ec5-3c4d-40b7-9bbc-96f2a8f8a9d8" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/c0f2fc0d-0fc9-43c0-b063-7aeb268fd424" />

[ArbolBinarioMain.java](https://github.com/user-attachments/files/22713360/ArbolBinarioMain.java)import java.util.Scanner;

// Clase principal con menú en consola
public class ArbolBinarioMain {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArbolBinario arbol = new ArbolBinario();
        int opcion;

        do {
            System.out.println("\n===== MENÚ ÁRBOL BINARIO =====");
            System.out.println("1. Insertar número");
            System.out.println("2. Mostrar recorrido inorden");
            System.out.println("3. Buscar número");
            System.out.println("4. Salir");
            System.out.print("Seleccione una opción: ");
            opcion = sc.nextInt();

            switch (opcion) {
                case 1:
                    System.out.print("Ingrese un número: ");
                    int valor = sc.nextInt();
                    arbol.insertar(valor);
                    System.out.println("Número insertado correctamente.");
                    break;
                case 2:
                    System.out.println("Recorrido inorden del árbol:");
                    arbol.inorden();
                    break;
                case 3:
                    System.out.print("Ingrese el número a buscar: ");
                    int buscar = sc.nextInt();
                    if (arbol.buscar(buscar))
                        System.out.println("El número SÍ existe en el árbol.");
                    else
                        System.out.println("El número NO se encuentra en el árbol.");
                    break;
                case 4:
                    System.out.println("Saliendo del programa...");
                    break;
                default:
                    System.out.println("Opción no válida.");
            }
        } while (opcion != 4);
    }
}



