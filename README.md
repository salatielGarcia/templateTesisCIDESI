Template de tesis para CIDESI
=============================

El siguiente formato utiliza Latex para la generación de tesis. El archivo principal del proyecto es `tesisMain.tex` el cual importa el resto de los documentos para la generación del documento final. Dependiendo del editor que se utilice puede variar el método para poder compilar desde cualquier otro archivo el proyecto completo.

Para ayudar en la organización de documentos grandes se recomienda que cada capítulo este contenido en un archivo y después sea agregado al documento completo por medio del comando `\include{*}`. El nombre del documento a incluir va en la posición del asterisco **sin la extensión**. Se prefiere `include` sobre `input` ya que en compilaciones continuas solo se recompilan aquellos documentos que han sido modificados, mientras que `input` compila siempre todo. Además, se puede utilizar el comando `\includeonly` cuando se está trabajando en un solo capítulo para reducir el tiempo de compilación.

Se agrega el comando `\clearemptydoublepage` el cual forza a que los nuevos capítulos siempre inicien en página con número impar, es decir, empezará siempre al frente de la página.

Los margenes están definidos pensando en impresión a doble cara, de tal manera que el margen adicional para empastado está intercalado, hojas par del lado izquierdo y hojas impar del lado derecho.

Recomendaciones
---------------

- **TexLive**: versión más reciente, se puede encontrar [aquí](https://tug.org/texlive/acquire-netinstall.html). Otras versiones deben de funcionar.
- **Latexmk**: como entorno de compilación, reduce los ciclos necesarios, se puede encontrar [aquí](http://personal.psu.edu/~jcc8/software/latexmk/). Este compilador viene incluido en la instalación de TexLive. Otras opciones como [`arara`](https://www.ctan.org/pkg/arara)  no han sido probadas.
- **Sumatra PDF**: solo en _Windows_, se puede encontrar [aquí](https://www.sumatrapdfreader.org/download-free-pdf-viewer.html). La principal ventaja es que no se requiere cerrar el archivo pdf para compilar, además de ser bastante ligero (rápido).
- **Zathura**: en sistemas _Unix_. Se requiere el _plugin_ para lectura de archivos pdf, se puede encontrar [aquí](https://pwmt.org/projects/zathura/download/). Otras opciones pueden ser **Okular**, **Evince**.

Paquetes utilizados
-------------------

Se presenta una breve descripción de los paquetes utilizados. Si se desea adentrar en las opciones utilizadas revisar la documentación de cada uno de los paquetes. En algunos casos el orden en el que se agregan los paquetes tiene relevancia, tener cuidado con eso.

- `fontenc`: para habilitar el uso general de distintos tipos de fuentes. En la página de [https://tug.org/FontCatalogue/](_The Latex Font Catalog_) se pueden encontrar múltiples tipos de fuentes además de la metodología para utilizarlas.
- `inputenc`: para permitir el uso de caracteres acentuados dentro del documento.
- `geometry`: definición de margenes y tamaño de hoja.
- `minted`: para entrada y formato de código dentro del documento. Si se desea habilitar la codificación del lenguaje SPICE revisar [instrucciones](https://github.com/salatielGarcia/spiceForMinted).
- `caption`: para poner en negritas los _captions_ en figuras y tablas.
- `biblatex`: para referencias bibliográficas, se requiere el uso de _biber_.
- `tocloft`: mejora un poco el formato de los índices, se puede eliminar sin afectar el formato.
- `babel`: para definir el formato en español.
- `\decimalpoint`: para la utilización del punto como separador decimal.
- `hyphenat`: para habilitar el uso de guiones al final de párrafos, ayuda en la estética del documento.
- `enumitem`: agrega opciones adicionales para la numeración de listas.
- `xcolor`: agrega nombres de colores predefinidos.
- `graphicx`: permite la inserción de imágenes.
- `titling`: agrega opciones para el formato de títulos.
- `fancyhdr`: agrega opciones para el formato de encabezados y pies de página.
- `csquotes`: mejora el formato de comillas.
- `amsmath, amssymb, bm`: paquetes matemáticos.
- `steinmetz`: mejora la notación de números polares (opcional).
- `xfp`: permite el uso de operaciones matemáticas durante la compilación del documento, útil para cálculos de resultados.
- `siunitx`: manejo de unidades y notación numérica.
- `booktabs`: mejora el formato de tablas.
- `subfig`: figuras múltiples.
- `tikz`: creación de imágenes.
- `circuitikz`: diseño de circuitos nativo de Latex.
- `pgfplots`: generación de gráficas nativo de Latex.
- `pdfpages`: inserción de hojas de documentos en pdf, útil para agregar las hojas de liberación de tesis.
- `titlesec`: formato de inicio de capítulo.
- `hyperref`: referencias cruzadas en el pdf.
