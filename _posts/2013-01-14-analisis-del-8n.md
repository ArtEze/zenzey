---
layout: entry
title: Análisis del 8N en Twitter
---
![Grafo Clustering][3]

# Contexto

El 8 de Noviembre (8N) se organizo en Argentina la primera movilización de gran envergadura en oposición al gobierno democrático de Cristina Fernandez de Kirchner. La convocatoria se dio principalmente a través de las redes sociales (Twitter y Facebook) y sus repercusiones en los medios tradicionales (TV, diarios, radios, etc.). A través del uso del Hashtag [#8N](https://twitter.com/#!/search?q=%238N) (un meme) se aglutinó a los usuarios en torno a las consignas que libremente se plantearon en torno a la manifestación. Dado el carácter abierto que mantuvo, la heterogeneidad de los reclamos y pedidos se constituyó en uno de los puntos más criticados por los usuarios afines al gobierno de CFK.

El contexto político actual de Argentina se encausa desde 2008 hacia una marcada polarización ideológica en torno al gobierno kirchnerista que se expresa en posiciones antagónicas sobre la forma de concebir la política nacional e internacional, el manejo de la economía y de la asistencia del estado hacia los sectores vulnerables.  Esta polarización se ve reflejada en el ecosistema de Twitter, donde en torno de los principales antagonistas políticos y mediáticos pudimos detectar [comunidades](http://es.wikipedia.org/wiki/Cluster) `[1]` de afinidad ideológica o política, y cuyas principales figuras fueron el blanco de la mayoría de las menciones de parte de los usuarios que activamente impulsaron la movilización, además de ser la fuente principal de los Retweets más populares.

# Grafos

A través de Zenzey, un producto desarrollado en [Grupo42](http://www.grupo42.com/), monitoreamos todas las menciones referidas a las Keywords "8N", "Cacerolazo" y "#8N" entre el 7 y el 10 de Noviembre obteniendo un total de 154 mil Tweets sobre el tema. Dado el elevado volumen, **el análisis se realizó sobre una muestra de 1055 usuarios que registraron diez o más menciones** entre las realizadas a otros usuarios y las recibidas, esto nos permitió acceder únicamente a los usuarios más influyentes que participaron del evento. A partir de esta muestra generamos dos [grafos](http://es.wikipedia.org/wiki/Grafo) `[2]` sociales en los que se muestran las relaciones entre los usuarios.

## Grafo Menciones

[Éste grafo](/reports/8N/2.html) está compuesto por 3 grandes clusters. 

El cluster 0 está compuesto por personas que recibieron muchas mentions. Entre las figuras de este clúster se reconocen principalmente a **Cristina Fernandez de Kirchner** a través de su cuenta oficial [@CFKArgentina](http://twitter.com/CFKArgentina) como el destinatario de la mayor cantidad de mensajes sobre el 8N.  Mauricio Macri ([@mauriciomacri](http://twitter.com/mauriciomacri)), Jorge Lanata ([@Lanataenel13](http://twitter.com/Lanataenel13)), Jorge Rial ([@jorgerial](http://twitter.com/jorgerial)) y Luis D'Elia ([@Luis_Delia](http://twitter.com/Luis_Delia)) completan la lista de personalidades de la política y el periodismo que mayor cantidad de mensajes recibieron. Entre los medios de prensa más mencionados, encontramos a los diarios La Nación ([@lanacioncom](http://twitter.com/lanacioncom)) e Infobae ([@infobae](http://twitter.com/infobae)) y los canales televisivos de noticias Todo Noticias ([@todonoticias](http://twitter.com/todonoticias)) y C5N ([@C5N](http://twitter.com/C5N)).

El cluster 1 referencia a las cuentas con mayor actividad durante el evento. Las mismas se caracterizan por un ratio de "mentions" muy superior a la media. Este grupo esta compuesto por personas que genuinamente se manifestaron de acuerdo a su ideología más un conjunto de cuentas con comportamiento sospechoso de pertenecer a campañas orquestadas por grupos con distíntos intereses.

El cluster 2 está compuesto por cuentas que manifestaron un comportamiento estándar durante el evento.

## Grafo Clustering

[Este grafo](/reports/8N/) utiliza algoritmos de clustering (utilizando el método Louvain) para la separación de los usuarios en los distintos grupos (7 en total). El resultado son agrupaciones que demuestran interesantes coincidencias ideológicas y políticas, con clusters que representan a diversos grupos de la contienda, por ejemplo:

* **Verde**: cuentas ligadas al oficialismo ([@678Oficial](http://twitter.com/678Oficial), [@cyngarciaradio](http://twitter.com/cyngarciaradio), [@ddd_ok](http://twitter.com/ddd_ok), [@tognetti_daniel](http://twitter.com/tognetti_daniel) y, curiosamente, [@telefenoticias](http://twitter.com/telefenoticias)).

* **Naranja Pálido y Rosa**: medios y periodistas anti-kirchneristas ([@fetcheves](http://twitter.com/fetcheves), [@ertenembaum](http://twitter.com/ertenembaum), [@radiomitre](http://twitter.com/radiomitre), [@perfilcom](http://twitter.com/perfilcom)).

* **Naranja**: cuentas muy populares, con gran cantidad de menciones, entre funcionarios del gobierno, miembros de la oposición y grandes medios.

* **Verde claro**: usuarios comunes, se ven pocas personalidades o famosos.

<img src="/static/img/8N-tabla.png" />

#Análisis de los principales actores

1.  **Nodos centrales**
    Entre los nodos centrales detectamos a personalidades de la política como Cristina Fernandez de Kirchner, Mauricio Macri y Anibal Fernandez; periodistas como Jorge Lanata y Jorge Rial; y medios de prensa digitales o tradicionales como La Nación, Clarín, Infobae, C5N. Alrededor de estos actores se generó la mayor cantidad de menciones y Retweets, lo que ilustra el carácter político y el fuerte impulso mediático que se dio a la movilización.
    La centralidad de los nodos está dada tanto por la cantidad de conexiones que poseen respecto a otros nodos ("Degree Centrality") como así también por la relevancia del nodo por funcionar como puente entre comunidades distintas ("Betweenness Centrality").
2.  **Usuarios genuinos:**
    La mayor cantidad de las interacciones partieron de usuarios genuinos que impulsaron el meme [#8N](https://twitter.com/#!/search?q=%238N) a través del envío de mensajes a sus seguidores y a personas influyentes de los medios o la política, y retweeteando los mensajes de otros usuarios referidos a la movilización. Este conjunto, si bien no está diferenciado en los grafos como un clúster distinto, es por lejos el más voluminoso.
3.  **Spam Bots (o usuarios abusivos)**
    Detectamos un grupo de usuarios que actualmente tienen sus cuentas suspendidas en la plataforma, las mismas se mostraron muy activos en las fechas cercanas al 8N mediante el envío masivo o repetitivo de mensajes a otros usuarios de Twitter. Twitter castiga a los usuarios que envían muchos mensajes indeseados o con contenido repetido con la suspensión. 
    * [@AntonioAmarildo](http://twitter.com/AntonioAmarildo) 
    * [@todosalasplazas](http://twitter.com/todosalasplazas) 
    * [@antonio4017](http://twitter.com/antonio4017) 
    * [@canellargentina](http://twitter.com/canellargentina) 
    * [@LaParcaOk](http://twitter.com/LaParcaOk) 
    * [@martinchoelchek](http://twitter.com/martinchoelchek) 
    * [@MIK_ELA](http://twitter.com/MIK_ELA) 
    * [@opino_hoy](http://twitter.com/opino_hoy) 
    * [@alvarocasablanc](http://twitter.com/alvarocasablanc) 
    * [@jaimelagos2](http://twitter.com/jaimelagos2) 
    * [@Capo150294](http://twitter.com/Capo150294) 
    * [@pablito_solari](http://twitter.com/pablito_solari) 
    * [@Pythep](http://twitter.com/Pythep) 
    * [@silviagracielap](http://twitter.com/silviagracielap) 
    * [@lochamo](http://twitter.com/lochamo) 
    * [@Arturo_Lopez85](http://twitter.com/Arturo_Lopez85) 
    * [@miguellalomia26](http://twitter.com/miguellalomia26) 
    * [@ranchomancho89](http://twitter.com/ranchomancho89) 
    * [@GabyWinsGaby](http://twitter.com/GabyWinsGaby) 
    * [@VenitePorEsta](http://twitter.com/VenitePorEsta) 
    * [@galloester1](http://twitter.com/galloester1) 
    * [@samazul2001](http://twitter.com/samazul2001) 
4.  **Usuarios "sospechosos"**
    Similares a los Spammers pero enmarcando su comportamiento dentro de las reglas de Twitter, encontramos a un segundo grupo al que elegimos llamar Usuarios "Sospechosos" o "Dudosos" dado que mostraron un pico de actividad en torno al 8 de Noviembre a través del envío de mensajes y Retweets, cuyo nivel cayó drásticamente en los días posteriores. No podemos afirmar que sean Bots o no, pero el análisis manual de estos usuarios mostró muchos tweets repetidos entre sí.
    * [@netfilmx](http://twitter.com/netfilmx) 
    * [@8NNNNNNNN](http://twitter.com/8NNNNNNNN) 
    * [@_8N_](http://twitter.com/_8N_) 
    * [@8NO_ORG](http://twitter.com/8NO_ORG) 
    * [@pablomontagner](http://twitter.com/pablomontagner) 
    * [@todosal8N](http://twitter.com/todosal8N) 
    * [@libre_ar](http://twitter.com/libre_ar) 
    * [@orellanasergio1](http://twitter.com/orellanasergio1) 
    * [@SoyMatreros1928](http://twitter.com/SoyMatreros1928) 
    * [@SoledadRojasT](http://twitter.com/SoledadRojasT)

# Conclusiones

Una de las principales conclusiones que podemos extraer de este análisis es que nos encontramos frente a una protesta genuina que contó con un fuerte impulso del trabajo colectivo de muchos usuarios comunes de Twitter organizados en torno al "meme" [#8N](https://twitter.com/#!/search?q=%238N). Dejando de lado los casos puntuales en los que algunos usuarios mostraron comportamientos abusivos o que jugaron en el límite del spam, la gran mayoría de las cuentas era de usuarios reales y que actuaron de buena fe en lo que consideraron una consigna válida y digna de difusión.

A su vez, buena parte de las menciones y acciones realizadas se nucleó en torno a los medios de comunicación y sus principales actores (periodistas, locutores), hecho que fue retribuido y aprovechado mediante la participación activa en la difusión y cobertura de la movilización. Sin embargo, en el marco de la pugna entre los medios y el gobierno de Cristina Fernández de Kirchner por la nueva Ley de Servicios Audiovisuales, no debería pasar desapercibido que la cuenta de Twitter del diario Clarín ([@clarincom](http://twitter.com/clarincom)), el principal antagonista del gobierno en esta pugna, no aparezca entre los nodos centrales. Pero sí subrayamos el importante rol que ocupó la cuenta del diario La Nación como principal medio difusor.

Finalmente, es de destacar la utilización de bots de comportamiento abusivo para tratar de influir en la difusión del 8N. Si bien concluimos que su uso no fue determinante, y de hecho fue sancionado por Twitter a través de la suspensión de las cuentas, fueron uno de los factores más interesantes para analizar dada la dificultad para diferenciar a los usuarios genuinos de los automatizados.

En futuros trabajos, desarrollaremos otras aristas de este conflicto y de otras coyunturas políticas y económicas de amplio impacto en Twitter.


# Cómo navegar la información

Cada usuario se encuentra representado en el grafo por un pelota cuyo tamaño determina la cantidad total de Tweets contabilizados (entre menciones recibidas y enviados enviados) y cuyo color remite al clúster al que pertenece. Clickear sobre la pelota nos permite visualizar las conexiones (representadas por las lineas que unen dos pelotas) que ese usuario posee con otros, y a su vez ver los Tweets que demuestran esas relaciones.

`[Para una mejor visualización, abrir los grafos con Chrome]`

## Grafo

* **Search:** permite buscar cuentas de twitter específicas dentro del grafo.
* **Zoom:** es posible usar el scroll o los botones de arriba a la derecha (Zoom in y Zoom out)
Movimiento: manteniendo el click presionado sobre un espacio en blanco y moviendo el mouse, nos desplazamos dentro del grafo.
* **Barra de Interacciones:** desplazando hacia cualquiera de los lados es posible filtrar las cuentas que se muestran en el grafo en base a la cantidad de interacciones recibidas. Si queremos ver las cuentas con mayor cantidad de menciones o mensajes enviados, corremos el selector de la izquierda hacia la derecha, filtrando las cuentas con menor cantidad de interacciones.
* **Clusters:** arriba a la izquierda se ubican los distintos clusters (grupos) en los que se agrupan los usuarios. Al cargar el grafo se ven todos los clusters en simultáneo. Clickeando sobre cualquiera de ellos la visualización se enfoca solamente sobre los nodos que le pertenecen, y al volver a clickearlo vuelven a mostrarse todos a la vez. Se puede armar cualquier combinación de clusters en la visualización, simplemente hay que clickear en los que queramos ver.

## Tabla

En simultáneo al grafo, es posible analizar la información a través de la tabla incluida debajo del grafo: todas las columnas se pueden ordenar de mayor a menor o alfabéticamente, y al hacer click sobre el nombre de un usuario se resaltarán en el grafo sus conexiones con otros y los tweets que explican esa relación (idéntico a clickear sobre la pelota en el grafo).

**Grupo42 Lab**

Links
* [Grafo Menciones](/reports/8N/2.html)
* [Grafo Clustering](/reports/8N/)

Referencias
* `[1]`: [http://es.wikipedia.org/wiki/Cluster](http://es.wikipedia.org/wiki/Cluster)
* `[2]`: [http://es.wikipedia.org/wiki/Grafo](http://es.wikipedia.org/wiki/Grafo) 

[3]: /zenzey/static/img/8N.png
