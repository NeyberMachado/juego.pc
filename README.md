# Definimos la funcion opciones
def opciones(pregunta, opciones_lista):
    print(pregunta)
    for opcion in opciones_lista:
        print(opcion)
    while True: # Ejecutamos varias veces con while True
        respuesta = input("Elige una opción: ").strip() # respuesta es igual a la entrada del teclado
        if respuesta in opciones_lista: # si la respuesta esta en opciones
            return respuesta # entonces devuelve la respuesta
        else: # si no
            print("!Opción no válida¡. Intenta de nuevo.\n") # "imprime opcion no valida"


def historia():
    
    # Se ejecuta varias veces, se imprime la introducción y se presenta la primera tanda de elecciones
    while True:
        print("\n Te despiertas en una habitación oscura, con un ligero zumbido resonando en tus oídos.")
        print("Al abrir los ojos, te das cuenta de que estás en un laberinto.")
        print("Las paredes son altas y están cubiertas de enredaderas.")
        print("A tu alrededor, hay tres caminos que se bifurcan, cada uno marcado con un símbolo diferente:\n")

        eleccion_1 = opciones(
            "¿Qué camino eliges?",
            ["A - El Camino de la Sabiduría (un libro abierto)",
             "B - El Camino del Valor (una espada brillante)",
             "C - El Camino del Engaño (una máscara sonriente)"]
        )
        # si la eleccion es A entonces imprime: y continuamos con las elecciones
        if eleccion_1 == "A - El Camino de la Sabiduría (un libro abierto)":
            print("\n Decides seguir el camino del libro. A medida que avanzas, encuentras un anciano sentado en una roca, rodeado de libros.")
            print("mira y dice: \"Bienvenido, viajero. Aquí puedes aprender sobre el laberinto, pero debes responder a mi acertijo para continuar\".")
            print("\nTe presenta el acertijo: \"Soy ligero como una pluma, pero ni el hombre más fuerte puede sostenerme por mucho tiempo. ¿Qué soy?\"")

            SubEleccion_1 = opciones("Tienes tres opciones:", [
                "A. El aliento",
                "B. El tiempo",
                "C. La esperanza"
            ])

            if SubEleccion_1 == "A. El aliento":
                print("\n El anciano sonríe: \"Has acertado.\"")
                print("Te da un mapa del laberinto que te muestra la ruta más corta hacia la salida. Con su ayuda, logras escapar y ganar el juego.")
                break  # Fin del juego

            elif SubEleccion_1 == "B. El tiempo":
                print("\n El anciano frunce el ceño: \"Has fallado.\"")
                print("Una niebla oscura te envuelve y te lleva de regreso al inicio del laberinto, donde debes elegir nuevamente...\n")
                continue  # Reinicia el juego

            elif SubEleccion_1 == "C. La esperanza":
                print("\n El anciano frunce el ceño: \"Has fallado.\"")
                print("Una niebla oscura te envuelve y te lleva de regreso al inicio del laberinto, donde debes elegir nuevamente...\n")
                continue  # Reinicia el juego

        # si la la eleccion no es A y es B entonces imprime: y continuamos con las elecciones
        elif eleccion_1 == "B - El Camino del Valor (una espada brillante)":
            print("\n Decides tomar el camino de la espada. Al avanzar, te encuentras con un dragón dormido en medio del camino. Tienes dos opciones:")

            SubEleccion_2 = opciones("¿Qué harás?", [
                "A. Intentar atravesar sigilosamente sin despertarlo.",
                "B. Desafiar al dragón y luchar con tu espada."
            ])

            if SubEleccion_2 == "A. Intentar atravesar sigilosamente sin despertarlo.":
                print("\n Con pasos silenciosos, logras pasar al otro lado.")
                print("Una puerta dorada se abre frente a ti. ¡Has escapado del laberinto! UwU")
                break  # Fin del juego

            elif SubEleccion_2 == "B. Desafiar al dragón y luchar con tu espada.":
                print("\n El dragón se despierta y lanza una llamarada hacia ti.")
                print("Aunque luchas valientemente, no logras vencerlo y caes derrotado, siendo transportado nuevamente al inicio del laberinto UnU...\n")
                continue  # Reinicia el juego

        # si la la eleccion no es A o B y es C entonces imprime: y continuamos con las elecciones
        elif eleccion_1 == "C - El Camino del Engaño (una máscara sonriente)":
            print("\n Decides seguir el camino de la máscara sonriente. Al avanzar, encuentras una sala llena de espejos distorsionados.")
            print("En el centro, hay un espejo especial que parece mostrar la verdad sobre ti mismo. Tienes dos opciones:")

            SubEleccion_3 = opciones("¿Qué decides hacer?", [
                "A. Mirarte en el espejo y aceptar lo que ves.",
                "B. Ignorar el espejo y seguir adelante."
            ])

            if SubEleccion_3 == "A. Mirarte en el espejo y aceptar lo que ves.":
                print("\n Ves tus miedos y debilidades, pero también tus fortalezas.")
                print("Al aceptar tu verdadero yo, el espejo se rompe y revela un pasaje secreto que te lleva a la salida del laberinto.")
                break  # Fin del juego

            elif SubEleccion_3 == "B. Ignorar el espejo y seguir adelante.":
                print("\n Te sientes perdido y desorientado en los espejos, atrapado por tus propios engaños.")
                print("La confusión te lleva de regreso al inicio del laberinto...\n")
                continue  # Reinicia el juego
            
            
def opciones(pregunta, opciones_lista):
    print(pregunta)
    letras_validas = {}
    
    for opcion in opciones_lista:
        print(opcion)
        letra = opcion.split(".")[0].split("-")[0].strip().lower()
        letras_validas[letra] = opcion
        letras_validas[opcion.strip().lower()] = opcion

    while True:
        respuesta = input("\nElige una opción: ").strip().lower()
        if respuesta in letras_validas:
            return letras_validas[respuesta]
        else:
            print("\n!Opción no válida¡. Intenta de nuevo.\n")

def historia():
    
    while True:
        print("\nTe despiertas en una habitación oscura, con un ligero zumbido resonando en tus oídos.")
        print("Al abrir los ojos, te das cuenta de que estás en un laberinto.")
        print("Las paredes son altas y están cubiertas de enredaderas.")
        print("A tu alrededor, hay tres caminos que se bifurcan, cada uno marcado con un símbolo diferente:\n")

        eleccion_1 = opciones(
            "¿Qué camino eliges?\n",
            ["A - El Camino de la Sabiduría (un libro abierto)",
             "B - El Camino del Valor (una espada brillante)",
             "C - El Camino del Engaño (una máscara sonriente)"]
        )

        if eleccion_1 == "A - El Camino de la Sabiduría (un libro abierto)":
            print("\nDecides seguir el camino del libro. A medida que avanzas, encuentras un anciano sentado en una roca, rodeado de libros.")
            print("mira y dice: \"Bienvenido, viajero. Aquí puedes aprender sobre el laberinto, pero debes responder a mi acertijo para continuar\".")
            print("\nTe presenta el acertijo: \"Soy ligero como una pluma, pero ni el hombre más fuerte puede sostenerme por mucho tiempo. ¿Qué soy?\"")

            SubEleccion_1 = opciones("Tienes tres opciones:\n", [
                "A. El aliento",
                "B. El tiempo",
                "C. La esperanza"
            ])

            if SubEleccion_1 == "A. El aliento":
                print("\nEl anciano sonríe: \"Has acertado.\"")
                print("Te da un mapa del laberinto que te muestra la ruta más corta hacia la salida. Con su ayuda, logras escapar y ganar el juego.")
                break

            elif SubEleccion_1 == "B. El tiempo":
                print("\nEl anciano frunce el ceño: \"Has fallado.\"")
                print("Una niebla oscura te envuelve y te lleva de regreso al inicio del laberinto, donde debes elegir nuevamente...\n")
                continue

            elif SubEleccion_1 == "C. La esperanza":
                print("\nEl anciano frunce el ceño: \"Has fallado.\"")
                print("Una niebla oscura te envuelve y te lleva de regreso al inicio del laberinto, donde debes elegir nuevamente...\n")
                continue

        elif eleccion_1 == "B - El Camino del Valor (una espada brillante)":
            print("\nDecides tomar el camino de la espada. Al avanzar, te encuentras con un dragón dormido en medio del camino. Tienes dos opciones:")

            SubEleccion_2 = opciones("¿Qué harás?\n", [
                "A. Intentar atravesar sigilosamente sin despertarlo.",
                "B. Desafiar al dragón y luchar con tu espada."
            ])

            if SubEleccion_2 == "A. Intentar atravesar sigilosamente sin despertarlo.":
                print("\nCon pasos silenciosos, logras pasar al otro lado.")
                print("Una puerta dorada se abre frente a ti. ¡Has escapado del laberinto! UwU")
                break

            elif SubEleccion_2 == "B. Desafiar al dragón y luchar con tu espada.":
                print("\nEl dragón se despierta y lanza una llamarada hacia ti.")
                print("Aunque luchas valientemente, no logras vencerlo y caes derrotado, siendo transportado nuevamente al inicio del laberinto UnU...\n")
                continue

        elif eleccion_1 == "C - El Camino del Engaño (una máscara sonriente)":
            print("\nDecides seguir el camino de la máscara sonriente. Al avanzar, encuentras una sala llena de espejos distorsionados.")
            print("En el centro, hay un espejo especial que parece mostrar la verdad sobre ti mismo. Tienes dos opciones:")

            SubEleccion_3 = opciones("¿Qué decides hacer?\n", [
                "A. Mirarte en el espejo y aceptar lo que ves.",
                "B. Ignorar el espejo y seguir adelante."
            ])

            if SubEleccion_3 == "A. Mirarte en el espejo y aceptar lo que ves.":
                print("\nVes tus miedos y debilidades, pero también tus fortalezas.")
                print("Al aceptar tu verdadero yo, el espejo se rompe y revela un pasaje secreto que te lleva a la salida del laberinto.")
                break

            elif SubEleccion_3 == "B. Ignorar el espejo y seguir adelante.":
                print("\nTe sientes perdido y desorientado en los espejos, atrapado por tus propios engaños.")
                print("La confusión te lleva de regreso al inicio del laberinto...\n")
                continue


def opciones(pregunta, opciones_lista):
    print(pregunta)
    letras_validas = {}
    
    for opcion in opciones_lista:
        print(opcion)
        letra = opcion.split(".")[0].split("-")[0].strip().lower()
        letras_validas[letra] = opcion
        letras_validas[opcion.strip().lower()] = opcion

    while True:
        respuesta = input("\nElige una opción: ").strip().lower()
        if respuesta in letras_validas:
            return letras_validas[respuesta]
        else:
            print("\n!Opción no válida¡. Intenta de nuevo.\n")

def historia():
    
    while True:
        print("\nTe despiertas en una habitación oscura, con un ligero zumbido resonando en tus oídos.")
        print("Al abrir los ojos, te das cuenta de que estás en un laberinto.")
        print("Las paredes son altas y están cubiertas de enredaderas.")
        print("A tu alrededor, hay cinco caminos que se bifurcan, cada uno marcado con un símbolo diferente:\n")

        eleccion_1 = opciones(
            "¿Qué camino eliges?\n",
            ["A - El Camino de la Sabiduría (un libro abierto)",
             "B - El Camino del Valor (una espada brillante)",
             "C - El Camino del Engaño (una máscara sonriente)",
             "D - El Camino de la Naturaleza (una hoja verde)",
             "E - El Camino del Misterio (un ojo que todo lo ve)"]
        )

        
        if eleccion_1 == "A - El Camino de la Sabiduría (un libro abierto)":
            print("\nDecides seguir el camino del libro. A medida que avanzas, encuentras un anciano sentado en una roca, rodeado de libros.")
            print("Él te dice: \"Bienvenido, viajero. Aquí puedes aprender sobre el laberinto, pero debes responder a mi acertijo para continuar\".")
            print("\nTe presenta el acertijo: \"Soy ligero como una pluma, pero ni el hombre más fuerte puede sostenerme por mucho tiempo. ¿Qué soy?\"")

            SubEleccion_1 = opciones("Elige tu respuesta:\n", [
                "A. El aliento",
                "B. El tiempo",
                "C. La esperanza",
                "D. La sombra",
                "E. El silencio"
            ])

            if SubEleccion_1 == "A. El aliento":
                print("\nEl anciano sonríe: \"Has acertado.\"")
                print("Te da un mapa del laberinto que te muestra la ruta más corta hacia la salida. ¡Escapas victorioso!")
                break

            elif SubEleccion_1 in ["B. El tiempo", "C. La esperanza", "D. La sombra"]:
                print("\nEl anciano frunce el ceño: \"Has fallado.\"")
                print("Una niebla oscura te devuelve al inicio del laberinto...\n")
                continue

            elif SubEleccion_1 == "E. El silencio":
                print("\nEl anciano sonríe intrigado: \"Interesante interpretación, viajero. Aceptaré tu respuesta.\"")
                print("Te abre un portal secreto hacia la salida. ¡Has ganado por tu ingenio!")
                break

        
        elif eleccion_1 == "B - El Camino del Valor (una espada brillante)":
            print("\nDecides tomar el camino de la espada. Al avanzar, te encuentras con un dragón dormido en medio del camino.")

            SubEleccion_2 = opciones("¿Qué harás?\n", [
                "A. Intentar atravesar sigilosamente sin despertarlo.",
                "B. Desafiar al dragón y luchar con tu espada.",
                "C. Buscar un punto débil en el entorno.",
                "D. Ofrecerle comida para distraerlo.",
                "E. Cantarle una canción para calmarlo."
            ])

            if SubEleccion_2 == "A. Intentar atravesar sigilosamente sin despertarlo.":
                print("\nCon pasos silenciosos, logras pasar al otro lado.")
                print("Una puerta dorada se abre frente a ti. ¡Has escapado del laberinto!")
                break

            elif SubEleccion_2 == "B. Desafiar al dragón y luchar con tu espada.":
                print("\nEl dragón despierta furioso y te reduce con fuego. Vuelves al inicio...")
                continue

            elif SubEleccion_2 == "C. Buscar un punto débil en el entorno.":
                print("\nDescubres un techo de rocas sueltas. Al empujarlas, caen sobre el dragón y lo inmovilizan. ¡Escapas triunfante!")
                break

            elif SubEleccion_2 == "D. Ofrecerle comida para distraerlo.":
                print("\nLe lanzas provisiones al dragón. Él las devora y se duerme más profundamente. Escapas en silencio.")
                break

            elif SubEleccion_2 == "E. Cantarle una canción para calmarlo.":
                print("\nTu voz lo arrulla, pero el dragón se despierta confundido y te atrapa. Vuelves al inicio...")
                continue

        
        elif eleccion_1 == "C - El Camino del Engaño (una máscara sonriente)":
            print("\nDecides seguir el camino de la máscara. Encuentras una sala llena de espejos distorsionados.")
            print("En el centro, hay un espejo especial que parece mostrar la verdad sobre ti mismo.")

            SubEleccion_3 = opciones("¿Qué decides hacer?\n", [
                "A. Mirarte en el espejo y aceptar lo que ves.",
                "B. Ignorar el espejo y seguir adelante.",
                "C. Romper todos los espejos.",
                "D. Tocar el espejo central.",
                "E. Dar la espalda y cerrar los ojos."
            ])

            if SubEleccion_3 == "A. Mirarte en el espejo y aceptar lo que ves.":
                print("\nAceptas tus miedos y fortalezas. El espejo se rompe y revela la salida.")
                break

            elif SubEleccion_3 == "B. Ignorar el espejo y seguir adelante.":
                print("\nTe pierdes en la confusión de los espejos y vuelves al inicio...")
                continue

            elif SubEleccion_3 == "C. Romper todos los espejos.":
                print("\nEl estruendo destruye la ilusión, y aparece un pasadizo secreto hacia la salida.")
                break

            elif SubEleccion_3 == "D. Tocar el espejo central.":
                print("\nEl espejo te absorbe y despiertas al inicio del laberinto.")
                continue

            elif SubEleccion_3 == "E. Dar la espalda y cerrar los ojos.":
                print("\nCuando los abres, ya no hay espejos. Frente a ti está la salida.")
                break

        
        elif eleccion_1 == "D - El Camino de la Naturaleza (una hoja verde)":
            print("\nAvanzas entre raíces y flores luminosas. Un árbol gigante habla: \"Viajero, debo ponerte a prueba.\"")

            SubEleccion_4 = opciones("¿Qué haces?\n", [
                "A. Escalar el árbol para observar el laberinto.",
                "B. Beber agua de un arroyo cercano.",
                "C. Hablar con los animales del lugar.",
                "D. Descansar bajo la sombra del árbol.",
                "E. Pedir ayuda directamente al árbol."
            ])

            if SubEleccion_4 == "A. Escalar el árbol para observar el laberinto.":
                print("\nDesde lo alto, ves la salida y bajas con el camino claro. ¡Has escapado!")
                break

            elif SubEleccion_4 == "B. Beber agua de un arroyo cercano.":
                print("\nEl agua estaba envenenada... despiertas en el inicio.")
                continue

            elif SubEleccion_4 == "C. Hablar con los animales del lugar.":
                print("\nEllos te guían hacia la salida escondida.")
                break

            elif SubEleccion_4 == "D. Descansar bajo la sombra del árbol.":
                print("\nTe duermes profundamente y al despertar vuelves al inicio.")
                continue

            elif SubEleccion_4 == "E. Pedir ayuda directamente al árbol.":
                print("\nEl árbol abre sus raíces y te muestra un túnel hacia la salida.")
                break

        
        elif eleccion_1 == "E - El Camino del Misterio (un ojo que todo lo ve)":
            print("\nEl pasillo es oscuro y se llena de símbolos brillantes. Una voz susurra: \"Debes elegir tu destino.\"")

            SubEleccion_5 = opciones("¿Qué eliges?\n", [
                "A. Seguir la luz azul.",
                "B. Seguir la luz roja.",
                "C. Seguir la luz dorada.",
                "D. Sentarte y esperar.",
                "E. Caminar en la oscuridad sin seguir luces."
            ])

            if SubEleccion_5 == "A. Seguir la luz azul.":
                print("\nLa luz azul te conduce a la salida. Has escapado con calma y sabiduría.")
                break

            elif SubEleccion_5 == "B. Seguir la luz roja.":
                print("\nLa luz roja era una trampa. Vuelves al inicio.")
                continue

            elif SubEleccion_5 == "C. Seguir la luz dorada.":
                print("\nLa luz dorada te eleva y sales del laberinto por un portal celestial.")
                break

            elif SubEleccion_5 == "D. Sentarte y esperar.":
                print("\nLa voz se desvanece y despiertas en el inicio.")
                continue

            elif SubEleccion_5 == "E. Caminar en la oscuridad sin seguir luces.":
                print("\nEncuentras la salida a ciegas, confiando en tu instinto. ¡Lo lograste!")
                break

historia()
