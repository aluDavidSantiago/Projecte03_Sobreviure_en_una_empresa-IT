# Informe Técnico: Uso de Gestores de Contraseñas en Entornos Empresariales

## Justificación: ¿Por qué usar un gestor de contraseñas?

El uso de gestores de contraseñas es fundamental para garantizar la seguridad digital en entornos empresariales. Las principales razones incluyen:

- **Seguridad centralizada**: Protege credenciales mediante cifrado robusto (AES-256).
- **Reducción de errores humanos**: Evita contraseñas débiles, repetidas o almacenadas en texto plano.
- **Auditoría y control**: Permite gestionar accesos, compartir credenciales de forma segura y revocar permisos.
- **Cumplimiento normativo**: Facilita el cumplimiento de estándares como ISO 27001, GDPR, entre otros.

## Comparativa técnica: Bitwarden vs KeePassXC/KeePassX

| Característica                  | Bitwarden (Online)                                   | KeePassXC/KeePassX (Offline)                        |
|--------------------------------|------------------------------------------------------|-----------------------------------------------------|
| Modelo de uso                  | Basado en la nube, sincronización automática         | Local, sin sincronización por defecto               |
| Código abierto                 | Sí                                                   | Sí                                                  |
| Cifrado                        | AES-256 + PBKDF2 SHA-256                             | AES-256 + SHA-256                                   |
| Autenticación 2FA             | Sí (TOTP, Duo, FIDO2, etc.)                          | Limitada, depende de extensiones                    |
| Compatibilidad                | Windows, macOS, Linux, Android, iOS, navegadores     | Windows, macOS, Linux (KeePassXC)                   |
| Interfaz web                  | Sí                                                   | No                                                  |
| Compartición de contraseñas   | Sí (organizaciones, grupos, roles)                   | No nativo, requiere exportación manual              |
| Sincronización                | Automática entre dispositivos                        | Manual (ej. Dropbox, Nextcloud)                     |
| Auditoría y registros         | Sí (Bitwarden Enterprise)                            | No                                                  |
| Facilidad de uso              | Alta, interfaz intuitiva                             | Media, requiere conocimientos técnicos              |
| Precio                        | Gratuito / Premium desde 4 €/mes                     | Gratuito                                            |

Fuentes: [Cybernews](https://cybernews.com/best-password-managers/bitwarden-vs-keepass/), [TechRepublic](https://www.techrepublic.com/article/bitwarden-vs-keepass/), [TechRadar](https://www.techradar.com/versus/bitwarden-vs-keepass), [Slant](https://www.slant.co/versus/19421/24184/~bitwarden_vs_keepassxc), [Capterra](https://www.capterra.com/compare/210695-247048/Bitwarden-vs-KeePassXC)

## Recomendación para empresas

**Bitwarden** es la opción más adecuada para empresas por las siguientes razones:

- Gestión centralizada de usuarios y roles.
- Sincronización segura entre dispositivos.
- Facilidad para compartir credenciales entre equipos.
- Auditoría de accesos y cumplimiento normativo.

**KeePassXC** puede ser útil en entornos altamente técnicos, aislados de internet o con políticas de seguridad extremas, pero requiere más mantenimiento manual y conocimientos avanzados.

## Conclusión

Para una empresa que busca seguridad, escalabilidad y facilidad de uso, **Bitwarden** ofrece una solución robusta y moderna. KeePassXC es excelente para usuarios avanzados o entornos sin conexión, pero menos práctico para equipos colaborativos.
