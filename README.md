import time

alphabet = "abcdefghijklmnopqrstuvwxyz"

def bruteforce(alp, password):
    inicial = time.time()
    char_times = []
    intentos = 0

    for a in alp:
        for b in alp:
            for c in alp:
                for d in alp:
                    intento = a + b + c + d
                    intentos += 1

                    if intento == password:
                        print("contraseña encontrada:", intento)
                        final = time.time()
                        char_times.append((intentos, final - inicial))
                        print(char_times)
                        return intentos, char_times

    print("NO se encontro la contraseña usando el alfabeto")
    return intentos, char_times

bruteforce(alphabet, "mesa")
bruteforce(alphabet, "casa")
bruteforce(alphabet, "luna")