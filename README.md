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

##### Causas:
* El sistema fue puesto en producción sin revisión previa.
* No existe una arquitectura definida.
* El desarrollo esta a cargo de una sola persona.
* Existen varios métodos de prueba.
* El código debe ser corregido constantemente.

##### Solucion:
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


##### Causas:
* El diseño del proyecto no coincide con la implementacíon.
* Las clases del proyecto aparecen solamente para iniciar un método.

##### Solucion:
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
## Codigo Espagueti

Es un término despectivo en el ámbito de la programación sobre un código enrevesado sin necesidad, particularmente por las ramificaciones de una parte del código con otro. A veces el spaghetti code es el resultado de múltiples modificaciones de un código antiguo.

Otra analogía de que se llame spaghetti es cuando se realiza un cambio en una parte del código y se tienen efectos impredecibles sobre el resto del programa, como cuando halas un tira de espagueti y afecta a las otras

###ejemplo 

![ejemplo](imagenes/ejemploespagueti.PNG)
* imagen obtenida de https://www.tecbolivia.com



## Lava Flow
Algo así como “programar al estilo volcán”. Es construir grandes cantidades de código de manera desordenada, con poca documentación y poca claridad de su función en el sistema. Conforme el sistema avanza en su desarrollo, y crece, se dice que estos flujos de lava se solidifican, es decir, se vuelve mucho más complicado corregir los problemas que originan, y el desorden va creciendo geométricamente. 

Esto se hace patente cuando:

1. Se declaran variables no justificadas
2. Se construyen clases o bloques de código muy grandes y complejas sin documentar, o que no se relacionan claramente con la arquitectura. 
3. Usando un inconsistente y difuso estilo de evolución de una arquitectura.
4. Cuando en el sistema existen muchas áreas con código por terminar o reemplazar. 

### Ejemplo
![ejemplo1](imagenes/ejemplolavaflow.PNG)
* Imagen obtenida de https://es.wikipedia.org/wiki/Lava_seca

### Referencias
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

 https://geekytheory.com/spaghetti-code

 https://www.tecbolivia.com/index.php/articulos-y-tutoriales-microcontroladores/12-el-qcodigo-espaguetiq-y-los-patrones-avanzados-de-programacion

 https://es.wikipedia.org/wiki/Lava_seca
