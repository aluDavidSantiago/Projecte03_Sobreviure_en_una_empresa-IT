# 🖥️ Producte04: Publicación de Configuración DNS en GitHub

## 📝 Breve descripción

¡Bienvenidos a vuestra nueva tarea, consultores!

Como miembros del equipo de sistemas de **EverPia**, habéis superado el reto de configurar un **servidor de nombres (DNS)** como prueba de concepto para nuestro cliente **DigiCore**. Actualmente, el resultado de vuestro trabajo se encuentra en una **máquina virtual Ubuntu Server**.

El objetivo ahora es **publicar estas configuraciones en GitHub**, para que puedan ser replicadas fácilmente en cualquier servidor Linux sin necesidad de empezar desde cero. Bastará con descargar los archivos y reiniciar el servicio para tener el servidor operativo.

---

## 🔌 Fase 1: Preparación de la conectividad y extracción de archivos

### 🔧 Paso 1.1: Configuración de la interfaz Host-Only

- Añadir una **segunda interfaz de red** en modo **Host-Only** a la máquina virtual
- Activarla y verificar la **conectividad desde la máquina física**

### 🔐 Paso 1.2: Copia segura de archivos con SCP

Utilizar el protocolo **SCP** (Secure Copy Protocol), incluido con el servicio SSH, para transferir los archivos de configuración al PC físico.

📂 Archivos a copiar:

- `/etc/bind/named.conf.options`
- `/etc/bind/named.conf.local`
- Archivos de zonas en `/etc/bind/zones`

📌 Comando ejemplo:

```bash
scp usuario@ip_vm:/etc/bind/named.conf.options .

