# Versjonskontroll
Intro til versjonskontroll
Har du kontroll på koden din? På innleveringer? På bacheloroppgaven?
I dette kurset får du en intro til prinsippene og bruken av versjonskontrollsystemet Git. 
Kurset gir også intro til ulike verktøy som gjør versjonskontroll enklere og kraftigere.
Etter å ha vært på dette kurset kan du mer om hvordan versjonskontroll bør gjøres og du er klar for å lage ditt første repository.


#### Hvorfor trenger vi versjonskontroll?
 + Lagre alle gamle versjoner, så man kan gå tilbake til en gammel versjon om noe blir ødelagt
 + Har det dukket opp en feil, når kom den?
 + Holde oversikt over prosjektet
 + Flere kan jobbe samtidig
 + Backup
#### Hva er det som trenger versjonskontroll?
+ Kode
+ Tekstfiler
#### Hva er git?
+ Lager av alle gamle versjoner
+ Eksternt repository på en server
+ Kan være lokalt eller hos en ekstern hosting
+ Et sentral lager med koden, lokal kopi du kan jobbe på
***

### Basic versjonskontroll
The name "git" was given by Linus Torvalds when he wrote the very
first version. He described the tool as "the stupid content tracker"
and the name as (depending on your mood):

 - random three-letter combination that is pronounceable, and not
   actually used by any common UNIX command.  The fact that it is a
   mispronunciation of "get" may or may not be relevant.
 - stupid. contemptible and despicable. simple. Take your pick from the
   dictionary of slang.
 - "global information tracker": you're in a good mood, and it actually
   works for you. Angels sing, and a light suddenly fills the room.
 - "goddamn idiotic truckload of sh*t": when it breaks


```
git pull 
```
+ Hente kopi av repositoryet fra en server
+ Gir det deg nyeste på serveren
 ---
```git
git push <REMOTENAME> <BRANCHNAME>
```
+ Sender dine endringer til serveren
+ Du må ha de siste endringene fra serveren for å få lov til å pushe
 
--- 
```
git commit -m "beskrivende tekst om committen"
```
+ Legger til en punkt i historien
+ Lagres bare i din lokale kopi frem til du pusher til serveren
+ Legger bare til endringer i filer som er sjekket inn i repositoryet
+ Bruke git status for å sjekke hva som kommer til å bli lagt til med commiten
+ Eller git diff for å se endringer
```
git add [file]
```
+ For å legge til en fil i versjonskontroll brukes Add
+ For å fjerne en fil i versjonskontroll brukes Remove
 
---
```
git branch [navn-på-ny-gren]
```
```
git checkout [navn-på-gren]
```
+ Lag en ny gren for å lage en ny versjon av repositoryet
+ Gjør det lettere å samarbeide
+ Gjør det lettere å holde kontroll på historien
+ Kan holde en gren fungerende under utvikling av nye funksjoner
 
---
```
git merge [gren]
```
+ Slå sammen grener til en
+ Gjør det mulig at flere har gjort endringer i samme fil, og begge endringene kan beholdes
+ Konflikter må løses, feks om to har endret samme linje koden
+ Beholder hele historien til begge grenene
+ Slår sammen til den grenen du har aktiv

[Cheatsheet](https://services.github.com/kit/downloads/github-git-cheat-sheet.pdf)

***

## Verktøy
#### Versjonskontrollsystem
+ [Git](https://git-scm.com/downloads)
+ [Mercurial](https://www.mercurial-scm.org/wiki/Download)
+ [SVN](https://subversion.apache.org/download.cgi)
+ [CVS](http://www.nongnu.org/cvs/)

#### Online repositories
+ [Github](https://github.com)
+ [Bitbucket](https://bitbucket.com)

#### GUI program
+ [TortoiseGit/HG](https://tortoisegit.org)
+ [SourceTree](https://www.sourcetreeapp.com)

***

## Workflow
#### Basic Versjonskontroll
En rett linje med historie. Bare en branch, alt til master. Greit nok for en person. CVS/SVN er mer enn nok.

#### Basic Git workflow
En master branch. Feature branches for utvikling. Mergeing skjer inn i master
når en feature er stabil. Merging skjer i branchen hvor det utvikles.

#### Produksjons Git workflow
Master er prod. Development skal til prod. Feature branches for hver feature. 
Ny branch fra feature for hver utviklingsoppgave. Merge skjer alltid ut til
branch det er gjort utvikling i. Pull request mot development. Kan trigge
automagiske tester eller manuell godkjenning for å sjekkes inn i development.


### Installer git
##### Linux
```
sudo yum install git-all
```
```
sudo apt-get install git-all
```
##### MacOS
```
git
```
##### Windows
[Git-scm.com]( http://git-scm.com/download/win)
***