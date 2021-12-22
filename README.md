# Saksfordelingssystem laget av Daniel

## Bytte eier på sak

### Overfør sak fra Person A til Person B:
	00001 > Person A >> Person B
	
### Sett sak til Person B:
    00001 > Person B
	
### Sett sak til Person B med kommentar:
	00001 # "Kommentar" -> Person B
	
## Legg til / Fjern bruker:

#### Legg til:
    00001 p+ Navn

#### Fjern:
    00001 p- Navn 

## Oppdatere saken
	
### Gi nytt navn på sak:
	00001 ! "Nytt navn"
	
### Gi nytt navn og kommenter saken:
	00001 ! "Nytt navn" > # "Kommentar"
	
### Legg sak i kø:
	00001 q+ Kønavn
	
### Fjern sak fra kø:
	00001 q- Kønavn
	
### Flytt fra kø til annen kø:
	00001 q "Kø 1" >> "Kø 2"
	
### Løs saken:
	00001 S
	
## Svar på saken

### Svar:
    00001 << "Svar"

## Prioriter saken
### Sett prioritet:
	00001 <LOW> (LOW / MEDIUM / HIGH)

## Eksempel
`28860 << "Vi skal sjekke brukeren din" > # "Kan være passord utgått?" > Person B > q+ "ITHjelp"`

Eksempelet sier:

`Svar sak 28860 med "Vi skal sjekke brukeren din" og legg til kommentar "Kan passord være utgått?",
gi sak til Person B og legg sak i køen "ITHjelp"`
