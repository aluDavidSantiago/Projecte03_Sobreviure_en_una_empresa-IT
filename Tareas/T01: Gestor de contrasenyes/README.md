# 🔐 Tasca 01 — Gestió Segura de Contrasenyes

## 📢 Context de la Crisi

⚠️ **Alerta!!** L'empresa EverPia ha estat víctima d'un atac cibernètic. La consultora on esteu de becaris ha patit una **fuita d’informació confidencial** relacionada amb un projecte en desenvolupament. Els ciberdelinqüents amenacen amb publicar-la si no es paga un rescat.

🔍 La investigació interna ha revelat que un **compte tècnic va ser compromès** a causa de l'ús d'una **contrasenya feble o reutilitzada**.

## 🛡️ Mesures Preses

La **Direcció Tècnica** ha creat un comitè de crisi i ha emès una directriu urgent:

> Tot el personal tècnic ha de començar a utilitzar un **gestor de contrasenyes validat** per garantir credencials úniques i robustes.

## 🧠 Objectiu de la Tasca

Se t'encarrega avaluar les opcions disponibles i crear la documentació necessària per formar l'equip tècnic.

---

## 📝 Fase 1: Informe Tècnic (`informe.md`)

### 📌 Contingut Obligatori

1. **Introducció i Justificació**
   - Riscos de contrasenyes febles o reutilitzades (atac de diccionari, credential stuffing, etc.).
   - Funció d’un gestor de contrasenyes per mitigar aquests riscos.

2. **🔍 Comparativa Tècnica**
   | Característica | Bitwarden (Online / Núvol) | KeePassX / KeePassXC (Offline / Escriptori) |
   |----------------|-----------------------------|---------------------------------------------|
   | Sincronització | ✅ Multi-dispositiu via núvol | ❌ Manual (portabilitat via arxiu) |
   | Seguretat      | 🔒 Xifratge end-to-end       | 🔐 Emmagatzematge local xifrat (KDBX) |
   | Accés          | 🌐 Web, mòbil, escriptori    | 💻 Només escriptori |
   | Cost           | 💸 Freemium (gratuït + premium) | 🆓 Totalment gratuït (open source) |

3. **⚖️ Avantatges i Inconvenients**
   - Comparació entre models online vs offline en termes de seguretat, usabilitat i continuïtat del negoci.

4. **✅ Recomanació Final**
   - Elecció de l’eina més adequada per al personal tècnic.
   - Justificació tècnica de la decisió.

---

## 📘 Fase 2: Guia d’Ús Tècnica (`guia.md`)

### 📌 Contingut Obligatori

1. **🛠️ Instal·lació i Configuració Inicial**
   - Descàrrega i instal·lació de l’eina.
   - Creació de la base de dades principal o compte mestre.

2. **🔑 Generació de Contrasenyes Segures**
   - Ús del generador de contrasenyes.
   - Paràmetres: longitud, caràcters especials, etc.

3. **💾 Exemples d’Ús i Emplenament Automàtic**
   - Desar credencials d’un compte de correu electrònic.
   - Desar credencials d’una aplicació o servei web.
   - Ús de l’extensió del navegador per emplenar automàticament.

4. **🧭 Gestió de Còpies de Seguretat**
   - Com fer una còpia de seguretat (KDBX o exportació).
   - Recomanació: clau USB xifrada o emmagatzematge xifrat al núvol.

📸 Les imatges de la guia han d’estar dins una carpeta específica: `img/`, `pics/`, etc.

---

## 📂 Estructura del Repositori

- `projecte-3/`
  - `tasca01/`
    - `README.md` — Descripció de la tasca i enllaços als arxius
    - `informe.md` — Informe tècnic (Fase 1)
    - `guia.md` — Guia d'ús tècnica (Fase 2)
    - `img/` — Carpeta amb captures de pantalla per la guia
      - `captura1.png`
      - `captura2.png`
      - `...` — Altres imatges necessàries

---

## 📄 README.md

Aquest arxiu ha d’incloure:

- Descripció breu de la tasca.
- Enllaços als arxius `informe.md` i `guia.md`.

---

## 📚 Materials i Enllaços de Suport

- 🔗 [INCIBE: Contrasenyes segures](https://www.incibe.es/ciudadania/tematicas/contrasenas-seguras)  
- 🔗 [INCIBE: Gestió de contrasenyes segures](https://www.incibe.es/ciudadania/tematicas/contrasenas-seguras)  
- 🔗 [Pàgina oficial de Bitwarden](https://bitwarden.com/)  
- 🔗 [Pàgina oficial de KeePassXC](https://keepassxc.org/)  
- 🔗 [INCIBE: Gestors de contrasenyes — què són i com poden millorar la seguretat de les empreses](https://www.incibe.es/empresas/blog/gestores-de-contrasenas-que-son-y-como-pueden-mejorar-la-seguridad-de-las-empresas)
