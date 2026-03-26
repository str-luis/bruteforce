alphabet = "abcdefghijklmnopqrstuvwxyz"
contraseña = "mesa"
encontrada = False
intentos = 0

for a in alphabet:
    for b in alphabet:
        for c in alphabet:
            for d in alphabet:
                intento = a + b + c + d
                intentos += 1

                if intento == contraseña:
                    print("Contraseña encontrada:", intento)
                    print("Intentos:", intentos)
                    encontrada = True
                    break
            if encontrada:
                break
        if encontrada:
            break
    if encontrada:
        break

if not encontrada:
    print("No se encontró la contraseña usando el alfabeto")