## ASINCRONIA POR DISEÑO:

* EventLoop: Es un proceso que se comporta como un bucle y se gestiona de forma automática. Todo lo que pase en la aplicación funciona de forma asíncrona asegurando que no se va a bloquear el bucle y todo lo que le enviemos va a ejecutarse aparte. El bucle puede seguir recibiendo peticiones.
Es por esto que Node JS se considera como altamente recurrente y se usa en muchas aplicaciones que requieren múltiples entradas y salidas.
Lo podemos imaginar como un circulo dando vueltas, los eventos vienen desde la cola de eventos o Event Queue

* Event queue: Va a tener todo lo que se ejecute en el código y lo va a ir enviando uno a uno hacia el event loop en donde se van a procesar.

* Thread Pool: En caso de que no sea rápido de resolver se va a enviar al Thread Pool, allí se empezara a gestionar de forma asíncrona. Lo que hace es levantar un hilo nuevo que se encargara de que el proceso se ejecute, una vez termine de ejecutarse el Thread Pool dispara un evento y se devuelve a el Event Loop y si es necesario a el Event Queu

El funcionamiento asíncrono nos sirve para que no se bloquee el hilo principal, ya que las operaciones mas lentas, con bases de datos o lectura de archivos, se van a seguir ejecutando en su propio hilo. Cada hilo se encargara de gestionar sus procesos lentos.

Esto diferencia a Node.JS de otros leguajes como PHP, Python o Java que son síncronos y una operación va detrás de la otra.