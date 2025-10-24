# 🧠 Auditoría DNS para DigiCore - Proyecto EverPia

Como miembros cada vez más integrados del equipo técnico de la consultora **EverPia**, tenéis ante vosotros un nuevo reto.

El cliente, **DigiCore**, una empresa de marketing digital, experimenta errores de conectividad en ciertas aplicaciones. Su equipo técnico sospecha que el origen podría estar en una **resolución de nombres (DNS)** incorrecta o lenta.

---

## 🎯 Objetivo del proyecto

Realizar una **auditoría teórica y práctica** del servicio DNS para:

- Formar al personal del cliente
- Ofrecer herramientas de diagnóstico rápidas y efectivas

---

## 📚 Fase teórica: Sesión formativa

Deberéis elaborar un **material formativo** para el personal de DigiCore. Para garantizar la calidad, vuestros directores técnicos han preparado sesiones previas para que dominéis los conceptos que luego explicaréis.

### 🧩 Conceptos clave a explicar

- **Jerarquía y estructura del DNS**  
  Árbol DNS: Root → TLDs → Segundo nivel

- **Proceso de resolución**  
  Consultas iterativas y recursivas  
  Servidor raíz (Root Server) y servidor autoritativo

- **Tipos de zonas**  
  Zona directa e inversa  
  Zona primaria y secundaria

- **Tipos de registros clave (Records)**  
  A, CNAME, MX, NS, SVR

- **Conceptos esenciales**  
  - Respuesta autoritativa  
  - TTL (Time To Live)  
  - SOA (Start of Authority)  
  - Reenviadores: condicionales e incondicionales  
  - Resolución local: protocolo mDNS

### 🎥 Actividad teórica

Preparar una **píldora formativa en vídeo** (10–15 minutos) que explique de forma clara y breve todos los conceptos anteriores.

---

## 🧪 Fase práctica: Diagnóstico DNS con CLI

Demostrar el uso de las principales herramientas de diagnóstico DNS en los sistemas operativos utilizados por DigiCore: **Linux/macOS y Windows**.

Para la demostración, se usará un equipo **Zorin OS** con dos interfaces:

- NAT
- Adaptador puente con IP configurada según indicaciones

### 🧰 Diagnóstico avanzado con `dig` (Linux/macOS)

1. **Consulta básica de registro A**  
   `dig xtec.cat A`  
   🔍 Analizar: IP de respuesta, TTL y servidor que responde

2. **Consulta de servidores de nombres (NS)**  
   `dig tecnocampus.cat NS`  
   🔍 Analizar: Servidores autoritativos del dominio

3. **Consulta detallada SOA**  
   `dig escolapia.cat SOA`  
   🔍 Analizar: Correo del administrador y número de serie

4. **Consulta de resolución inversa**  
   `dig -x 147.83.2.135`  
   🔍 Analizar: Información obtenida de los registros

---

### 🧰 Diagnóstico con `nslookup` (Multiplataforma)

Modo interactivo (`nslookup` sin argumentos) con las siguientes instrucciones:

- `set type=` → Tipo de consulta: A, AAA, MX, NS, SOA, TXT, ALL
- `server IP` → IP o nombre del servidor de nombres
- `exit` → Salir del modo interactivo

#### Comandas

1. **Consulta básica no autoritativa**  
   - `set type=A`  
   - Dominio: `tecnocampus.cat`  
   🔍 Analizar: ¿Por qué la respuesta no es autoritativa?

2. **Consulta autoritativa**  
   - `server IP` → IP del primer servidor de nombres obtenido antes  
   - `set type=A` → Dominio: `tecnocampus.cat`  
   🔍 Analizar: Diferencias respecto a la consulta anterior

---

## 🖥️ Resolución local

Comprobar el funcionamiento de la **resolución local**, útil en redes sin servidor DNS propio, evitando el uso de IPs para acceder a recursos.

---

## 📄 Actividad práctica

Crear un documento `guia.md` que incluya:

- Capturas de las 5 consultas anteriores
- Explicaciones detalladas de cada resultado

---

¡Buena suerte con la auditoría! DigiCore cuenta con vosotros para mejorar su infraestructura DNS 🚀🔧

