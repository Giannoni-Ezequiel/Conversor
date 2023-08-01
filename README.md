# Conversor
conversor de divisas utilizando el lenguaje Java.

MoneyCalculator
===============

NOTA PREVIA: Esta aplicación utiliza una API de internet para realizar las conversiones de las divisas. el módulo es totalmente sustituible.

Este proyecto ha sido creado con el fin de adquirir los conocimientos básicos de la arquitectura del software.
Así mismo, estamos ante un conversor de divisas que permite la conversión de las diferentes monedas entre si, a partir de un determinado valor y una fecha específica.

Principios de diseño respetados
===============================
<b>Modelo - Vista - Controlador:</b> El Modelo Vista Controlador (MVC) es un patrón de arquitectura de software que separa los datos y la lógica de negocio de una aplicación de la interfaz de usuario y el módulo encargado de gestionar los eventos y las comunicaciones. Para ello MVC propone la construcción de tres componentes distintos que son el modelo, la vista y el controlador, es decir, por un lado define componentes para la representación de la información, y por otro lado para la interacción del usuario. Este patrón de diseño se basa en las ideas de reutilización de código y la separación de conceptos, características que buscan facilitar la tarea de desarrollo de aplicaciones y su posterior mantenimiento. Evita las referencias circulares

<b>Single responsibility principle:</b> En programación orientada a objetos, se suele definir como principio de diseño que cada clase debe tener una única responsabilidad, y que esta debe estar contenida únicamente en la clase. Así:
- Una clase debería tener sólo una razón para cambiar
- Cada responsabilidad es el eje del cambio
- Para contener la propagación del cambio, debemos separar las responsabilidades.
- Si una clase asume más de una responsabilidad, será más sensible al cambio.
- Si una clase asume más de una responsabilidad, las responsabilidades se acoplan.

<b>Open-Close Principle:</b> Acuñado por el Dr. Bertrand Meyer en su libro "Object Oriented Software Construction", afirma que una clase debe estar abierta a extensiones, pero cerrada a las modificaciones.
OCP es la respuesta a la pregunta que hacíamos anteriormente, ya que argumenta que deberíamos diseñar clases que nunca cambien, y que cuando un requisito cambie, lo que debemos hacer es extender el comportamiento de dichas clases añadiendo código, no modificando el existente.

<b>Liskof Substitution Principle:</b> Cada clase que hereda de otra puede usarse como su padre sin necesidad de conocer las diferencias entre ellas. En lenguaje mas formal: si S es un subtipo de T, entonces los objetos de tipo T en un programa de computadora pueden ser sustituidos por objetos de tipo S (es decir, los objetos de tipo S pueden sustituir objetos de tipo T), sin alterar ninguna de las propiedades deseables de ese programa (la corrección, la tarea que realiza, etc.)

<b>Interface Segregation Principle:</b> Fue utilizado por primera vez por Robert C. Martin durante unas sesiones de consultoría en Xerox. Por aquella época, Xerox estaba diseñando una impresora multifuncional. El software diseñado para la impresora funcionaba y se adaptaba perfectamente a las necesidades iniciales de la impresora; sin embargo, conforme fue evolucionando, y por lo tanto cambiando, se hizo cada vez más difícil de mantener. Cualquier modificación tenía un gran impacto global sobre el sistema. La utilización de ISP permitió reducir los riesgos de las modificaciones y otorgó una mayor facilidad al mantenimiento. El ISP declara que <i>los clientes no deben ser forzosamente dependientes de las interfaces que no utilizan.</i>

<b>Dependency inversion Principle:</b> Este principio dicta que los módulos de alto nivel no deberían depender de módulos de bajo nivel. Ambos deberían depender de abstracciones.Así mismo, Las abstracciones no deberían depender de los detalles. Los detalles deberían depender de las abstracciones.


Patrones de diseño utilizados
=============================
<b>Command:</b> Encapsula un mensaje como un objeto. Especifica una forma simple de separar la ejecución de un comando, del entorno que generó dicho comando. Permite solicitar una operación a un objeto sin conocer el contenido ni el receptor real de la misma. Si bien estas definiciones parecen un tanto ambigüas, sería oportuno volver a leerlas luego de entender el ejemplo.
Este patrón se suele establecer en escenarios donde se necesite encapsular una petición dentro de un objeto, permitiendo parametrizar a los clientes con distintas peticiones, encolarlas, guardarlas en un registro de sucesos o implementar un mecanismo de deshacer/repetir.

<b>Dependency injection:</b> Patrón de diseño orientado a objetos, en el que se suministran objetos a una clase en lugar de ser la propia clase quien cree el objeto. El término fue acuñado por primera vez por Martin Fowler.

<b>Singleton:</b> La idea del patrón Singleton es proveer un mecanismo para limitar el número de instancias de una clase. Por lo tanto el mismo objeto es siempre compartido por distintas partes del código. Puede ser visto como una solución más elegante para una variable global porque los datos son abstraídos por detrás de la interfaz que publica la clase singleton.
Dicho de otra manera, esta patrón busca garantizar que una clase sólo tenga una instancia y proporcionar un punto de acceso global a ella.
