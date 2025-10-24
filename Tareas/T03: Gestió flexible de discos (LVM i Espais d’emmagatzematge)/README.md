# 🧠 Proyecto de Almacenamiento Seguro - EverPia

Una vez superada la fase de formación, estáis preparados para afrontar el reto de nuestros clientes. El prestigioso bufete de abogados **Garriga i Associats**, uno de los más reconocidos de la ciudad, ha solicitado los servicios de nuestra consultora.

Gestionan una gran cantidad de **información legal sensible**, por lo que la **integridad**, la **disponibilidad** (alta redundancia) y la **facilidad de gestión** del almacenamiento son aspectos críticos.

## 🚨 Requisitos del cliente

La dirección de Garriga i Associats ha expresado la necesidad urgente de **renovar sus sistemas de servidores** para garantizar:

- Protección frente a fallos de disco
- Escalabilidad sin interrupciones

## 🛠️ Encargo técnico

Como técnicos de **EverPia**, debéis diseñar y documentar dos soluciones de almacenamiento:

- Una para servidores **Linux**
- Otra para servidores **Windows**

Estas soluciones deben cumplir con los principios de **alta disponibilidad**, **redundancia** y **escalabilidad**. Como se trata de una **prueba de concepto**, trabajaréis con **máquinas virtuales** en lugar de servidores reales.

---

## 🐧 Parte Linux: LVM con Zorin OS

Se utilizará la distribución **Zorin OS** (o una alternativa compatible) para demostrar la utilidad de **LVM (Logical Volume Manager)**.

### 🔧 Requisitos de implementación

- **Configuración inicial**  
  Crear un grupo de volúmenes (VG) y un volumen lógico (LV) con dos discos simulados de 10 GB. El volumen debe estar formateado y montado automáticamente mediante `/etc/fstab`.

- **Alta disponibilidad**  
  Implementar un espejo (`lvm_mirror`) para proteger la información ante la falla de un disco.

- **Instantáneas (snapshots)**  
  - Añadir dos discos de 10 GB al grupo de volúmenes.
  - Crear un volumen (`lvm_dades`) con el primer disco, formatearlo y montarlo.
  - Añadir archivos (por ejemplo, imágenes de Internet).
  - Usar el segundo disco para crear un snapshot (`lv_snapshot`) y documentar cómo restaurarlo si el volumen original se daña.

- **Escalabilidad**  
  Ampliar el volumen `lv_dades` usando el espacio libre del grupo de volúmenes.

---

## 🪟 Parte Windows: Espacios de Almacenamiento (Storage Spaces)

Se utilizará **Windows 11** para demostrar las configuraciones posibles con **Storage Spaces**.

### 🔧 Requisitos de implementación

- **Configuración inicial**  
  Crear un pool de almacenamiento con tres discos simulados de 10 GB.

- **Estudio de configuraciones**  
  - **Resiliencia de espejo (Mirroring)**: Usar dos discos y comprobar la alta disponibilidad.
  - **Espejo triple**: Eliminar el espacio anterior y crear uno nuevo con los tres discos. Justificar sus ventajas frente al mirroring.
  - **Resiliencia de paridad (Parity)**: Explicar su eficiencia de espacio comparada con el espejo. Añadir discos de 10 GB según sea necesario.

- **Demostración de gestión**  
  Mostrar cómo se visualiza el estado de los discos y del pool desde la consola de gestión de Windows.

---

## 👥 Trabajo en equipo y entrega

- El trabajo se realizará en **grupos** divididos en dos equipos:
  - Equipo Linux → LVM
  - Equipo Windows → Storage Spaces

- Cada miembro preparará individualmente el guion de la tarea, investigando comandos y documentación.

- Las parejas realizarán su parte de la demostración.

- El grupo completo revisará la documentación y **cada miembro la subirá a su repositorio**.

### 📁 Estructura de entrega

- La documentación se presentará en formato **Markdown**.
- Se incluirán **imágenes**, **explicaciones**, etc.
- Todo se guardará en una carpeta llamada `tasca03`.
- El archivo `README.md` debe contener:
  - Descripción de la tarea
  - Enlaces a los dos documentos

📌 La nota será **conjunta** para todo el grupo, así que ¡organizad bien el trabajo y comunicad con claridad!

---

## 🧑‍💼 Presentación final

Posteriormente, deberéis presentar al cliente las **conclusiones** de vuestro trabajo en una **presentación conjunta**.

---

## 📎 Material de clase (disponible en Moodle)

- [LVM en Linux](https://docs.google.com/presentation/d/1EFSMfLQRM0wvxRFEvXLN0oaiBq3goWNQ/edit?usp=sharing&ouid=104728425662496836733&rtpof=true&sd=true)
- [Espacios de almacenamiento en Windows](https://docs.google.com/presentation/d/1Xi9atPzB6fmiLM0qmKP2PxBrixb-s-ZB/edit?usp=sharing&ouid=104728425662496836733&rtpof=true&sd=true)

---

¡Mucho éxito en este reto técnico! 💪📂

