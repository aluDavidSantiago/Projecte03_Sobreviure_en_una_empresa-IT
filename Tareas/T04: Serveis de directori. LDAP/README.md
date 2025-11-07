# 🔐 Proyecto de Autenticación Centralizada - Innovatech

**Innovatech**, una start-up tecnológica emergente, está experimentando un rápido crecimiento y sufre un caos en la gestión de usuarios y accesos.

Actualmente, cada servicio interno (servidor de archivos, wiki de documentación, etc.) utiliza su propia base de datos de usuarios y contraseñas. Además, en los ordenadores cliente se usa autenticación local. Esto genera varios problemas críticos:

## ⚠️ Problemas detectados

- **Ineficiencia operativa**  
  Cada vez que se incorpora o se marcha un empleado, el equipo técnico debe crear o eliminar cuentas en múltiples sistemas.

- **Riesgo de seguridad**  
  Los usuarios tienden a reutilizar contraseñas entre servicios para evitar olvidarlas.

- **Falta de escalabilidad**  
  A medida que Innovatech añade nuevos servicios, el problema se vuelve insostenible.

---

## 🧩 Solución propuesta

El CEO de Innovatech ha contactado con **EverPia** para implementar una solución de **autenticación centralizada**.

La propuesta consiste en utilizar **OpenLDAP (Lightweight Directory Access Protocol)**, una solución robusta y de código abierto que se alinea con el espíritu de Innovatech, ya que todos los equipos usan **GNU/Linux**.

---

## 🎯 Misión del proyecto

Implementar el servicio **OpenLDAP** en un servidor Linux. Esto incluye:

- Instalación del servicio
- Configuración del dominio base
- Creación de la jerarquía de unidades organizativas
- Integración de usuarios y grupos para su uso en otros servicios de red
- Configuración de un equipo cliente para que utilice el directorio como sistema de autenticación

---

## 📄 Documentación técnica

Se ha redactado un documento con las especificaciones detalladas del trabajo. Está disponible en el **pliego de condiciones técnicas** y también en el **Moodle** de la asignatura.

---

## 📎 Material de clase (disponible en Moodle)

- [UD04.AA1 - Servicios de Directorio](https://docs.google.com/presentation/d/1x5i7JaRtzXtdNADtBevuX1HIMJkICo4O/edit?usp=drive_link&ouid=104728425662496836733&rtpof=true&sd=true)
- [UD04.AA2 - Instalación de OpenLDAP](https://docs.google.com/presentation/d/1k3qzGN8Zp8jQYH6sqNJeEfj5os0ziksD/edit?usp=drive_link&ouid=104728425662496836733&rtpof=true&sd=true)
- [UD04.AA3 - Configuración del Directorio](https://docs.google.com/presentation/d/1y4Av3fDSca9K3Oij-fQKJ6GsoaoKc0S-/edit?usp=drive_link&ouid=104728425662496836733&rtpof=true&sd=true)
- [UD04.AA5 - Agregar Cliente al Directorio](https://docs.google.com/presentation/d/1vlN5itS7RyiTEq4Do6xnBe-bPzMdl5nt/edit?usp=drive_link&ouid=104728425662496836733&rtpof=true&sd=true)

---

¡Manos a la obra! Este proyecto marcará un antes y un después en la infraestructura de Innovatech 🚀


# 📂 Documentació (T04)

## 📑 Índex de Documents

1. [Objecte de l'Encàrrec](Objecte%20de%20l%27Enc%C3%A0rrec.md)
2. [Requeriments d'Infraestructura Inicial](Requeriments%20d%27Infraestructura%20Inicial.md)
3. [Tasques d'Implementació i Configuració del Servidor LDAP](Tasques%20d%27Implementaci%C3%B3%20i%20Configuraci%C3%B3%20del%20Servidor%20LDAP.md)
4. [Integració de Client (Client Ubuntu Desktop)](Integraci%C3%B3%20de%20Client%20%28Client%20Ubuntu%20Desktop%29.md)

