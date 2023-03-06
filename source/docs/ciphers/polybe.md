# Mono-alphabetic substitution: Polybe

[RootMe Challenge: Monoalphabetic substitution - Polybe](https://www.root-me.org/en/Challenges/Cryptanalysis/Monoalphabetic-substitution-Polybe): A strange person contact you after purchasing a parchment of weird origin ... He is counting on your quick wit to decrypt this message! You will need to deploy all your cryptanalyses faculties.

```text
for line in open('ch12.txt'):
    line = line.replace('b4', 'm')
    line = line.replace('a4', 'o')
    line = line.replace('a1', 't')
    line = line.replace('d3', 'd')
    line = line.replace('a3', 'e')
    line = line.replace('e1', 'p')
    line = line.replace('e3', 'a')
    line = line.replace('d1', 's')
    line = line.replace('c4', 'l')
    line = line.replace('e5', 'u')
    line = line.replace('b1', 'r')
    line = line.replace('d2', 'i')
    line = line.replace('d4', 'n')
    line = line.replace('c5', 'v')
    line = line.replace('b2', 'h')
    line = line.replace('c1', 'q')
    line = line.replace('c2', 'g')
    line = line.replace('e2', 'f')
    line = line.replace('c3', 'b')
    line = line.replace('b3', 'c')
    line = line.replace('b5', 'x')
    line = line.replace('d5', 'y')
    line = line.replace('a2', 'j')

    print(line)
```

Result:

```text
ces grands ouvrages compares au corps humain semblent

solides consideres selon les lois de cette nature qui detruit

[...]

 voila telles que je les ai pu rediger les reflexions d un

esprit des longtemps affaisse et appesanti par la disgrace si

elles vous semblent audessous de votre genie ou peu propres

a guerir vos douleurs songea5 combien l homme qu enlacent

et absorbent ses propres maux manque de loisir pour

consoler autrui et que les termes de notre idiome viennent

difficilement au banni entoure de barbares dont le langage

discordant choquant meme pour des barbares un peu civilises

fremit incessamment a son oreille

pass / mot de passe : cpaaourbxpjpgfo
```

