# it_sikkerhed_2026f

Dette et skole projekt til Zealand 


<img width="1446" height="682" alt="unittest 1" src="https://github.com/user-attachments/assets/8731d2c7-f8dc-437d-9c59-3e348e82cd7b" />
<img width="1561" height="611" alt="unittest 2" src="https://github.com/user-attachments/assets/80d2b107-9a65-4f46-91a1-303577aecc09" />
<img width="1547" height="702" alt="rettet kode" src="https://github.com/user-attachments/assets/fb05727c-da2f-49d0-bee9-c942a552cf88" />


Emne: Login til en webside
Nedenfor er de mest simple eksempler for hver testtype.

Ækvivalens klasser
- Inddata: Brugernavn og adgangskode.
- Gyldig klasse: korrekt brugernavn + korrekt adgangskode.
- Ugyldig klasse: forkert brugernavn.
- Ugyldig klasse: forkert adgangskode.

Grænseværdi test
- Regel: Adgangskode skal være mellem 8 og 12 tegn.
- 7 tegn (for kort) = fejl.
- 8 tegn (mindste gyldige) = ok.
- 12 tegn (største gyldige) = ok.
- 13 tegn (for langt) = fejl.

CRUD
- For brugerkonto i systemet:
- Create: Opret ny bruger.
- Read: Se brugerens profil.
- Update: Skift adgangskode.
- Delete: Slet bruger.
- List: Vis alle brugere.

Cycle process test
- Simpel login-flow:
- Start: Bruger åbner login-side.
- Indtastning: Bruger skriver brugernavn + adgangskode.
- Validering: System tjekker data.
- Resultat: Login ok eller fejlbesked.
- Slut: Bruger er logget ind eller prøver igen.
 
Test Pyramid
- Simpelt fokus:
- Unit tests: Tjek at kode validerer længden på adgangskode.
- Integration tests: Tjek at login-API kan kalde databasen.
- UI tests: Tjek at login-knappen virker i browseren.

Decision table test
- Regler:
- Hvis brugernavn er korrekt OG adgangskode er korrekt = login ok.
- Hvis brugernavn er korrekt OG adgangskode er forkert = fejl.
- Hvis brugernavn er forkert OG adgangskode er korrekt = fejl.
- Hvis brugernavn er forkert OG adgangskode er forkert = fejl.

10-2-2026 - Flat file

-Det er smart at bruge en flat_file_db, fordi den er nem at implementere, kræver ingen database-server og er god til små projekter og tests, hvor data bare skal gemmes simpelt og hurtigt.
<img width="805" height="583" alt="Skærmbillede 2026-02-10 114324" src="https://github.com/user-attachments/assets/092e6694-23b7-4b17-abcd-04c72922a2a5" />

-Hvis testen ikke består, er der risiko for at data ikke bliver gemt eller hentet korrekt, hvilket kan føre til datatab eller fejl i applikationen.
<img width="822" height="287" alt="Skærmbillede 2026-02-10 113430" src="https://github.com/user-attachments/assets/c9847eb9-f03a-42be-ac7c-c16899081ed8" />


Kryptering og Hashing

-Jeg kunne vælge mellem flere algoritmer som AES og hashing-algoritmer. Jeg valgte AES, fordi den er sikker og nem at bruge.
-Jeg krypterer data, når jeg gemmer følsomme oplysninger, så andre ikke kan læse dem.
-Jeg dekrypterer data, når programmet skal bruge oplysningerne igen.
-Jeg fjerner data fra hukommelsen, når det ikke længere er nødvendigt, for at gøre det mere sikkert.
-Ja, man bør også tage hensyn til sikker nøglehåndtering og adgangskontrol.
