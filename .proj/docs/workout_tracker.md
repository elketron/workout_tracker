# workout tracker

## dependencies
sqlite db
gui with kivy

## general capabilities
- generate workout
- ingeven hoe moeilijk de oefening was (1 - 10)
- tonen stats per exersice: in vorm van numerieke en visuele grafieken
- oefening toevoegen
- settings
- goals setten per oefening

AI gaat voor latere versies ik zie dit niet als iets dat ik kan toevoegen in 3 weken
optional: (for AI)
- ingeven wat je eet
- ingeven hoe lang je slaapt
- ingeven hoe je slaap was (1 - 10)
- ingeven hoe je je de dag erna voelt

## plan
einddatum 6/12

1. [ ] database design
2. [ ] ui design
3. [ ] adden oefeningen
4. [ ] ingeven hoe moeilijk een oefening was en saven
5. [ ] maken algoritme voor generen oefening
6. [ ] goals per oefening kunnen toevoegen
7. [ ] een stats pagina maken waar je bijde je beste per oefening kan zien en een grafiek kan bekijken

## database
exersice {
    naam, [PK]
    categorie, -> categorie table [1 - n]
    goal,
    reps,
    keer per week,
    gewichten -> gewichten table [1 - 1]
}

categorieen {
    naam, [PK]
    description
}

gewichten {
    id, [PK]
    datum,
    het gewicht,
    moeilijkheidsgraad,
    kon het afwerken
}

generator settings {
    hoeveel oefeningen,
    increase factor
}
