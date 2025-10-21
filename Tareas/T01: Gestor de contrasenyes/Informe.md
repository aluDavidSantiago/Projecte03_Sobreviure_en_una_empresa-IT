# Informe tècnic — Fase 1: Anàlisi i justificació

## 1. Introducció

El present informe té com a objectiu justificar tècnicament la decisió de la Direcció Tècnica d’EverPia d’implantar un gestor de contrasenyes per a tot el personal tècnic. Aquesta mesura s’ha pres arran d’un incident de seguretat greu: un atac informàtic que ha provocat una fuita d’informació confidencial relacionada amb un projecte en desenvolupament. La investigació interna ha determinat que l’origen de la vulnerabilitat ha estat l’ús d’una contrasenya feble o reutilitzada en un compte tècnic.

Aquest fet posa de manifest la necessitat d’adoptar bones pràctiques en la gestió de credencials, especialment en entorns professionals on es treballa amb dades sensibles i sistemes crítics.

## 2. Riscos associats a contrasenyes febles o reutilitzades

L’ús de contrasenyes poc robustes o repetides en diversos serveis representa un risc crític per a la seguretat de qualsevol organització. A continuació es detallen alguns dels atacs més habituals que aprofiten aquesta debilitat:

- **Atacs de diccionari**: consisteixen a provar contrasenyes comunes o paraules del diccionari fins a trobar una coincidència.
- **Credential stuffing**: utilització de credencials filtrades d’altres serveis per accedir a comptes on s’han reutilitzat les mateixes dades d’accés.
- **Phishing i enginyeria social**: tècniques que busquen enganyar l’usuari per obtenir les seves credencials.

Aquest tipus d’atacs són especialment efectius quan els usuaris utilitzen contrasenyes senzilles, previsibles o repetides en diversos serveis.

## 3. Funció d’un gestor de contrasenyes

Un gestor de contrasenyes és una eina que permet generar, emmagatzemar i gestionar credencials d’accés de manera segura. Els avantatges principals són:

- Generació de contrasenyes úniques, llargues i complexes.
- Emmagatzematge xifrat de totes les credencials en una base de dades protegida per una contrasenya mestra.
- Accés ràpid i segur a les contrasenyes des de diferents dispositius.
- Reducció del risc de reutilització de contrasenyes i de filtracions per mala gestió manual.

L’ús d’un gestor de contrasenyes contribueix a millorar la seguretat global de l’organització i facilita el compliment de bones pràctiques en ciberseguretat.

## 4. Comparativa tècnica: Bitwarden vs KeePassXC

A continuació es presenta una comparativa entre dues solucions de gestió de contrasenyes: Bitwarden (basada en el núvol) i KeePassXC (basada en emmagatzematge local).

| Característica                | Bitwarden (Online / Núvol)                          | KeePassXC (Offline / Escriptori)                     |
|------------------------------|-----------------------------------------------------|------------------------------------------------------|
| Sincronització               | Sí, automàtica entre dispositius                    | No, sincronització manual de l’arxiu KDBX            |
| Model de seguretat           | Xifratge de punta a punta amb clau mestra           | Xifratge local amb clau mestra                       |
| Accés multiplataforma        | Web, mòbil i escriptori                             | Només escriptori (Windows, Linux, macOS)             |
| Cost / model freemium        | Gratuït amb opcions premium                         | Totalment gratuït (codi obert)                       |
| Codi obert                   | Sí                                                  | Sí                                                   |
| Facilitat d’ús               | Interfície moderna i intuïtiva                      | Interfície més tècnica, orientada a usuaris avançats |

## 5. Avantatges i inconvenients

### Bitwarden

**Avantatges:**
- Sincronització automàtica entre dispositius.
- Accés des de qualsevol lloc amb connexió a Internet.
- Interfície senzilla i fàcil d’utilitzar.
- Opcions de compartició segura entre usuaris.

**Inconvenients:**
- Dependència del núvol i de tercers.
- Necessita connexió a Internet per a la sincronització.

### KeePassXC

**Avantatges:**
- Control total sobre les dades (emmagatzematge local).
- No depèn de cap servidor extern.
- Ideal per a entorns amb polítiques de seguretat estrictes.

**Inconvenients:**
- Sincronització manual (pot generar errors o pèrdues si no es gestiona bé).
- Interfície menys intuïtiva per a usuaris no tècnics.

## 6. Recomanació

Tenint en compte les necessitats de l’equip tècnic d’EverPia, es recomana la implantació de **Bitwarden** com a gestor de contrasenyes corporatiu.

Els motius principals són:

- Facilita la gestió centralitzada i segura de credencials.
- Permet una adopció ràpida gràcies a la seva interfície intuïtiva.
- Ofereix sincronització entre dispositius, fet que és clau per a equips que treballen en remot o en mobilitat.
- El seu model freemium cobreix les funcionalitats essencials sense cost, amb opcions avançades disponibles si cal.

Aquesta solució representa un equilibri adequat entre seguretat, usabilitat i eficiència operativa.

## 7. Conclusions

La implantació d’un gestor de contrasenyes és una mesura imprescindible per reforçar la seguretat de l’organització i evitar incidents com el que ha patit EverPia. Bitwarden ofereix una solució robusta, escalable i fàcil d’adoptar per part del personal tècnic, i per tant es considera l’opció més adequada per a aquest entorn.

