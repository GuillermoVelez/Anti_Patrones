# Anti-patrones
## Autores: Luis Guillermo Velez - Johan Aguirre Diaz
### Código muerto
Consiste en crear grandes cantidades de código con poca documentación, de forma desordenada y poca claridad de su funcionamiento en el sistema. A medida que el proyecto avanza en su desarrollo el sistema se hace solidifica y resulta más complicado cambiar funcionalidades, documentarlo, reutilizarlo e incluso entenderlo. También se conoce como "Lava flow" ya que caracteriza a los trozos de código (flujo de lava), y a medida que avanza el proyecto se dificulta el cambiar o mejorar este código (flujo de lava seco y endurecido).

##### Principales Sintomas:
* Se crean variables, objetos o lineas de código que no son justificadas.
* Los nombres de las variables, clase y/o objetos no se relacionan con su funcionalidad.
* Se construyen clases o muchas lineas de código complejas sin documentar.
* Existen muchas áreas de codigo por terminar o por reemplazar.

##### Consecuencias: 
* Se genera perdida de modularidad del cóidgo, esto dificulta la reutilización de fragmentos de código. Esto implica que el codigo sea mas confuso y pueda contener funcionalidades duplicadas.
* Se dificulta documentar el código.
* Se dificulta la posibilidad de mejorar el código a medida que va avanzando el desarrollo del programa.

##### Causas
* El sistema fue puesto en producción sin revisión previa.
* No existe una arquitectura definida.
* El desarrollo esta a cargo de una sola persona.
* Existen varios métodos de prueba.
* El código debe ser corregido constantemente.

##### Solucion
* Tener un desarrollo comentado y estructurado desde el comienzo del proyecto.
* Eliminar partes no funcionales del código (código muerto).

##### Ejemplo:
```java
 public int Sumar_Numeros (int a, int b){
    int c=b-a
    return a+b
 }
```

### Fantasma
Consiste en un numero grande de clases (Fantasmas) o de tablas en una base de datos, con muy pocas responsibildades. Existe un gran número de clases con un ciclo de vida breve, que disfrazan la idea de que el sistema esta construido bajo unos pocos módulos, arhivos o clases,y ocultar las presencia del anti-patron The God.

##### Principales Sintomas:
* El diseño es inestable.
* El rendimiento del sistema es pobre.
* Se dificulta mejorar o cambiar el código ya que se dificulta encontrar los elementos relevantes del sistema.


##### Causas
* El diseño del proyecto no coincide con la implementacíon.
* Las clases del proyecto aparecen solamente para iniciar un método.

##### Solucion
* Eliminar clases fantasmas.
* Replantear un diseño sólido del proyecto.

##### Ejemplo:
```java
  public class Multiplicacion{
      public int Multiplicar_numeros(int a, int b){
        return a*b;
      }
  }
  public class Recibir_numeros{
      public void ir_multiplicacion(int c, int z){
         operacion= Multiplicacion();
         operacion.Multiplicar_numeros(c,z);
      }
  }
  package Fantasma;
  import java.util.Scanner;
  public class Usuario{
      public static void main(String[] args) {
          int numero1,numero2;
          System.out.println("Digite los respectivos numeros");
          Scanner leer=new Scanner(System.in);
          numero1=leer.nextInt();
          numero2=leer.nextInt();
          usuario= Recibir_numeros(); 
          usuario.ir_multiplicacion(numero1,numero2);
      }
  }
  
```

##### Referencias:
Grupo 0 – Antipatrones
https://aprendearquitecturasoftware.wordpress.com/2018/10/13/grupo-0-antipatrones/

Antipatron Lava Flow-Edwin Salcedo
https://www.academia.edu/9453479/Antipatron_Lava_Flow

cómo NO hacer programas Las mejores prácticas MCs Jvier González Sánchez
https://es.slideshare.net/javiergs/cb894-antipatterns

Patrones de Diseño, Refactorización y Antipatrones.
Ventajas y Desventajas de su Utilización en el Software
Orientado a Objetoso Gustavo Damián Campo

https://www.ucasal.edu.ar/htm/ingenieria/cuadernos/archivos/4-p101-Campo.pdf
