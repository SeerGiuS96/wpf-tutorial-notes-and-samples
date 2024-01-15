# wpf-tutorial-notes-and-samples

# Acerca de WPF

**¿Qué es WPF?**

*Windows Presentation Foundation (WPF)* es el framework de interfaz gráfica de usuario (GUI) más reciente de Microsoft, diseñado para utilizarse con el framework .NET.

## Explicación del Framework GUI

Una interfaz gráfica de usuario (GUI) te permite crear aplicaciones con diversos elementos de interfaz gráfica, como etiquetas y cuadros de texto. A diferencia de la creación manual, donde tendrías que dibujar estos elementos y manejar las interacciones del usuario, como el ingreso de texto y el uso del mouse, un framework GUI simplifica este proceso. Esto permite a los desarrolladores concentrarse en crear aplicaciones excepcionales.

## Opciones para Desarrolladores .NET

Para los desarrolladores .NET, dos frameworks GUI principales son relevantes: *WinForms* y *WPF*. Aunque WPF es más nuevo, Microsoft sigue manteniendo y respaldando WinForms. En el próximo capítulo, exploraremos las diferencias entre estos frameworks, a pesar de su objetivo compartido de simplificar la creación de aplicaciones con interfaces gráficas impresionantes.



# WPF vs. WinForms

## Introducción

En el capítulo anterior, hablamos sobre la esencia de WPF y tocamos brevemente WinForms. En este capítulo, intentaré comparar ambos, ya que, aunque sirven al mismo propósito, existen muchas diferencias significativas. Si nunca has trabajado con WinForms antes y especialmente si WPF es tu primer framework de GUI, puedes omitir este capítulo. Sin embargo, si te interesa conocer las diferencias, sigue leyendo.

## Diferencia Fundamental

La diferencia más importante entre **WinForms** y **WPF** radica en el hecho de que, mientras que WinForms es simplemente una capa sobre los controles estándar de Windows (por ejemplo, un TextBox), WPF se construye desde cero y no depende de los controles estándar de Windows en casi todas las situaciones. Esto puede parecer una diferencia sutil, pero realmente no lo es, como definitivamente notarás si alguna vez has trabajado con un framework que depende de Win32/WinAPI.

### Ejemplo: Botón con Imagen y Texto

Considera un botón con una imagen y texto, un control de Windows atípico. WinForms no ofrece esta posibilidad de manera nativa, por lo que tendrías que dibujar la imagen tú mismo, implementar tu propio botón que admita imágenes o usar un control de terceros. Con WPF, un botón puede contener cualquier cosa, ya que es esencialmente un borde con contenido y varios estados (sin tocar, señalado, presionado). El botón de WPF es "sin apariencia", al igual que la mayoría de los otros controles de WPF, lo que significa que puede contener una variedad de otros controles dentro de él. ¿Quieres un botón con una imagen y texto? ¡Simplemente coloca un control Image y un TextBlock dentro del botón y listo! Simplemente no obtienes este tipo de flexibilidad con los controles estándar de WinForms, por eso hay un gran mercado para implementaciones bastante simples de controles como botones con imágenes, etc.

## Flexibilidad y Compromisos

La flexibilidad de WPF permite diseños no convencionales, pero a veces puede requerir más esfuerzo que WinForms, que simplifica los escenarios comunes. Inicialmente, puede sentirse más trabajoso en WPF crear plantillas para realizar una tarea que se hace fácilmente en una línea de código de WinForms.

## Ventajas Subjetivas

### Ventajas de WPF

- **Novedad y Estándares:** Se alinea con los estándares actuales al ser una tecnología más nueva.
- **Adopción por Microsoft:** Se utiliza en aplicaciones significativas de Microsoft como Visual Studio.
- **Flexibilidad:** Permite funcionalidades diversas sin depender de controles adicionales.
- **Enfoque de Terceros:** Los desarrolladores de controles de terceros a menudo se centran en WPF por ser más reciente.
- **Eficiencia con XAML:** Facilita la creación y edición de la GUI al separar el diseño (XAML) del código (C#, VB.NET, etc.).
- **Databinding:** Facilita una separación limpia entre datos y diseño.
- **Aceleración de Hardware:** Utiliza aceleración de hardware para dibujar la GUI, mejorando el rendimiento.
- **Versatilidad:** Permite crear interfaces de usuario tanto para aplicaciones de Windows como para aplicaciones web (Silverlight/XBAP).

### Ventajas de WinForms

- **Estabilidad Comprobada:** Una tecnología establecida y probada debido a su antigüedad.
- **Abundancia de Controles:** Una amplia variedad de controles de terceros disponibles de forma gratuita o para comprar.
- **Diseñador de Visual Studio:** Hasta la fecha de redacción, el diseñador de WinForms en Visual Studio es mejor que el de WPF, donde tendrás que hacer más trabajo por ti mismo.

Esta lista proporciona una visión subjetiva para ayudarte a comprender las fortalezas distintivas de WPF y WinForms según tus necesidades de desarrollo.
