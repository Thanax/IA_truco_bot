# Truco bot
 
 Trabajo Práctico realizado para la materia IA de la UP, si se ejecuta el archivo "truco.py" dentro de la carpeta "truco" comenzará a jugar el truco_bot contra el CPU, está configurado al mejor de 15 por defecto pero cambiar eso es sólo un parámetro

# Recursos usados

 Créditos por la información de las tablas a IIAR: https://github.com/IAARhub/TrucoAnalytics

 Código original de truco en Python de Gonzalo Ciruelo Gonzalo Ciruelos 
 git: https://github.com/gciruelos/truco
 mail: <gonzalo.ciruelos@gmail.com>
 License: GPLv3

# truco_bot

Autor: Gonzalo Lucena
mail: <gonzaluc@hotmail.com>

# funciones agregadas del truco_bot
 
- get_cards_id(hand): recibe la mano del bot y convierte las cartas en números de id que pueda relacionar con la tabla "cartas_truco"
- show_hand_table(hand_ids): recibe una lista con los id de las cartas y muestra los datos estadísticos (probabilidad de obtener, probabilidad de derrotar) y ranking de cada una 
- envido_choice(hand): revisa la puntuación de envido total de la mano y si el bot es "pie" o "mano", y usa la tabla "envido_truco" para obtener la probabilidad de derrotar al oponente, retornando "si" o "no"
- truco_choice(hand_ids): calcula la probabilidad total de vencer entre las cartas restantes en mano y retorna "si" o "no"
- card_choice(hand_ids,previously_played): revisa la probabilidad de derrotar de cada carta y las compara individualmente con la carta jugada del oponente, eligiendo de ser posible la menor carta que igual derrote a la carta del oponente o, en caso de no poseer tal carta, la peor de la mano (para "quemarla"). En caso de que sea la primera carta a tirarse en esa mano simplemente elige la carta con mayor probabilidad de vencer a la carta que pueda tener el oponente  
