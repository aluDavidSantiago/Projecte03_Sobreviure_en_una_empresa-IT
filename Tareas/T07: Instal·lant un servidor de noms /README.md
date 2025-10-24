# 🌐 Implantación de DNS Interno para DigiCore - Proyecto EverPia

Tras la exitosa experiencia formativa, nuestros clientes de **DigiCore** han quedado tan satisfechos que nos han encargado la **implantación desde cero** de sus servicios de DNS internos.

Actualmente, la agencia accede a sus servidores de desarrollo, bases de datos y herramientas internas mediante **direcciones IP**, lo cual genera varios problemas:

## ⚠️ Problemas detectados

- **Usabilidad deficiente**  
  Los empleados deben memorizar o buscar constantemente IPs complejas (ej. `192.168.10.25`).

- **Mantenimiento costoso**  
  Si un servidor cambia de IP, hay que actualizar manualmente la configuración en todos los equipos y aplicaciones.

- **Falta de profesionalidad**  
  En un entorno profesional, los servicios deben ser accesibles mediante **nombres de dominio amigables** (ej. `bbdd.digicore.lan`, `wiki.digicore.lan`).

---

## 🎯 Objetivo del proyecto

Implementar un **Sistema de Nombres de Dominio (DNS)** interno robusto usando **BIND9**, el estándar de facto en servidores Linux por su fiabilidad y flexibilidad.

---

## 🛠️ Misión técnica

Instalar y configurar un **servidor DNS primario (máster)** con BIND9 en un sistema Linux. Se deben crear:

- Una **Zona Directa** (Forward Zone)
- Una **Zona Inversa** (Reverse Zone)

El dominio de prueba será `digicore-XX.test`, donde `XX` es vuestro número de lista.

---

## 🧰 Preparación del entorno

- Configurar una máquina virtual **Ubuntu Server** con:
  - 4 GB de RAM
  - 20 GB de disco
  - Una interfaz en **adaptador puente**
  - Una segunda en **host-only**
- Instalar el paquete `bind9`
- Instalar el servicio `ssh` para exportar los archivos de configuración al repositorio de GitHub

---

## 🔧 Acciones a realizar

1. **Configuración de named.conf.options**
   - Permitir consultas recursivas desde la red local
   - Usar como reenviador la IP `8.8.8.8`
   - Mostrar captura de configuración
   - Reiniciar el servicio y comprobar su estado

2. **Configuración del cliente**
   - Usar la máquina Zorin con adaptador puente
   - Configurar el DNS con la IP del servidor
   - Verificar resolución a Internet (`dig google.com` o abrir navegador)

3. **Definición de zonas en named.conf.local**
   - Zona directa: `digicore-XX.test`
   - Zona inversa: red local utilizada en la prueba

4. **Creación de archivos de zona**
   - Carpeta `/etc/bind/zones`
   - Zona directa: copiar `db.local`
     - Configurar registros:
       - `SOA` con datos correctos
       - `NS` apuntando al servidor
       - `A` para `server` con IP del servidor
       - `A` para `dbserver` con IP del cliente
       - `CNAME` llamado `data` apuntando a `dbserver`
   - Zona inversa: copiar `db.127`
     - Configurar registros:
       - `SOA` y `NS` adecuados
       - `PTR` para `server` y `dbserver`

5. **Reiniciar servicio y comprobaciones**
   - Consultas directas e inversas desde el cliente

6. **Transferencia de zona**
   - Editar `named.conf.local` para permitir transferencia de zona directa
   - Configurar zona secundaria del dominio de un compañero
   - Forzar transferencia y comprobar funcionamiento desde el cliente

---

## 🧪 Evaluación del reto

Al finalizar, deberéis superar una **evaluación práctica**. Solo podréis usar como material de apoyo un **folio manuscrito** con vuestras anotaciones, que se entregará al finalizar la prueba.

---

¡Demostrad vuestra competencia técnica y llevad a DigiCore al siguiente nivel! 🚀🔧

