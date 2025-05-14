from random import choice
import time

def continuar():
      input("\n... ")

def dicas():
    global dicasDisp
    print("\nGostaria de pedir uma dica à sua irmã? (s/n)")
    inputDica = input("\n... ").lower()
    if inputDica == 's':
         if dicasDisp > 0:
            dicasDisp -= 1
            print("\nSua dica foi usada.\n")
            print(dica)
         else:
            print("\nVocê já usou sua dica. Sua irmã não tem mais nada a dizer além de 'Boa sorte'.")
    else:
       print("\nVocê optou por não usar a dica.")


def vida(vidas):
    if vidas == 2:
        print("\n[■□□]\nIncorreto. O assassino te viu falando com o detetive. Seu nível de suspeita aumentou.")
    elif vidas == 1:
        print("\n[■■□]\nIncorreto. O assassino ouviu sua conversa e está vindo atrás de você.")
    elif vidas == 0:
        print("\n[■■■]\nApós tantas sugestões tolas, o detetive decide te ignorar. "
        "A noite chega sem que ninguém acredite em você, mas não chega sozinha. "
        "Você foi pêga pelo assassino e se junta à sua irmã.\n\nFim de jogo.")
        exit()
    return vidas

def quem(vidas, assassino):
      print("\n\nQuando amanhece sua mãe já não está mais lá e assim que ela se foi, tudo o que você fez foi ficar olhando "
      "pela janela. Um carro se aproxima, deve ser do detetive, vindo para as investigações. Você vai até ele para contar "
      "o que descobriu. \nVocê tem 3 chances.")
      while True:
            inputQuem = input("\nQuem é o assassino? ").upper()
            print("\n")
            if inputQuem == assassino:
                  print("\n\nResposta correta!")
                  if assassino == 'PAI':
                        print("\n\nO detetive te deixa com um assistente por segurança, e vai investigar sobre sua afirmação.\n\n"
                              "— Parece que você estava correta, Srta. Cattons. Infelizmente foi o seu pai. Ele descobriu que "
                              "vocês não eram filhas legítimas dele, mas sim do jardineiro, as encarou como uma vergonha e decidiu "
                              "se livrar disso. Ele fez embreagado no jardim, enquanto sua irmã observava as flores, e ela não "
                              "foi a única vítima. \nPelo visto seu pai teve algumas relações extraconjugais que deram frutos, "
                              "dos quais ele se livrava.\nSinto muito, garota. Eu normalmente não contaria isso para uma criança, "
                              "mas como foi você quem descobriu, achei que seria justo saber da verdade completa. \nQue agora "
                              "você e sua irmã tenham paz.")
                        continuar()
                        print("\n\nAo ver seu pai ser levado, você reflete sobre se algum dia vai experientar dessa paz, mas "
                        "sua irmã pelo menos, está livre.")
                        break
                  elif assassino == 'MÃE':
                        print("\n\nO detetive te deixa com um assistente por segurança, e vai investigar sobre sua afirmação.\n\n"
                              "— Parece que você estava correta, Srta. Cattons. Infelizmente foi a sua mãe, ela admitiu tudo. "
                              "Acontece que ela odiava crianças, pois as via como o motivo por não poder se separar do Sr. Cattons, "
                              "mas isso não se extendia para suas próprias filhas. Ela as amava, mas em um surto, drogada com a "
                              "cocaína que escondia em cápsulas de remédios para dormir, ao ver sua irmã na mansão não foi "
                              "capaz de reconhecer o que ela própria fazia. Ela se arrepende e condenará a si mesma pelo resto "
                              "de seus dias.\nSinto muito, garota. Eu normalmente não contaria isso para uma criança, mas como "
                              "foi você quem descobriu, achei que seria justo saber da verdade completa. \nQue agora você e sua "
                              "irmã tenham paz., e que saibam que apesar de tudo, foram amadas.")
                        continuar()
                        print("\n\nAo ver sua mãe ser levada, você reflete sobre se algum dia vai experientar dessa paz, mas "
                        "sua irmã pelo menos, está livre.")
                        break
                  elif assassino == 'COZINHEIRA':
                        print("\n\nO detetive te deixa com um assistente por segurança, e vai investigar sobre sua afirmação.\n\n"
                              "— Parece que você estava correta, Srta. Cattons. Foi de fato a cozinheira. Sinto muito, garota. "
                              "Eu normalmente não contaria isso para uma criança, mas como foi você quem descobriu, achei que "
                              "seria justo saber da verdade completa. \nAcontece que ela era uma canibal com um gosto especial "
                              "por carne de crianças. Esse tempo todo ela esteve matando-as para alimentação, mas parece que ao "
                              "ver sua irmã ela não resistiu à “carne nobre” como ela chama.")
                        continuar()
                        time.sleep(2)
                        print("\n\n...")
                        time.sleep(2)
                        print("\nEu...")
                        time.sleep(2)
                        print("Comi...")
                        time.sleep(2)
                        print("Minha irmã...?")
                        continuar()
                        print("\n\nEnquanto a cozinheira é levada até o carro de polícia ela ouve sua pergunta e começa a rir "
                              "maniacamente.\n\n— ", end='')
                        for i in range(25):
                              print("HA", end='')
                              time.sleep(0.21)
                        continuar()
                        print("\n\n— Menina tola, carne nobre eu não divido.\n\n— Que agoravocê e sua irmã tenham paz, Srta Cattons.\n"
                              "Diz o detetive ao entrar no carro.\nVendo a cozinheira ser levada, você reflete sobre se algum "
                              "dia vai experientar dessa paz, mas sua irmã pelo menos, está livre.")
                        break
                  elif assassino == 'JARDINEIRO':
                        print("\n\nO detetive te deixa com um assistente por segurança, e vai investigar sobre sua afirmação.\n\n"
                              "— Parece que você estava correta, Srta. Cattons. O assassino foi o jardineiro. Ele amava sua mãe "
                              "e acreditava que o motivo de não poderem ficar juntos eram vocês. Encontramos também o nome dele "
                              "em meio aos de outros fugitivos de um hospício não muito longe daqui. \nPelo visto ele matava "
                              "outras crianças para tentar saciar a vontade de matar as senhoritas, visto que isso não era o "
                              "que a Sra. Cattons queria, mas pelo visto seu último fio de sanidade se rompeu. \nEu normalmente "
                              "não contaria isso para uma criança, mas como foi você quem descobriu, achei que seria justo saber "
                              "da verdade completa. Que agora você e sua irmã tenham paz.")
                        break
                  elif assassino == 'BABÁ':
                        print("\n\nO detetive te deixa com um assistente por segurança, e vai investigar sobre sua afirmação.\n\n"
                              "— Parece que você estava correta, Srta. Cattons. A assassina foi a babá. Pelo visto ela faz parte "
                              "de um culto muito complicado, que envolve sangue infantil e incensos em seus rituais. Pelas minhas "
                              "pesquisas, estes têm horários muito rigorosos e acredito que ela ficou sem tempo para encontrar "
                              "outra criança. Apesar disso, ela ainda conseguiu armar para que sua mãe fosse a última vista com "
                              "sua irmã antes que a apagasse e levasse para uma sala escondida abaixo de um alçapão no jardim. "
                              "\nEu normalmente não contaria isso para uma criança, mas como foi você quem descobriu, achei que "
                              "seria justo saber da verdade completa. Que agora você e sua irmã tenham paz.")
                        break
                  elif assassino == 'TIO':
                        print("\n\nO detetive te deixa com um assistente por segurança, e vai investigar sobre sua afirmação.\n\n"
                              "— Parece que você estava correta, Srta. Cattons. O assassino foi seu tio. Parece que assim que "
                              "vocês nasceram ele adquiriu uma obcessão secreta anormal por gêmeos. Repetidas vezes fez pedidos "
                              "a universidades por material para estudos sobre, mas não foi concedido. Assim, ele os arranjou "
                              "por si mesmo, as outras vítimas todas possuíam irmãos próximos, mas vocês são as únicas gêmeas "
                              "na cidade e após anos de fracasso, ele ficou sem paciência. \nEu normalmente não contaria isso "
                              "para uma criança, mas como foi você quem descobriu, achei que seria justo saber da verdade completa. "
                              "Que agora você e sua irmã tenham paz.")
                        break
            else:
                  vidas -= 1
                  vidas = vida(vidas)
                  continue

def escolher_assassino():
    suspeitos = ["PAI", "MÃE", "COZINHEIRA", "JARDINEIRO", "BABÁ", "TIO"]
    assassino = choice(suspeitos)
    return assassino

dicasDisp = 1
vidas = 3
dica = 'p = F' # Exemplo de dica
assassino = escolher_assassino()


print("\nAlerta de gatilho! \nContém: Morte intencional; Consumo de droga ilícita; Canibalismo; Medo ou tensão; "
      "Violência física e psicológica; Violência doméstica.\n\nPressione o enter para continuar.")
continuar()
print("\n\nEm meados de 1800, em época de Revolução Industrial, você e sua gêmea são as crianças "
      "da poderosa família burguesa Cattons. A noite está fria e nublada, mas mesmo assim você está fora de casa, "
      "em um funeral, após uma grande tragédia ter ocorrido.")
continuar()
print("\n\nAssim que suas lágrimas finalmente cessam, envolta nos braços de sua babá, você ouve a conversa entre seus "
      "pais e um homem que você nunca havia visto.\n\n— Boa noite, Senhor e Senhora Cattons. Meus pêsames pela "
      "morte de uma de suas filhas, mas eu vim do Norte para investigar o que houve com ela. Precisam saber que ela "
      "não é a primeira porém, com sua colaboração, será a última. Digo isso, apesar de seu luto, pois tenho motivos "
      "para crer que o assassino está entre aqueles que vivem em sua mansão.\n\nVocê não ouve a resposta de seus pais.")
continuar()
print("\n\nAo voltar para dentro da mansão, no quarto que você dividia com sua irmã, você percebe que o ursinho que "
      "sempre a acompanhava estava no chão.\np: pegar o ursinho de sua irmã.\nq: receber ajuda ao longo do jogo."
      "\np --> q\nVocê pega o ursinho? (s/n)")
sn = input("\n... ").lower() # O "não/n" deve ser um else (ao invés de elif) para que mesmo que o usuário não digite
# nada, o jogo continue sem dar erro e reiniciar.
if sn == 's':
      print("\n\nAo pegar a pelúcia você sente um calafrio apesar da janela fechada e de seus agasalhos. Você anda "
            "até a cama de sua irmã para deixar a pelúcia, mas seus olhos parecem lhe pregar uma peça. Ela está ali? "
            "Sentada, como se nada tivesse acontecido? Após esfregar seus olhos e beliscar seu braço, você percebe "
            "que é real e sua irmã está tão surpresa quanto você.")
      continuar()
      print("\n\n— Irmã, você consegue me ver? Ah, que bom. Não sabe o quanto eu chorei, invisível. Ei, e pare de "
            "chorar você também. Isso é bom! Você me vê!\n\nVocê pergunta o que houve, quem a matou? Quem seria capaz "
            "de fazer isso com alguém tão doce quanto ela? Sempre se comportou, sempre tão educada... Por que?")
      continuar()
      print("\n\n— Ah irmã, eu gostaria de saber, mas não é o caso. De repente algo acertou minha cabeça, eu apaguei e "
            "acordei assim, póstuma. O que foi que fiz? Por que mereci isso? Sempre me esforcei tanto para ser "
            "gentil, o que houve para me odiarem a esse ponto? Não estarei em paz até saber.\n\nVocê então decide que"
            " irá descobrir quem fez isso, e libertar sua irmã.")
      continuar()
      print("\n\nSua irmã pode te dar apenas 1 dica, use com sabedoria!")
      continuar()
else:
      print("\n\nVocê decide não movê-lo. Parece estranho mexer nas coisas dela agora. Ao encarar a pelúcia lá, "
            "jogada, você é tomada pela raiva. \nO que houve, quem a matou? Quem seria capaz de fazer isso com alguém "
            "tão doce quanto sua irmã? Sempre se comportou, sempre tão educada... Por que? Você não estará em paz até"
            " descobrir.")
      continuar()




if assassino == 'PAI':
      print("\n\nVocê sai do quarto para o corredor. Já daqui é possível ouvir a briga rotineira de seus pais, mas "
      "está diferente. Você se aproxima para observar pela fresta da porta.")
      continuar()
      print("\n\n— COMO OUSA VOCÊ ME TRAIR! VOCÊ É UMA VERGONHA, ONDE JÁ SE VIU UMA MULHER CASADA SAIR TÃO TARDE DA NOITE!\n\n"
            "Seu pai, um homem alto e gordo, grita como se sua mãe não estivesse bem à frente dele. Ela chora, mas não "
            "parece triste. Parece esgotada, e apesar de tão pequena e magra, enraivecida. Ela está em mais um de seus surtos.")
      continuar()
      print("\n\n— Fala como se não sempre fizesse o mesmo, meu marid-\n\nA fala dela é interrompida por um tapa que lhe "
            "é desferido no rosto, o anel que seu pai usa no mindinho direito claramente deixaria um hematoma escuro. ")
      continuar()
      print("\n\nAntes que você pudesse fazer qualquer coisa, sua babá, de estatura não muito diferente de sua mãe, lhe "
      "afasta de lá, a colocando de volta no quarto. \n\n— Pobre menina, tudo ficará bem. Os senhores só estão conversando "
      "sobre o jardineiro, não é nada demais.")
      continuar()
      print("\n\nVocê espera a babá sair pela porta, mas antes que pudesse fazer o mesmo, escuta sussurros. Você "
            "identifica as vozes como da babá e do jardineiro, um homem magro como um palito, porém alto e imponente."
            "\n\n— Esse bastardo está me enlouquecendo! Odeio como ele a trata. Eu faria qualquer coisa, me livraria de "
            "qualquer empecilho por ela. Se ao menos ela não tivesse engravidado dele...")
      continuar()
      print("\n\n— Isso é ousadia demais para um mero jardineiro! Não posso nem imaginar o que o Sr. Cattons faria se "
            "ouvisse tamanha insanidade.\n\n— Entregue-me e você desce ao quinto dos infernos junto comigo! Não pense "
            "que não sei do que faz debaixo daquele maldito alçapão no jardim.\n\n— Se eu for descoberta, perderei tudo."
            "\n\n— Então lhe sugiro o silêncio pois, apesar de tudo, você também não passa de uma mera babá.")
      continuar()
      dica = "\n\np: A babá pratica da religião dela lá.\nq: A babá pode usar aquela sala.\nr: Mamãe e papai sabem.\np ^(q <--> (~ r))"
      dicas()
      continuar()
      print("\n\nApós os passos se afastarem, sua tentativa de sair do quarto é novamente frustrada, dessa vez por seu "
            "tio, um médico fracassado de mesmo tamanho do jardineiro, de repente entrando.\n\n— Minha sobrinha! Sua "
            "cuidadora acabara de passar por mim no corredor, me dizendo que você não dorme, e que há muito não come. \n\n"
            "Essas parecem preocupações tão banais, que você constantemente se questiona se é a única em luto por sua irmã.")
      continuar()
      print("\n\n— Sabe, quando não sinto sono gosto de fazer caminhadas pela mansão...\n\nUma oportunidade! Você o "
            "pergunta se em alguma de suas caminhadas ele já viu algo suspeito relacionado à tragédia.\n\n— Suspeito? "
            "Hahaha! Essa é uma palavra muito forte, sobrinha. Mas não, nada 'suspeito' como diz. É o de sempre: seu pai "
            "gritando, sua mãe chorando, e sua irmã, que Deus a tenha, indo até a cozinha buscar água. Foi até engraçado "
            "quando vi seu pai indo também logo atrás! Tal pai tal filha, não é? Hahahahaha!")
      continuar()
      print("\n\nSeu tio finalmente se retira, e você vai em rumo à cozinha. Lá você encontra a cozinheira, que se assusta "
            "ao te ver, mas logo continua o que fazia. Você pergunta a ela sobre a fala de seu tio. \n\n— Não houve nada "
            "especialmente suspeito por aqui. Como sempre, sua irmã só entrou e bebeu água. Ah sim, ela também foi ao "
            "jardim depois, mas não vi nada além pois estava cuidando de uma panela. Ainda assim me lembro de ouvir passos "
            "pesados passando pela cozinha quando me virei...")
      continuar()
      print("\n\nNo jardim, você não encontra o jardineiro, apenas as flores preferidas de sua irmã completamente amassadas. "
            "Ao voltar para o corredor, o encontra ainda perto do quarto de seus pais, ouvindo a discussão. \nAo te ver ele "
            "vem até você, claramente irritado.\n\n— O que faz aqui a essa hora?\n\nVocê responde estar fazendo um passeio "
            "para trazer sono, mas que viu as flores amassadas lá fora.\n\n— Eu as encontrei já daquela forma, com uma "
            "garrava vazia de Whiskey jogada ao meio.")
      continuar()
      print("\n\nVocês são alarmados por seu pai saindo do quarto e gritando com vocês por bisbilhotarem. Você vai em "
            "direção ao seu quarto, passando pelo olhar mortal de seu pai, o choro de sua mãe, e o cheiro de álcool e "
            "spray para cabelos.")
      continuar()
      print("\n\nVocê então entra em seu quarto, e ouve seu pai, com a voz estranha, gritando algo para o jardineiro que "
            "você não consegue identificar. Só ouve o jardineiro dizendo para que ele não descontasse seu estresse em sua "
            "filha, para o qual ele responde “NÃO A CHAME DISSO!”")
      continuar()
      dica = "\n\np: O papai não bebe.\nq: O papai é agressivo.\n~ p --> q"
      dicas()
      continuar()
      print("\n\nVocê vai para a cama e se senta, se sentindo tonta com tudo isso. Após a gritaria acabar sua mãe entra "
            "para te ver, te conforta e você pega no sono junto a ela. ")
      continuar()
      print("\n\nVocê acorda com o som da porta abrindo, vê uma sombra alta e larga que não entra, e logo em seguida a "
            "porta se fecha, deixando para trás apenas o forte odor de bebida que se misturava com o de spray capilar de "
            "sua mãe. É impossível que você volte a dormir, assustada. Ficou claro que essa seria sua vez, e que por sorte "
            "você não estava sozinha. ")
      continuar()

      quem(vidas, assassino)


elif assassino == 'MÃE':
      print("\n\nVocê sai do quarto para o corredor. Já daqui é possível ouvir a briga rotineira de seus pais, mas "
            "está diferente. Você se aproxima para observar pela fresta da porta.")
      continuar()
      print("\n\n— COMO OUSA VOCÊ ME TRAIR! VOCÊ É UMA VERGONHA, ONDE JÁ SE VIU UMA MULHER CASADA SAIR TÃO TARDE DA NOITE!\n\n"
            "Seu pai, um homem alto e gordo, grita como se sua mãe não estivesse bem à frente dele. Ela chora, mas não "
            "parece triste. Parece esgotada, e apesar de tão pequena e magra, enraivecida. Ela está em mais um de seus surtos.")
      continuar()
      print("\n\n— Fala como se não sempre fizesse o mesmo, meu marid-\n\nA fala dela é interrompida por um tapa que lhe "
            "é desferido no rosto, o anel que seu pai usa no mindinho direito claramente deixaria um hematoma escuro. ")
      continuar()
      print("\n\nAntes que você pudesse fazer qualquer coisa, sua babá, de estatura não muito diferente de sua mãe, lhe "
            "afasta de lá, a colocando de volta no quarto. \n\n— Pobre menina, tudo ficará bem. Os senhores só estão conversando "
            "sobre o jardineiro, não é nada demais.")
      continuar()
      print("\n\nVocê espera a babá sair pela porta, mas antes que pudesse fazer o mesmo, escuta sussurros. Você "
            "identifica as vozes como da babá e do jardineiro, um homem magro como um palito, porém alto e imponente."
            "\n\n— Esse bastardo está me enlouquecendo! Odeio como ele a trata. Eu faria qualquer coisa, me livraria de "
            "qualquer empecilho por ela. Se ao menos ela não tivesse engravidado dele...")
      continuar()
      print("\n\n— Isso é ousadia demais para um mero jardineiro! Não posso nem imaginar o que o Sr. Cattons faria se "
            "ouvisse tamanha insanidade.\n\n— Entregue-me e você desce ao quinto dos infernos junto comigo! Não pense "
            "que não sei do que faz debaixo daquele maldito alçapão no jardim.\n\n— Se eu for descoberta, perderei tudo."
            "\n\n— Então lhe sugiro o silêncio pois, apesar de tudo, você também não passa de uma mera babá.")
      continuar()
      dica = "\n\np: A babá pratica da religião dela lá.\nq: A babá pode usar aquela sala.\nr: Mamãe e papai sabem.\np ^(q <--> (~ r))"
      dicas()
      continuar()
      print("\n\nApós os passos se afastarem, sua tentativa de sair do quarto é novamente frustrada, dessa vez por seu "
            "tio, um médico fracassado de mesmo tamanho do jardineiro, de repente entrando.\n\n— Minha sobrinha! Sua "
            "cuidadora acabara de passar por mim no corredor, me dizendo que você não dorme, e que há muito não come. \n\n"
            "Essas parecem preocupações tão banais, que você constantemente se questiona se  é a única em luto por sua irmã.")
      continuar()
      print("\n\n— Sabe, quando não sinto sono gosto de fazer caminhadas pela mansão...\n\nUma oportunidade! Você o "
            "pergunta se em alguma de suas caminhadas ele já viu algo suspeito relacionado à tragédia.\n\n— Suspeito? "
            "Hahaha! Essa é uma palavra muito forte, sobrinha. Mas não, nada 'suspeito' como diz. É o de sempre: seu pai "
            "gritando, sua mãe chorando, e sua irmã, que Deus a tenha, indo até a cozinha buscar água. Foi até engraçado "
            "quando vi minha cunhada indo também logo atrás! Tal mãe tal filha, não é? Hahahahaha!")
      continuar()
      print("\n\nSeu tio finalmente se retira, e você vai em rumo à cozinha. Lá você encontra a cozinheira, que se assusta "
            "ao te ver, mas logo continua o que fazia. Você pergunta a ela sobre a fala de seu tio. \n\n— Não houve nada "
            "especialmente suspeito por aqui. Como sempre, sua irmã só entrou e bebeu água. Ah sim, ela também foi ao "
            "jardim depois, mas só após ela ter saído que sua mãe entrou para tomar os comprimidos novos para dormir. Porém "
            "não vi nada além pois estava cuidando de uma panela.")
      continuar()
      print("\n\nNo jardim, você não encontra o jardineiro, apenas as flores preferidas de sua irmã completamente amassadas. "
            "Ao voltar para o corredor, o encontra ainda perto do quarto de seus pais, ouvindo a discussão. Ao te ver ele "
            "vem até você, claramente irritado.\n\n— O que faz aqui a essa hora?\n\nVocê responde estar fazendo um passeio "
            "para trazer sono, mas que viu as flores amassadas lá fora.\n\n— Eu as encontrei já daquela forma, com algumas "
            "cápsulas vazias jogadas ao meio.")
      continuar()
      print("\n\nVocês são alarmados por seu pai saindo do quarto e gritando com vocês por bisbilhotarem. Você vai em "
            "direção ao seu quarto, passando por sua mãe que desvia o olhar, chorosa.")
      continuar()
      dica = "\n\np: Mamãe pode se divorciar.\nq: Mamãe teve a gente.\nr: Mamãe gosta de crianças.\n(q --> (~ p)) --> (~ r)"
      dicas()
      continuar()
      print("\n\nVocê então entra em seu quarto, e ouve seu pai, com a voz estranha, gritando algo para o jardineiro que "
            "você não consegue identificar. Só ouve o jardineiro dizendo para que ele não descontasse seu estresse na "
            "esposa e filha, o que ele ignora, voltando a gritar com sua mãe  “ESSES REMÉDIOS CAROS SÃO TÃO INÚTEIS QUANTO "
            "VOCÊ!”")
      continuar()
      print("\n\nVocê vai para a cama e se deita, se sentindo tonta com tudo isso. Após a gritaria acabar sua mãe entra "
            "para te ver, mas te encontra fingindo dormir. “Sinto muito, sinto muito”, ela repete baixo entre soluços até "
            "cair no sono.")
      continuar()

      quem(vidas, assassino)

elif assassino == 'COZINHEIRA':
    print("\n\nVocê sai do quarto para o corredor. Já daqui é possível ouvir a briga rotineira de seus pais, mas "
          "está diferente. Você se aproxima para observar pela fresta da porta.")
    continuar()
    print(
        "\n\n— COMO OUSA VOCÊ ME TRAIR! VOCÊ É UMA VERGONHA, ONDE JÁ SE VIU UMA MULHER CASADA SAIR TÃO TARDE DA NOITE!\n\n"
        "Seu pai, um homem alto e gordo, grita como se sua mãe não estivesse bem à frente dele. Ela chora, mas não "
        "parece triste. Parece esgotada, e apesar de tão pequena e magra, enraivecida. Ela está em mais um de seus surtos.")
    continuar()
    print("\n\n— Fala como se não sempre fizesse o mesmo, meu marid-\n\nA fala dela é interrompida por um tapa que lhe "
          "é desferido no rosto, o anel que seu pai usa no mindinho direito claramente deixaria um hematoma escuro. ")
    continuar()
    print("\n\nAntes que você pudesse fazer qualquer coisa, sua babá, de estatura não muito diferente de sua mãe, lhe "
          "afasta de lá, a colocando de volta no quarto. \n\n— Pobre menina, tudo ficará bem. Há tempos que não come, "
          "por que não faz um lanchinho antes de dormir? A cozinheira faz tanta carne que sempre sobra!")
    continuar()
    print("\n\nApós negar, você espera a babá sair pela porta, mas antes que pudesse fazer o mesmo, escuta sussurros. "
          "Você identifica as vozes como da babá e do jardineiro, um homem magro como um palito, porém alto e imponente."
          "\n\n— Esse bastardo está me enlouquecendo! Odeio como ele a trata. Eu faria qualquer coisa, me livraria de "
          "qualquer empecilho por ela. Se ao menos ela não tivesse engravidado dele...")
    continuar()
    print("\n\nSão interrompidos por seu tio, um médico fracassado de mesmo tamanho do jardineiro, que passava. A babá "
          "comenta sobre como você não come nem dorme, e que teme que esteja doente. Ele responde que pode ser só uma "
          "intoxiação alimentar, ou simplesmente o luto.")
    continuar()
    dica = "\n\np: Você comeu demais noite passada.\nq: Talvez você esteja passando mal.\np --> q"
    dicas()
    continuar()
    print("\n\nSeu tio então adentra seu quarto sem aviso.\n\n— Minha sobrinha! Sua cuidadora acabara de passar por mim "
          "no corredor, me dizendo que você não dorme, e que há muito não come. \n\nEssas parecem preocupações tão banais, "
          "que você constantemente se questiona se é a única que se importava com sua irmã.")
    continuar()
    print("\n\n— Sabe, quando não sinto sono gosto de fazer caminhadas pela mansão...\n\nUma oportunidade! Você o "
          "pergunta se em alguma de suas caminhadas ele já viu algo suspeito relacionado à tragédia.\n\n— Suspeito? "
          "Hahaha! Essa é uma palavra muito forte, sobrinha. Mas não, nada 'suspeito' como diz. É o de sempre: seu pai "
          "gritando, sua mãe chorando, e sua irmã, que Deus a tenha, indo até a cozinha buscar água.")
    continuar()
    print("\n\nSeu tio finalmente se retira, e você vai em rumo à cozinha. Lá você encontra a cozinheira, que se assusta "
          "ao te ver, mas logo continua o que fazia. Você pergunta a ela sobre a fala de seu tio. \n\n— Não houve nada "
          "especialmente suspeito por aqui. Só vi sua irmã entrando e bebendo água, pois logo depois me ocupei com uma "
          "panela.")
    continuar()
    dica = "\n\np: A cozinheira tinha carne.\nq: A panela estava vazia.\nq --> (~ p)"
    dicas()
    continuar()
    print("\n\nVocê vai para o jardim e não encontra o jardineiro, apenas o forte cheiro de gordura da cozinha que sente-se "
          "daqui e que impregnou suas roupas. Ao voltar para o corredor, o encontra ainda perto do quarto de seus pais, "
          "ouvindo a discussão. \nAo te ver ele vem até você, claramente irritado.\n\n— O que faz aqui a essa hora?\n\n"
          "Você responde estar fazendo um passeio para trazer sono, e que viu as flores belíssimas lá fora. Ele diz ter "
          "ficado a noite passada inteira cuidando delas, e ao ser interrogado, que não havia visto mais nenguém no jardim.")
    continuar()
    print("\n\nVocês são alarmados por seu pai saindo do quarto e gritando com vocês por bisbilhotarem. Você vai em "
          "direção ao seu quarto, passando pelos murmúrios de seu pai.\n\n— Fede. Aquela desgraçada deve estar preparando "
          "para levar as sobras de novo.")
    continuar()
    print("\n\nVocê então entra em seu quarto, e ouve seu pai, com a voz estranha, gritando algo para o jardineiro que "
          "você não consegue identificar. Só ouve o jardineiro dizendo para ele que não tem porquê culpar a cozinheira, "
          "para o qual ele responde — Ela usa meu dinheiro para preparar uma carne que não como! Amanhã ela já não estará "
          "mais aqui.")
    continuar()
    print("\n\nVocê vai para a cama e se senta, se sentindo tonta com tudo isso. Após a gritaria acabar sua mãe entra "
          "para te ver, te conforta e você pega no sono junto a ela. ")
    continuar()
    print("\n\nVocê acorda com o som da porta abrindo, vê uma sombra baixa e larga que não entra, e logo em seguida a "
          "porta se fecha, deixando para trás o forte odor do qual você já estava enjoada. É impossível que você volte a "
          "dormir, assustada. Ficou claro que essa seria sua vez, e que por sorte você não estava sozinha. ")
    continuar()

    quem(vidas, assassino)


elif assassino == 'JARDINEIRO':
      print("\n\nVocê sai do quarto para o corredor. Já daqui é possível ouvir a briga rotineira de seus pais, mas "
            "está diferente. Você se aproxima para observar pela fresta da porta.")
      continuar()
      print("\n\n— COMO OUSA VOCÊ ME TRAIR! VOCÊ É UMA VERGONHA, ONDE JÁ SE VIU UMA MULHER CASADA SAIR TÃO TARDE DA NOITE!\n\n"
            "Seu pai, um homem alto e gordo, grita como se sua mãe não estivesse bem à frente dele. Ela chora, mas não "
            "parece triste. Parece esgotada, e apesar de tão pequena e magra, enraivecida. Ela está em mais um de seus surtos.")
      continuar()
      print("\n\n— Fala como se não sempre fizesse o mesmo, meu marid-\n\nA fala dela é interrompida por um tapa que lhe "
            "é desferido no rosto, o anel que seu pai usa no mindinho direito claramente deixaria um hematoma escuro. ")
      continuar()
      print("\n\nAntes que você pudesse fazer qualquer coisa, sua babá, de estatura não muito diferente de sua mãe, lhe "
            "afasta de lá, a colocando de volta no quarto. \n\n— Pobre menina, tudo ficará bem. Os senhores só estão conversando "
            "sobre o jardineiro, não é nada demais.")
      continuar()
      print("\n\nVocê espera a babá sair pela porta, mas antes que pudesse fazer o mesmo, escuta sussurros. Você "
            "identifica as vozes como da babá e do jardineiro, um homem magro como um palito, porém alto e imponente."
            "\n\n— Esse bastardo está me enlouquecendo! Odeio como ele a trata. Eu faria qualquer coisa, me livraria de "
            "qualquer empecilho por ela. Se ao menos ela não tivesse engravidado dele...")
      continuar()
      print("\n\n— Isso é ousadia demais para um mero jardineiro! Não posso nem imaginar o que o Sr. Cattons faria se "
            "ouvisse tamanha insanidade.\n\n— Entregue-me e você desce ao quinto dos infernos junto comigo! Não pense "
            "que não sei do que faz debaixo daquele maldito alçapão no jardim.\n\n— Se eu for descoberta, perderei tudo."
            "\n\n— Então lhe sugiro o silêncio pois, apesar de tudo, você também não passa de uma mera babá.")
      continuar()
      dica = "\n\np: A babá pratica da religião dela lá.\nq: A babá pode usar aquela sala.\nr: Mamãe e papai sabem.\np ^(q <--> (~ r))"
      dicas()
      continuar()
      print("\n\nApós os passos se afastarem, sua tentativa de sair do quarto é novamente frustrada, dessa vez por seu "
            "tio, um médico fracassado de mesmo tamanho do jardineiro, de repente entrando.\n\n— Minha sobrinha! Sua "
            "cuidadora acabara de passar por mim no corredor, me dizendo que você não dorme, e que há muito não come. \n\n"
            "Essas parecem preocupações tão banais, que você constantemente se questiona se é a única em luto por sua irmã.")
      continuar()
      print("\n\n— Sabe, quando não sinto sono gosto de fazer caminhadas pela mansão...\n\nUma oportunidade! Você o "
            "pergunta se em alguma de suas caminhadas ele já viu algo suspeito relacionado à tragédia.\n\n— Suspeito? "
            "Hahaha! Essa é uma palavra muito forte, sobrinha. Mas não, nada 'suspeito' como diz. É o de sempre: seu pai "
            "gritando, sua mãe chorando, e sua irmã, que Deus a tenha, indo até a cozinha buscar água. Foi até engraçado "
            "quando vi sua mãe indo também logo atrás! Tal mãe tal filha, não é? Hahahahaha!")
      continuar()
      print("\n\nSeu tio finalmente se retira, e você vai em rumo à cozinha. Lá você encontra a cozinheira, que se assusta "
            "ao te ver, mas logo continua o que fazia. Você pergunta a ela sobre a fala de seu tio. \n\n— Não houve nada "
            "especialmente suspeito por aqui. Como sempre, sua irmã só entrou e bebeu água, logo antes da Sra. Cattons. "
            "Acho que sua mãe ia ao jardim, mas quando viu sua irmã indo, desistiu e foi para o quarto.")
      continuar()
      dica = "\n\np: Eu fui para o jardim.\nq: O jardineiro não estava lá.\np ^ (~ q)"
      dicas()
      continuar()
      print("\n\nNo jardim, você não encontra o jardineiro, apenas as flores preferidas de sua irmã completamente amassadas. "
            "Ao voltar para o corredor, o encontra ainda perto do quarto de seus pais, ouvindo a discussão. \nAo te ver ele "
            "vem até você, claramente irritado.\n\n— O que faz aqui a essa hora?\n\nVocê responde estar fazendo um passeio "
            "para trazer sono, mas que viu as flores amassadas lá fora, e ele diz já ter as encontrado assim.")
      continuar()
      print("\n\nVocês são alarmados por seu pai saindo do quarto e gritando com vocês por bisbilhotarem. Você vai em "
            "direção ao seu quarto, passando pelo olhar mortal de seu pai para você, e do jardineiro para ele, ao ver sua "
            "mãe chorosa.")
      continuar()
      print("\n\nVocê então entra em seu quarto, e ouve seu pai, com a voz estranha, gritando algo para o jardineiro que "
            "você não consegue identificar. Só ouve o jardineiro dizendo para que ele não descontasse seu estresse em sua "
            "filha, para o qual ele responde “NÃO A CHAME DISSO!”, o confundindo. Você espia pela fechadura e assiste os "
            "olhos do jardineiro se arregalarem e olharem para sua mãe, como se tivesse percebido algo horrível.")
      continuar()
      print("\n\nVocê vai para a cama e se senta, se sentindo tonta com tudo isso. Após a gritaria acabar sua mãe entra "
            "para te ver, te conforta e você pega no sono junto a ela. ")
      continuar()
      print("\n\nVocê acorda com o som da porta abrindo, vê uma sombra alta e fina que apenas as observa em meio a murmúrios "
            "melancólicos, e logo em seguida a porta se fecha. É impossível que você volte a dormir, assustada. Ficou claro "
            "que essa seria sua vez, e que por sorte você não estava sozinha. ")
      continuar()

      quem(vidas, assassino)


elif assassino == 'BABÁ':
      print("\n\nVocê sai do quarto para o corredor. Já daqui é possível ouvir a briga rotineira de seus pais, mas "
            "está diferente. Você se aproxima para observar pela fresta da porta.")
      continuar()
      print("\n\n— SUA INÚTIL, VAGABUNDA! FICA NA MANSÃO O DIA TODO E NEM É CAPAZ DE CUIDAR DE MERAS CRIANÇAS!\n\n"
            "Seu pai, um homem alto e gordo, grita como se sua mãe não estivesse bem à frente dele. Ela, tão pequena e magra, "
            "chora incontrolavelmente. E seu pai, ainda não satisfeito, a desfere um tapa no rosto, o anel que ele usa "
            "claramente deixaria um hematoma escuro. ")
      continuar()
      print("\n\nAntes que você pudesse fazer qualquer coisa, sua babá, de estatura não muito diferente de sua mãe, lhe "
            "afasta de lá, a colocando de volta no quarto. \n\n— Pobre menina, tudo ficará bem. O Sr. Cattons só está "
            "gritando porque sente muito a falta de sua irmã, e porque foi sua mãe quem a viu por último.")
      continuar()
      print("\n\nVocê espera a babá sair pela porta, mas antes que pudesse fazer o mesmo, escuta sussurros. Você "
            "identifica as vozes como da babá e do jardineiro, um homem magro como um palito, porém alto e imponente."
            "\n\n— Esse bastardo está me enlouquecendo! Odeio como ele a trata. Eu faria qualquer coisa, me livraria de "
            "qualquer empecilho por ela. Se ao menos ela não tivesse engravidado dele...")
      continuar()
      print("\n\n— Isso é ousadia demais para um mero jardineiro! Não posso nem imaginar o que o Sr. Cattons faria se "
            "ouvisse tamanha insanidade.\n\n— Entregue-me e você desce ao quinto dos infernos junto comigo! Não pense "
            "que não sei do que faz debaixo daquele maldito alçapão no jardim.\n\n— Se eu for descoberta, perderei tudo."
            "\n\n— Então lhe sugiro o silêncio pois, apesar de tudo, você também não passa de uma mera babá.")
      continuar()
      dica = "\n\np: A babá pratica da religião dela lá.\nq: A babá pode usar aquela sala.\nr: Mamãe e papai sabem.\np ^(q <--> (~ r))"
      dicas()
      continuar()
      print("\n\nApós os passos se afastarem, sua tentativa de sair do quarto é novamente frustrada, dessa vez por seu "
            "tio, um médico fracassado de mesmo tamanho do jardineiro, de repente entrando.\n\n— Minha sobrinha! Sua "
            "cuidadora acabara de passar por mim no corredor, me dizendo que você não dorme, e que há muito não come. \n\n"
            "Essas parecem preocupações tão banais, que você constantemente se questiona se é a única em luto por sua irmã.")
      continuar()
      print("\n\n— Sabe, quando não sinto sono gosto de fazer caminhadas pela mansão...\n\nUma oportunidade! Você o "
            "pergunta se em alguma de suas caminhadas ele já viu algo suspeito relacionado à tragédia.\n\n— Suspeito? "
            "Hahaha! Essa é uma palavra muito forte, sobrinha. Mas não, nada 'suspeito' como diz. É o de sempre: seu pai "
            "gritando e sua irmã, que Deus a tenha, indo até a cozinha buscar água. Foi até engraçado quando vi sua mãe "
            "indo também logo atrás, após falar com sua babá! Tal mãe tal filha, não é? Hahahahaha!")
      continuar()
      print("\n\nSeu tio finalmente se retira, e você vai em rumo à cozinha. Lá você encontra a cozinheira, que se assusta "
            "ao te ver, mas logo continua o que fazia. Você pergunta a ela sobre a fala de seu tio. \n\n— Não houve nada "
            "especialmente suspeito por aqui. Como sempre, sua irmã só entrou, bebeu água, e saiu para o jardim. Foi só "
            "depois que vi a Sra. Cattons entrando para tomar os remédios para dormir, e logo voltar para o quarto."
            "Não vi nada além pois estava cuidando de uma panela, mas ouvi passos leves passando pela cozinha...")
      continuar()
      print("\n\nNo jardim, você não encontra o jardineiro, apenas as flores preferidas de sua irmã completamente amassadas. "
            "Ao voltar para o corredor, o encontra ainda perto do quarto de seus pais, ouvindo a discussão. \nAo te ver ele "
            "vem até você, claramente irritado.\n\n— O que faz aqui a essa hora?\n\nVocê responde estar fazendo um passeio "
            "para trazer sono, mas que viu as flores amassadas lá fora.\n\n— Eu as encontrei já daquela forma, com um palito "
            "queimado jogado ao meio.")
      continuar()
      dica = "\n\np: O palito não estava queimado.\nq: Era incenso.\n(~ p) --> q"
      dicas()
      continuar()
      print("\n\nVocês são alarmados por seu pai saindo do quarto e gritando com vocês por bisbilhotarem. Você vai em "
            "direção ao seu quarto, passando pelo cheiro de incenso e spray para cabelos, e por sua mãe chorosa sendo consolada "
            "pela babá, que te observa atentamente enquanto você entra.")
      continuar()
      print("\n\nLá dentro você ouve seu pai discutir com o jardineiro, mas através da porta as palavras são abafadas e "
            "incompreensíveis. Só ouve a babá, que agora está mais perto da porta, timidamente pedindo para falarem baixo "
            "pois quer que você durma cedo hoje.")
      continuar()
      print("\n\nVocê vai para a cama e se senta, se sentindo tonta com tudo isso. Após a gritaria acabar sua mãe entra "
            "para te ver, te conforta e você pega no sono junto a ela. ")
      continuar()
      print("\n\nVocê acorda com o som da porta abrindo, vê uma sombra baixa e fina que não entra, e logo em seguida a "
            "porta se fecha, deixando para trás apenas o forte odor de incenso que se misturava com o de spray capilar de "
            "sua mãe. É impossível que você volte a dormir, assustada. Ficou claro que essa seria sua vez, e que por sorte "
            "você não estava sozinha.")
      continuar()

      quem(vidas, assassino)

elif assassino == 'TIO':
      print("\n\nVocê sai do quarto para o corredor. Já daqui é possível ouvir a briga rotineira de seus pais, mas "
            "está diferente. Você se aproxima para observar pela fresta da porta.")
      continuar()
      print("\n\n— SUA INÚTIL, VAGABUNDA! FICA NA MANSÃO O DIA TODO E NEM É CAPAZ DE CUIDAR DE MERAS CRIANÇAS! INÚTIL COMO "
            "MEU IRMÃO E AQUELE FRACASSO DE PESQUISA!\n\nSeu pai, um homem alto e gordo, grita como se sua mãe não estivesse "
            "bem à frente dele. Ela, tão pequena e magra, chora incontrolavelmente. E seu pai, ainda não satisfeito, a "
            "desfere um tapa no rosto, o anel que ele usa claramente deixaria um hematoma escuro. ")
      continuar()
      print("\n\nAntes que você pudesse fazer qualquer coisa, sua babá, de estatura não muito diferente de sua mãe, lhe "
            "afasta de lá, a colocando de volta no quarto. \n\n— Pobre menina, tudo ficará bem. Os senhores só estão conversando "
            "sobre seu tio, não é nada demais.")
      continuar()
      print("\n\nVocê espera a babá sair pela porta, mas antes que pudesse fazer o mesmo, escuta sussurros. Você "
            "identifica as vozes como da babá e do jardineiro, um homem magro como um palito, porém alto e imponente."
            "\n\n— Esse bastardo está me enlouquecendo! Odeio como ele a trata. Eu faria qualquer coisa, me livraria de "
            "qualquer empecilho por ela. Se ao menos ela não tivesse engravidado dele...")
      continuar()
      print("\n\n— Isso é ousadia demais para um mero jardineiro! Não posso nem imaginar o que o Sr. Cattons faria se "
            "ouvisse tamanha insanidade.\n\n— Entregue-me e você desce ao quinto dos infernos junto comigo! Não pense "
            "que não sei do que faz debaixo daquele maldito alçapão no jardim.\n\n— Se eu for descoberta, perderei tudo."
            "\n\n— Então lhe sugiro o silêncio pois, apesar de tudo, você também não passa de uma mera babá.")
      continuar()
      dica = "\n\np: A babá pratica da religião dela lá.\nq: A babá pode usar aquela sala.\nr: Mamãe e papai sabem.\np ^(q <--> (~ r))"
      dicas()
      continuar()
      print("\n\nApós os passos se afastarem, sua tentativa de sair do quarto é novamente frustrada, dessa vez por seu "
            "tio, um médico fracassado de mesmo tamanho do jardineiro, de repente entrando.\n\n— Minha sobrinha! Sua "
            "cuidadora acabara de passar por mim no corredor, me dizendo que você não dorme, e que há muito não come. \n\n"
            "Essas parecem preocupações tão banais, que você constantemente se questiona se é a única em luto por sua irmã.")
      continuar()
      print("\n\n— Sabe, quando não sinto sono gosto de fazer caminhadas pela mansão...\n\nUma oportunidade! Você o "
            "pergunta se em alguma de suas caminhadas ele já viu algo suspeito relacionado à tragédia.\n\n— Suspeito? "
            "Hahaha! Essa é uma palavra muito forte, sobrinha. Mas não, nada 'suspeito' como diz. É o de sempre: seu pai "
            "gritando, sua mãe chorando, e sua irmã, que Deus a tenha, indo até a cozinha buscar água. Foi até engraçado "
            "que de repente também senti sede! Tal tio tal sobrinha, não é? Hahahahaha!")
      continuar()
      dica = ("\n\np: Titio nos acha fascinantes.\nq: Nós não ficamos doentes ao mesmo tempo.\nr: Nós completamos as frases "
              "uma da outra\n(~ q v r) --> p")
      dicas()
      continuar()
      print("\n\nSeu tio finalmente se retira, e você vai em rumo à cozinha. Lá você encontra a cozinheira, que se assusta "
            "ao te ver, mas logo continua o que fazia. Você pergunta a ela sobre a fala de seu tio. \n\n— Não houve nada "
            "especialmente suspeito por aqui. Como sempre, sua irmã só entrou e bebeu água. Ah sim, ela também foi ao "
            "jardim depois, mas não vi nada além pois estava cuidando de uma panela. Ainda assim me lembro de ouvir passos "
            "leves passando pela cozinha quando me virei...")
      continuar()
      print("\n\nNo jardim, você não encontra o jardineiro, apenas as flores preferidas de sua irmã completamente amassadas. "
            "Ao voltar para o corredor, o encontra ainda perto do quarto de seus pais, ouvindo a discussão. \nAo te ver ele "
            "vem até você, claramente irritado.\n\n— O que faz aqui a essa hora?\n\nVocê responde estar fazendo um passeio "
            "para trazer sono, mas que viu as flores amassadas lá fora.\n\n— Eu as encontrei já daquela forma, com uma "
            "bituca de charuto jogada ao meio.")
      continuar()
      print("\n\nVocês são alarmados por seu pai saindo do quarto e gritando com vocês por bisbilhotarem. Você vai em "
            "direção ao seu quarto, passando pelo cheiro de charuto e spray para cabelos, e por sua mãe chorosa sendo consolada "
            "pelo cunhado, que te observa atentamente enquanto você entra.")
      continuar()
      print("\n\nVocê então entra em seu quarto, e ouve seu pai, com a voz estranha, gritando algo para o jardineiro que "
            "você não consegue identificar. Só ouve o jardineiro dizendo para que ele não descontasse seu estresse em sua "
            "família, para o qual ele responde “Minha família é composta por insetos incompetentes! Uma mulher que "
            "deixou a filha ser assassinada e um irmão que só tem suas pesquisas negadas!”")
      continuar()
      print("\n\nVocê vai para a cama e se senta, se sentindo tonta com tudo isso. Após a gritaria acabar sua mãe entra "
            "para te ver, te conforta e você pega no sono junto a ela. ")
      continuar()
      print("\n\nVocê acorda com o som da porta abrindo, vê uma sombra alta e fina que não entra, e logo em seguida a "
            "porta se fecha, deixando para trás apenas o forte odor de charuto que se misturava com o de spray capilar de "
            "sua mãe. É impossível que você volte a dormir, assustada. Ficou claro que essa seria sua vez, e que por sorte "
            "você não estava sozinha. ")
      continuar()

      quem(vidas, assassino)
