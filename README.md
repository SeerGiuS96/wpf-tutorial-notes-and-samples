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


# Visual Studio Community

*WPF*, as previously described, is a fusion of XAML (markup) and C#/VB.NET/any other .NET language. While you can edit all of it in any text editor, even Notepad included in Windows, and then compile it from the command line, most developers prefer using an IDE (Integrated Development Environment) for the convenience it offers—from writing code to designing the interface and compiling it all.

The preferred IDE for .NET/WPF is **Visual Studio**, but it comes with a significant cost. Fortunately, Microsoft has made it easy and absolutely free for everyone to dive into .NET and WPF. They've introduced a no-cost version of Visual Studio called **Visual Studio Community**. Though this version has slightly fewer features than the full Visual Studio, it provides everything you need to start learning WPF and create real applications.

# What is XAML?

*XAML*, an acronym for eXtensible Application Markup Language, is Microsoft's variant of XML designed for describing a GUI. In contrast to previous GUI frameworks like WinForms, where the GUI was created in the same language used for interacting with it (e.g., C# or VB.NET) and typically maintained by the designer (e.g., Visual Studio), XAML takes a different approach. Similar to HTML, it allows you to easily write and edit your GUI.

muchos controles permiten otro contenido diferente a texto, como otros controles. Aquí tenemos un ejemplo donde tenemos texto en diferentes colores dentro de un mismo botón. Esto se puede lograr utilizando controles TextBlock dentro del Button



While this isn't a comprehensive XAML tutorial, I'll provide a brief overview of how you use it, as it's a crucial component of WPF. Whether you're crafting a Window or a Page, it will consist of a XAML document and a CodeBehind file, working in tandem to create the Window or Page. The XAML file delineates the interface with all its elements, while the CodeBehind manages events and can manipulate the XAML controls.


