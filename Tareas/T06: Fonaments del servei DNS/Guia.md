#  Información DNS y consultas

## Dirección IP del dominio `xtec.cat`

- **IP de respuesta:** `83.247.151.214`
- **TTL (Time To Live):** 3557 segundos  
  Este valor indica cuánto tiempo puede mantenerse esta respuesta en caché antes de que sea necesario hacer una nueva consulta.
- **Servidor que respondió:** `127.0.0.53#53`  
  Es el servidor DNS local del sistema, que normalmente actúa como intermediario entre el equipo y los servidores DNS externos.

---

## Servidores de nombres para `tecnocampus.cat`

En la sección ANSWER SECTION del comando `dig`, aparecen los servidores autoritativos del dominio:

- `ns-1071.awsdns-05.org`
- `ns-130.awsdns-16.com`
- `ns-1689.awsdns-19.co.uk`
- `ns-535.awsdns-02.net`

Estos son los servidores que gestionan directamente las consultas DNS para `tecnocampus.cat`.

---

## Información del registro SOA

A partir del registro SOA (Start of Authority), se obtiene:

- **Servidor primario:** `dns1.nominalia.com`
- **Correo del administrador:** `root@dns1.nominalia.com`  
  *(En los registros SOA, el primer punto del campo de correo se reemplaza por una @)*
- **Número de serie:** `1761028965`

---

## Consulta inversa para la IP `147.83.2.135`

Se realizó una búsqueda inversa (reverse DNS lookup) para esta IP. En la sección ANSWER SECTION se encontraron varios registros PTR que vinculan la IP con dominios relacionados con la Universitat Politècnica de Catalunya (UPC):

- `barcelonatech-upc.eu`
- `upc.cat`
- `upc.edu`
- `www.upc.es`
- `masters.upc.edu`
- `edicioweb.produccio.upc.edu`
- `saladeprensa.upc.edu`
- `barcelonatech-upc.edu`

Cada uno de estos registros PTR asocia la IP con distintos servicios o subdominios de la UPC.

---

## ¿Por qué aparece “Non-authoritative answer”?

La respuesta se marcó como “Non-authoritative” porque fue resuelta por un servidor DNS local (en este caso, `127.0.0.53`) que probablemente tenía la información en caché. Es decir, no se consultó directamente a los servidores autoritativos del dominio.

- **Servidor autoritativo:** Tiene la información original y oficial del dominio.
- **Servidor no autoritativo:** Devuelve datos almacenados en caché, obtenidos previamente de otro servidor.

Aunque la información sea correcta, no proviene directamente del servidor que gestiona la zona DNS, sino de un intermediario.

---

## Comparación entre dos consultas

| Característica         | Consulta con 127.0.0.53 (local) | Consulta con 205.251.196.47 (autoritativo) |
|------------------------|----------------------------------|---------------------------------------------|
| **Servidor usado**     | Resolver local (`127.0.0.53`)   | Servidor autoritativo de AWS               |
| **Tipo de respuesta**  | Non-authoritative               | Autoritativa                               |
| **Direcciones IP**     | Mismas en ambos casos           | Mismas en ambos casos                      |
| **Diferencia clave**   | Fuente de la información        | Autoridad de la respuesta                  |

