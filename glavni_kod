ime_datoteke = input()

try:

    lista_za_j_sortiranje = []
    with open(ime_datoteke, 'a') as f:
        f.write('\n')
    with open(ime_datoteke, 'r') as f:
        for i in f:
            podela = i.strip().split(',')
            if (podela[2]).isnumeric() == True and (podela[3]).isnumeric() == True:
                lista_za_j_sortiranje.append(i)

    c = True
    lista_za_j_sortiranje.sort()
    with open("estates.txt", 'w') as s:
        s.truncate(0)
        for i in lista_za_j_sortiranje:
            s.write("%s" % i)
    lista_za_j_sortiranje = []
    kriterijumi = input()
    if kriterijumi == ',':
        with open(ime_datoteke, "r") as f, open('stats.txt', "w") as s:
            for linija in f:
                podela = linija.strip().split(',')
                if (podela[2]).isnumeric() == True and (podela[3]).isnumeric() == True:

                    with open(ime_datoteke, 'r') as f:
                        prazna1 = []
                        prazna2 = []

                        for linija in f:
                            podela = linija.strip().split(',')
                            sprat = int(podela[2])
                            broj_soba = int(podela[3])
                            naziv = podela[0]
                            kvadrat = float(podela[1])
                            cena = float(podela[-1])

                            prazna1.append(list(linija.split(',')))
                    prazna1.sort()
                    for i in range(len(prazna1) - 1):
                        for j in range(i + 1, len(prazna1)):
                            if prazna1[i][0] == prazna1[j][0]:
                                prazna2.append(prazna1[i][0])
                    broj_ponavljanja = []
                    prazna2 = list(set(prazna2))
                    prazna2.sort()
                    #print(prazna1)

                    #print(prazna2)

                    broj = 0
                    zbir = []
                    zbir1 = []
                    zbir_za_cene = []
                    zbir_za_kvadrate = []
                    prva_lista = []
                    druga_lista = []
                    treca_lista = []
                    cetvrta_lista = []
                    konacna_lista = []
                    kon_pro = []
                    brojack = 0
                    for i in range(len(prazna1)):
                        if len(prazna2) == i:
                            break
                        if prazna1[i][0] == prazna2[i]:
                            broj += 1
                            zbir_za_cene.append(float((prazna1[i][-1])))
                            zbir_za_kvadrate.append(float((prazna1[i][1])))
                            kon_pro.append((float(prazna1[i][-1]) / float(prazna1[i][1])))
                        for j in range(i + 1, len(prazna1)):
                            if prazna1[j][0] == prazna2[i]:
                                broj += 1
                                zbir_za_cene.append(float(prazna1[j][-1]))
                                zbir_za_kvadrate.append(float(prazna1[j][1]))
                                kon_pro.append((float(prazna1[j][-1]) / float(prazna1[j][1])))
                        prva_lista.append((prazna2[i]))
                        druga_lista.append(broj)
                        treca_lista.append(zbir_za_cene)
                        cetvrta_lista.append(zbir_za_kvadrate)
                        zbir1 = [(prazna2[i]), "{:.2f}".format(min(zbir_za_cene)), "{:.2f}".format(max(zbir_za_cene)),
                                 "{:.2f}".format(sum(kon_pro) / broj)]
                        konacna_lista.append(zbir1)
                        kon_pro = []
                        zbir_za_cene = []
                        zbir_za_kvadrate = []
                        broj = 0
                        zbir1 = []
                    konacna_lista1 = []
                    konacna_lista2 = []
                    mozda = []
                    # print(konacna_lista)
                    for i in prazna1:
                        if any(b == i[0] for b in prazna2):
                            prazna1.remove(i)

                    for i in prazna1:
                        if any(b == i[0] for b in prazna2):
                            prazna1.remove(i)

                    for i in prazna1:
                        if any(b == i[0] for b in prazna2):
                            prazna1.remove(i)

                    for i in prazna1:
                        if any(b == i[0] for b in prazna2):
                            prazna1.remove(i)

                    for i in prazna1:
                        if any(b == i[0] for b in prazna2):
                            prazna1.remove(i)

                    for i in prazna1:
                        if any(b == i[0] for b in prazna2):
                            prazna1.remove(i)

                    for i in prazna1:
                        if any(b == i[0] for b in prazna2):
                            prazna1.remove(i)

                    for i in prazna1:
                        if any(b == i[0] for b in prazna2):
                            prazna1.remove(i)

                    for i in prazna1:
                        mozda = [i[0], "{:.2f}".format(float(i[-1])), "{:.2f}".format(float(i[-1])),
                                 "{:.2f}".format(float(i[-1]) / float(i[1]))]

                        konacna_lista.append(mozda)
                    #print(konacna_lista)
                    if len(prazna2) != 0:

                        with open("stats.txt", 'w') as s:
                            for m in range(len(konacna_lista)):
                                # s.write('\n')
                                for i in konacna_lista[m]:
                                    if i == konacna_lista[m][-1]:

                                        s.write('%s' % i)

                                    else:

                                        s.write('%s ' % i)
                                s.write('\n')

    elif len(kriterijumi) >= 2:

        if kriterijumi[0] == ',' and int(kriterijumi[1:len(kriterijumi)]) > 0:

            kriterijum_broj_sobe = int(kriterijumi[1:len(kriterijumi)])
            with open(ime_datoteke, 'r') as f:
                prazna1 = []
                prazna2 = []

                for linija in f:
                    podela = linija.strip().split(',')
                    sprat = int(podela[2])
                    broj_soba = int(podela[3])
                    naziv = podela[0]
                    kvadrat = float(podela[1])
                    cena = float(podela[-1])

                    if kriterijum_broj_sobe == broj_soba:
                        prazna1.append(list(linija.split(',')))
            prazna1.sort()
            for i in range(len(prazna1) - 1):
                for j in range(i + 1, len(prazna1)):
                    if prazna1[i][0] == prazna1[j][0]:
                        prazna2.append(prazna1[i][0])
            broj_ponavljanja = []
            prazna2 = list(set(prazna2))
            prazna2.sort()
            broj = 0
            zbir = []
            zbir1 = []
            zbir_za_cene = []
            zbir_za_kvadrate = []
            prva_lista = []
            druga_lista = []
            treca_lista = []
            cetvrta_lista = []
            konacna_lista = []
            kon_pro = []
            for i in range(len(prazna1)):
                if len(prazna2) == i:
                    break
                if prazna1[i][0] == prazna2[i]:
                    broj += 1
                    zbir_za_cene.append(float((prazna1[i][-1])))
                    zbir_za_kvadrate.append(float((prazna1[i][1])))
                    kon_pro.append((float(prazna1[i][-1]) / float(prazna1[i][1])))
                for j in range(i + 1, len(prazna1)):
                    if prazna1[j][0] == prazna2[i]:
                        broj += 1
                        zbir_za_cene.append(float(prazna1[j][-1]))
                        zbir_za_kvadrate.append(float(prazna1[j][1]))
                        kon_pro.append((float(prazna1[j][-1]) / float(prazna1[j][1])))
                prva_lista.append((prazna2[i]))
                druga_lista.append(broj)
                treca_lista.append(zbir_za_cene)
                cetvrta_lista.append(zbir_za_kvadrate)
                zbir1 = [(prazna2[i]), "{:.2f}".format(min(zbir_za_cene)), "{:.2f}".format(max(zbir_za_cene)),
                         "{:.2f}".format(sum(kon_pro) / broj)]
                konacna_lista.append(zbir1)
                kon_pro = []
                zbir_za_cene = []
                zbir_za_kvadrate = []
                broj = 0
                zbir1 = []
            konacna_lista1 = []
            konacna_lista2 = []
            mozda = []

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                mozda = [i[0], "{:.2f}".format(float(i[-1])), "{:.2f}".format(float(i[-1])),
                         "{:.2f}".format(float(i[-1]) / float(i[1]))]

                konacna_lista.append(mozda)

            if len(prazna2) != 0:

                with open("stats.txt", 'w') as s:
                    for m in range(len(konacna_lista)):
                        # s.write('\n')
                        for i in konacna_lista[m]:
                            if i == konacna_lista[m][-1]:

                                s.write('%s' % i)

                            else:

                                s.write('%s ' % i)
                        s.write('\n')

        elif kriterijumi[-1] == ',' and int(kriterijumi[0:(len(kriterijumi) - 1)]) >= 0:

            kriterijum_sprat = int(kriterijumi[0:(len(kriterijumi) - 1)])
            # print('samo_sprat')
            with open('estates.txt', 'r') as f:
                prazna1 = []
                prazna2 = []

                for linija in f:
                    podela = linija.strip().split(',')
                    sprat = int(podela[2])
                    broj_soba = int(podela[3])
                    naziv = podela[0]
                    kvadrat = float(podela[1])
                    cena = float(podela[-1])

                    if kriterijum_sprat == sprat:
                        prazna1.append(list(linija.split(',')))
            prazna1.sort()
            for i in range(len(prazna1) - 1):
                for j in range(i + 1, len(prazna1)):
                    if prazna1[i][0] == prazna1[j][0]:
                        prazna2.append(prazna1[i][0])
            broj_ponavljanja = []
            prazna2 = list(set(prazna2))
            prazna2.sort()
            broj = 0
            zbir = []
            zbir1 = []
            zbir_za_cene = []
            zbir_za_kvadrate = []
            prva_lista = []
            druga_lista = []
            treca_lista = []
            cetvrta_lista = []
            konacna_lista = []
            kon_pro = []
            for i in range(len(prazna1)):
                if len(prazna2) == i:
                    break
                if prazna1[i][0] == prazna2[i]:
                    broj += 1
                    zbir_za_cene.append(float((prazna1[i][-1])))
                    zbir_za_kvadrate.append(float((prazna1[i][1])))
                    kon_pro.append((float(prazna1[i][-1]) / float(prazna1[i][1])))
                for j in range(i + 1, len(prazna1)):
                    if prazna1[j][0] == prazna2[i]:
                        broj += 1
                        zbir_za_cene.append(float(prazna1[j][-1]))
                        zbir_za_kvadrate.append(float(prazna1[j][1]))
                        kon_pro.append((float(prazna1[j][-1]) / float(prazna1[j][1])))
                prva_lista.append((prazna2[i]))
                druga_lista.append(broj)
                treca_lista.append(zbir_za_cene)
                cetvrta_lista.append(zbir_za_kvadrate)
                zbir1 = [(prazna2[i]), "{:.2f}".format(min(zbir_za_cene)), "{:.2f}".format(max(zbir_za_cene)),
                         "{:.2f}".format(sum(kon_pro) / broj)]

                konacna_lista.append(zbir1)
                kon_pro = []

                zbir_za_cene = []
                zbir_za_kvadrate = []
                broj = 0

                zbir1 = []

            konacna_lista1 = []
            konacna_lista2 = []
            mozda = []
            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)

            for i in prazna1:
                if any(b == i[0] for b in prazna2):
                    prazna1.remove(i)


            for i in prazna1:
                mozda = [i[0], "{:.2f}".format(float(i[-1])), "{:.2f}".format(float(i[-1])),
                         "{:.2f}".format(float(i[-1]) / float(i[1]))]

                konacna_lista.append(mozda)

            if len(prazna2) != 0:

                with open("stats.txt", 'w') as s:
                    for m in range(len(konacna_lista)):
                        # s.write('\n')
                        for i in konacna_lista[m]:
                            if i == konacna_lista[m][-1]:

                                s.write('%s' % i)

                            else:

                                s.write('%s ' % i)
                        s.write('\n')

        else:
            brojackk = 0
            for i in range(len(kriterijumi)):
                if kriterijumi[i] == ',':
                    try:
                        if int(kriterijumi[0:i]) >= 0 and int(kriterijumi[i + 1:(len(kriterijumi))]) > 0:

                            kriterijumi_sprat = int(kriterijumi[0:i])
                            kriterijum_broj_soba = int(kriterijumi[i + 1:(len(kriterijumi))])

                            broj_linija = 0

                            prazna1 = []
                            prazna2 = []
                            brojac = 0
                            prosecna_cena = 0
                            prosecna_cenas = 0
                            prosecna_cenak = 0
                            lista = []
                            lista_za_nazive = []
                            lista_za_cene = []
                            lista_za_kvadrata = []
                            konana = []

                            lista_za_j_sortiranje = []
                            with open(ime_datoteke, 'r') as f:
                                for i in f:
                                    podela = i.strip().split(',')
                                    if (podela[2]).isnumeric() == True and (podela[3]).isnumeric() == True:
                                        lista_za_j_sortiranje.append(i)

                            lista_za_j_sortiranje.sort()
                            with open(ime_datoteke, 'w') as s:
                                s.truncate(0)
                                for i in lista_za_j_sortiranje:
                                    s.write("%s" % i)

                            with open('estates.txt', 'r') as f:
                                for linija in f:
                                    podela = linija.strip().split(',')
                                    sprat = int(podela[2])
                                    broj_soba = int(podela[3])
                                    naziv = podela[0]
                                    kvadrat = float(podela[1])
                                    cena = float(podela[-1])
                                    broj_linija += 1

                                    if kriterijumi_sprat == sprat and kriterijum_broj_soba == broj_soba:
                                        prazna1.append(list(linija.split(',')))

                            for i in range(len(prazna1) - 1):
                                for j in range(i + 1, len(prazna1)):
                                    if prazna1[i][0] == prazna1[j][0]:
                                        prazna2.append(prazna1[i][0])
                            broj_ponavljanja = []
                            prazna2 = list(set(prazna2))
                            prazna2.sort()
                            pis1 = 0
                            pis2 = []

                            for i in range(len(prazna1) - 1):
                                prazna1[i][-1] = prazna1[i][-1][0:(len(prazna1[i][-1]) - 1)]

                            broj = 0
                            zbir = []
                            zbir1 = []
                            for i in range(len(prazna1) - 1):
                                if len(prazna2) == i:
                                    break
                                if prazna1[i][0] == prazna2[i]:
                                    broj += 1
                                for j in range(i + 1, len(prazna1)):
                                    if prazna1[j][0] == prazna2[i]:
                                        broj += 1
                                zbir1 = [(prazna2[i]), broj]
                                zbir.append(zbir1)
                                broj = 0
                            # print(prazna1)
                            # print(prazna2)
                            with open(ime_datoteke, 'r') as f, open('stats.txt', 'w') as s:
                                for linija in f:
                                    podela = linija.strip().split(',')
                                    sprat = int(podela[2])
                                    broj_soba = int(podela[3])
                                    naziv = podela[0]
                                    kvadrat = float(podela[1])
                                    cena = float(podela[-1])

                                    if kriterijumi_sprat == sprat and kriterijum_broj_soba == broj_soba:
                                        with open(ime_datoteke, 'r') as f1:
                                            for linija1 in f1:
                                                podela1 = linija1.strip().split(',')

                                                if podela1[0] == naziv and kriterijumi_sprat == int(
                                                        podela1[2]) and kriterijum_broj_soba == int(
                                                    podela1[3]):

                                                    if any(i == naziv for i in prazna2):
                                                        if len(prazna2) != 0:
                                                            broj = 0
                                                            zbir = []
                                                            zbir1 = []
                                                            zbir_za_cene = []
                                                            zbir_za_kvadrate = []
                                                            prva_lista = []
                                                            druga_lista = []
                                                            treca_lista = []
                                                            cetvrta_lista = []
                                                            konacna_lista = []
                                                            kon_pro = []
                                                            brojack = 0
                                                            for i in range(len(prazna1) - 1):

                                                                if len(prazna2) == i:
                                                                    break
                                                                if prazna1[i][0] == prazna2[i]:
                                                                    broj += 1
                                                                    zbir_za_cene.append(float((prazna1[i][-1])))
                                                                    zbir_za_kvadrate.append(float((prazna1[i][1])))
                                                                    kon_pro.append(
                                                                        float((prazna1[i][-1])) / float(
                                                                            (prazna1[i][1])))
                                                                for j in range(i + 1, len(prazna1)):
                                                                    if prazna1[j][0] == prazna2[i]:
                                                                        broj += 1
                                                                        zbir_za_cene.append(float(prazna1[j][-1]))
                                                                        zbir_za_kvadrate.append(float(prazna1[j][1]))
                                                                        kon_pro.append(float((prazna1[j][-1])) / float(
                                                                            (prazna1[j][1])))
                                                                prva_lista.append((prazna2[i]))
                                                                druga_lista.append(broj)
                                                                treca_lista.append(zbir_za_cene)
                                                                cetvrta_lista.append(zbir_za_kvadrate)
                                                                zbir = [(prazna2[i]),
                                                                        "{:.2f}".format(min(zbir_za_cene)),
                                                                        "{:.2f}".format(max(zbir_za_cene)),
                                                                        "{:.2f}".format(sum(kon_pro) / broj)]
                                                                konacna_lista.append(zbir)

                                                            zbir_za_cene = []
                                                            zbir_za_kvadrate = []
                                                            broj = 0
                                                            zbir = []
                                                            kon_pro = []






                                                    elif i != naziv:
                                                        lista = [naziv, "{:.2f}".format(cena), "{:.2f}".format(cena),
                                                                 "{:.2f}".format(cena / kvadrat)]
                                                        for i in lista:
                                                            if i == lista[-1]:
                                                                s.write('%s' % i)
                                                            else:
                                                                s.write('%s ' % i)
                                                        s.write('\n')

                                                else:
                                                    pass

                                    else:
                                        pass

                            with open("stats.txt", 'r+') as s:
                                for i in s:
                                    konana.append(i)
                                konana.sort()

                            y = []
                            for i in range(len(konana)):

                                if i == len(konana) - 1:
                                    y.append(konana[i][0:(len(konana[i]) - 1)])

                                else:
                                    y.append(konana[i])

                            if len(prazna2) != 0:

                                with open("stats.txt", 'w') as s:
                                    s.truncate(0)
                                    for i in y:
                                        s.write("%s" % i)

                                with open("stats.txt", 'a+') as s:
                                    for m in range(len(konacna_lista)):
                                        s.write('\n')
                                        for i in konacna_lista[m]:
                                            if i == konacna_lista[m][-1]:

                                                s.write('%s' % i)

                                            else:

                                                s.write('%s ' % i)
                                        s.write('\n')






                        elif brojackk < 1:
                            print('GRESKA', end='')
                            c = False
                            brojackk += 1

                    except ValueError:
                        print('GRESKA', end='')
                        c = False

    brojac = 0
    brojac2 = 0

    if c == True:
        lista_za_j_sortiranje = []
        with open("stats.txt", 'r') as f:
            for i in f:
                brojac += 1
                lista_za_j_sortiranje.append(i)

        lista_za_j_sortiranje.sort()
        if len(lista_za_j_sortiranje) > 0:
            lista_za_j_sortiranje[-1] = lista_za_j_sortiranje[-1][0:len(lista_za_j_sortiranje[-1]) - 1]
            with open("stats.txt", 'w') as s:
                s.truncate(0)

                for i in lista_za_j_sortiranje:
                    if brojac == brojac2:
                        s.write("%s" % i)
                    else:
                        s.write("%s" % i)
                        brojac2 += 1

            with open('stats.txt', 'r+') as f:
                lines = f.readlines()
                f.seek(0)
                f.writelines(line for line in lines if line.strip())
                f.truncate()



        else:
            pass



except IndexError:
    print('DAT_GRESKA', end='')

