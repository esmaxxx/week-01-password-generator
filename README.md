# week-01-password-generator
A simple Python password generator
# Password Generator

Een eenvoudig Python-programma dat willekeurige wachtwoorden genereert. De gebruiker kiest de minimale lengte en kan aangeven of het wachtwoord cijfers en speciale tekens moet bevatten.

## Functionaliteiten

- Genereert een willekeurig wachtwoord.
- Vraagt om een minimale lengte.
- Laat de gebruiker kiezen of cijfers gebruikt moeten worden.
- Laat de gebruiker kiezen of speciale tekens gebruikt moeten worden.
- Controleert dat het wachtwoord lang genoeg is en voldoet aan de gekozen voorwaarden.

## Benodigdheden

- Python 3

Voor dit project zijn geen extra packages nodig. De gebruikte modules `random` en `string` zijn standaardonderdelen van Python.

## Installatie

1. Download of clone dit project.
2. Open de projectmap in VS Code of de Terminal.
3. Controleer of Python 3 is geïnstalleerd:

```bash
python3 --version
```

## Programma uitvoeren

Open de Terminal in de projectmap en voer uit:

```bash
python3 password_genarotor.py
```

> Let op: de bestandsnaam bevat momenteel `genarotor`. Dit is niet erg zolang je dezelfde naam gebruikt in de Terminal. Je kunt de naam eventueel later verbeteren naar `password_generator.py`.

## Gebruik

Het programma stelt drie vragen:

```text
enter minimum length: 12
do you want numbers in your password? (yes/no)? yes
do you want special characters in your password? (yes/no)? yes
```

Daarna verschijnt een gegenereerd wachtwoord, bijvoorbeeld:

```text
The generated password is: f9@Jp!4zQa#L
```

Omdat het wachtwoord willekeurig is, is de uitvoer iedere keer anders.

## Voorbeeld van keuzes

| Keuze | Betekenis |
|---|---|
| Minimum length: `8` | Het wachtwoord heeft minimaal 8 tekens. |
| Numbers: `yes` | Het wachtwoord bevat minimaal één cijfer. |
| Special characters: `yes` | Het wachtwoord bevat minimaal één speciaal teken, zoals `!`, `@` of `#`. |
| Numbers: `no` | Cijfers worden niet gebruikt. |
| Special characters: `no` | Speciale tekens worden niet gebruikt. |

## Hoe het werkt

1. Het programma gebruikt `string.ascii_letters` voor hoofdletters en kleine letters.
2. Als cijfers gekozen zijn, voegt het `string.digits` toe aan de beschikbare tekens.
3. Als speciale tekens gekozen zijn, voegt het `string.punctuation` toe.
4. Met `random.choice()` wordt steeds één willekeurig teken gekozen.
5. De `while`-lus gaat door totdat het wachtwoord:
   - minimaal de gekozen lengte heeft;
   - een cijfer bevat, wanneer dat is gekozen;
   - een speciaal teken bevat, wanneer dat is gekozen.

## Projectstructuur

```text
week-01-password-generator/
├── password_genarotor.py
└── README.md
```

## Mogelijke uitbreidingen

- Alleen veilige speciale tekens gebruiken.
- De gebruiker laten kiezen of hoofdletters verplicht zijn.
- Controleren of de ingevoerde minimumlengte een positief getal is.
- `ja` en `nee` naast `yes` en `no` accepteren.
- Voor productiegebruik `secrets` gebruiken in plaats van `random`, omdat `secrets` beter geschikt is voor beveiligde wachtwoorden.


