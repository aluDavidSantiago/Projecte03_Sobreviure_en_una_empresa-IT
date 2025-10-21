# Informe Técnico — Fase 1: Análisis y Justificación

## Introducción y Justificación

La empresa EverPia ha sido víctima de un ataque cibernético que ha provocado una fuga de información confidencial relacionada con un proyecto en fase de desarrollo. Los atacantes han accedido a datos sensibles y amenazan con publicarlos si no se paga un rescate.

La investigación interna ha revelado que uno de los accesos técnicos fue comprometido debido al uso de una contraseña débil o reutilizada. Este incidente pone de manifiesto un riesgo crítico para la seguridad de la empresa y evidencia la necesidad de adoptar medidas urgentes para proteger los sistemas y la información corporativa.

### Riesgos de contraseñas débiles o reutilizadas

- **Ataques de diccionario**: los atacantes prueban combinaciones comunes de palabras hasta encontrar una coincidencia válida.
- **Credential stuffing**: se utilizan credenciales filtradas de otros servicios para acceder a cuentas donde se han reutilizado las mismas contraseñas.
- **Phishing y técnicas de ingeniería social**: contraseñas simples son más susceptibles de ser deducidas o robadas mediante engaños.

### Función de un gestor de contraseñas

Un gestor de contraseñas permite:

- Generar contraseñas únicas, robustas y aleatorias para cada servicio.
- Almacenar credenciales de forma cifrada y segura.
- Acceder a las contraseñas desde múltiples dispositivos de forma rápida y controlada.
- Reducir la dependencia de la memoria humana y evitar la reutilización de contraseñas.

---

## Comparativa Técnica: Bitwarden vs KeePassXC

| Característica                  | Bitwarden (Online / Nube)                             | KeePassXC (Offline / Escritorio)                      |
|--------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| Sincronización                 | Sí, automática entre dispositivos vía nube            | No, requiere sincronización manual del archivo KDBX   |
| Modelo de seguridad            | Cifrado de extremo a extremo con clave maestra        | Cifrado local con clave maestra                       |
| Acceso multiplataforma         | Web, móvil, escritorio                                 | Escritorio (Windows, Linux, macOS)                    |
| Coste / modelo freemium        | Gratuito con opciones premium                         | Totalmente gratuito (software libre)                  |
| Código abierto                 | Sí                                                    | Sí                                                    |
| Facilidad de uso               | Interfaz moderna e intuitiva                          | Interfaz técnica y menos amigable para usuarios nuevos|

---

## Ventajas e Inconvenientes

### Bitwarden (Online)

**Ventajas:**

- Sincronización automática entre dispositivos.
- Acceso desde cualquier lugar con conexión a Internet.
- Interfaz moderna y fácil de usar.
- Modelo freemium que cubre necesidades básicas sin coste.

**Inconvenientes:**

- Dependencia de conexión a Internet.
- Riesgo potencial si el servicio en la nube es comprometido (aunque los datos están cifrados).

### KeePassXC (Offline)

**Ventajas:**

- Control total sobre los datos, sin depender de terceros.
- No requiere conexión a Internet.
- Ideal para entornos con políticas de seguridad estrictas.

**Inconvenientes:**

- Sincronización manual del archivo de contraseñas.
- Interfaz menos intuitiva.
- Riesgo de pérdida de datos si no se realizan copias de seguridad periódicas.

---

## Recomendación Final

Tras analizar ambas opciones, se recomienda el uso de **Bitwarden** para el personal técnico de EverPia.

### Justificación:

- Permite una implementación rápida y escalable.
- Facilita la formación del personal gracias a su interfaz intuitiva.
- Ofrece sincronización segura entre dispositivos, lo cual es esencial para equipos que trabajan en remoto o con movilidad.
- El modelo freemium cubre las necesidades básicas sin coste adicional, con posibilidad de ampliar funcionalidades si es necesario.



