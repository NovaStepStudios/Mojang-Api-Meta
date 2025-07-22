# Mojang Meta URLs — Repositorio de Endpoints Oficiales para Launchers Minecraft

Este recurso unifica y organiza **todas las URLs y APIs clave** del ecosistema de Mojang utilizadas por el launcher oficial (y alternativos) para descargar versiones, manejar cuentas, obtener assets, librerías, noticias y más.
Ideal para desarrolladores de launchers que buscan **máxima compatibilidad, control y fidelidad** al entorno original de Minecraft.

---

## 📌 Versiones y Metadatos Oficiales de Minecraft

Mojang ofrece dos infraestructuras de metadatos para versiones: `piston-meta` (moderna) y `launchermeta` (legacy). Ambas sirven para obtener información de todas las versiones de Minecraft y sus manifiestos JSON.

| Infraestructura | Recomendación          | Enlace                                                                                         |
| --------------- | ---------------------- | ---------------------------------------------------------------------------------------------- |
| `piston-meta`   | ✅ Moderna, más precisa | [`version_manifest_v2.json`](https://piston-meta.mojang.com/mc/game/version_manifest_v2.json)  |
| `launchermeta`  | ⚠️ Legacy              | [`version_manifest_v2.json`](https://launchermeta.mojang.com/mc/game/version_manifest_v2.json) |

🔹 Ambos contienen todas las versiones (`release`, `snapshot`, `old_beta`, `old_alpha`) con sus respectivos JSON de definición.

---

## 💻 Builds del Launcher Oficial

Mojang publica sus builds de launcher por plataforma y versión. Algunos endpoints aún activos permiten descargar instaladores antiguos o alternativos.

| Plataforma  | Versión | Enlace                                                                                                               |
| ----------- | ------- | -------------------------------------------------------------------------------------------------------------------- |
| Windows x86 | v1      | [🔗](https://launchermeta.mojang.com/v1/products/launcher/d03cf0cf95cce259fa9ea3ab54b65bd28bb0ae82/windows-x86.json) |
| Windows x86 | v2      | [🔗](https://launchermeta.mojang.com/v1/products/launcher/a9ed4e847bec412e84bbdc95c11e7771218be683/windows-x86.json) |
| Linux       | v1      | [🔗](https://launchermeta.mojang.com/v1/products/launcher/6f083b80d5e6fabbc4236f81d0d8f8a350c665a9/linux.json)       |
| Linux       | v2      | [🔗](https://launchermeta.mojang.com/v1/products/launcher/bb3355e087ada56549e6342233b57bf65d9d7147/linux.json)       |
| macOS       |         | [🔗](https://launchermeta.mojang.com/v1/products/launcher/022631aeac4a9addbce8e0503dce662152dc198d/mac-os.json)      |

---

## ☕ Runtimes de Java para Minecraft

El launcher descarga automáticamente el runtime Java correcto desde esta infraestructura. También se puede personalizar o forzar versiones.

* [`java-runtime/all.json`](https://launchermeta.mojang.com/v1/products/java-runtime/2ec0cc96c44e5a76b9c8b7c39df7210883d12871/all.json)

---

## 🧩 JSONs Útiles para Launchers Personalizados

Estos archivos adicionales (complementarios al manifiesto oficial) te permiten mejorar compatibilidad y extender funciones:

| Archivo              | Descripción                                                                               |
| -------------------- | ----------------------------------------------------------------------------------------- |
| `extraLibs.json`     | Lista de librerías adicionales, muchas veces requeridas por modloaders.                   |
| `maven.json`         | Repositorios Maven usados por Mojang y terceros. Útil para clonar dependencias.           |
| `launchWrapper.json` | Todas las versiones históricas del `LaunchWrapper`, ideal para `tweakers` personalizados. |

🛠 Recomendaciónes:
 - Mas LaunchWrappers : https://github.com/MCPHackers/BetterJSONs/tree/main/jsons
 

---

## 📰 Noticias, Parches y Contenido Dinámico

Estos JSON son consumidos por el launcher para mostrar novedades, alertas, parches y contenido DLC.  
Las versiones **v2** están actualizadas y mejor estructuradas para ofrecer mayor estabilidad y soporte futuro.  
Las versiones sin `v2` están desactualizadas, pero aún se usan para pruebas o compatibilidad retro.

### Patch Notes

* [JavaPatchNotes](https://launchercontent.mojang.com/javaPatchNotes.json)  
  *Versión original de notas de parche para Java Edition.*

* [JavaPatchNotesV2](https://launchercontent.mojang.com/v2/javaPatchNotes.json)  
  *Versión actualizada y mejorada para Java Edition.*

* [BedrockPatchNotes](https://launchercontent.mojang.com/bedrockPatchNotes.json)  
  *Notas de parche clásicas para Bedrock Edition.*

* [BedrockPatchNotesV2](https://launchercontent.mojang.com/v2/bedrockPatchNotes.json)  
  *Notas de parche actualizadas para Bedrock Edition.*

* [DungeonsPatchNotes](https://launchercontent.mojang.com/dungeonsPatchNotes.json)  
  *Notas clásicas para Minecraft Dungeons.*

* [DungeonsPatchNotes_V2](https://launchercontent.mojang.com/v2/dungeonsPatchNotes.json)  
  *Notas actualizadas para Minecraft Dungeons.*

* [LauncherPatchNotes](https://launchercontent.mojang.com/launcherPatchNotes_v2.json)  
  *Notas clásicas de parches para el launcher.*  
  *(Todos disponibles también en `/testing/`)*

* [LauncherPatchNotes_V2](https://launchercontent.mojang.com/v2/launcherPatchNotes_v2.json)  
  *Notas de parche actualizadas para el launcher.*

### Noticias, FAQs y Alertas

* [Noticias](https://launchercontent.mojang.com/news.json)  
  *Noticias clásicas sobre Minecraft y el launcher.*

* [NoticiasV2](https://launchercontent.mojang.com/v2/news.json)  
  *Noticias actualizadas y mejor organizadas.*

* [FAQ](https://launchercontent.mojang.com/faq.json)  
  *Preguntas frecuentes clásicas.*

* [Alertas](https://launchercontent.mojang.com/alertMessaging.json)  
  *Mensajes de alerta clásicos para el launcher.*

* [AlertasV2](https://launchercontent.mojang.com/v2/alertMessaging.json)  
  *Mensajes de alerta actualizados.*

* [MigracionCuenta](https://launchercontent.mojang.com/accountMigration.json)  
  *Información clásica sobre migración de cuentas.*

### Dungeons DLC

* [DLC EN 🇺🇸](https://launchercontent.mojang.com/dungeonsDLC/en-US.json)  
  *Contenido descargable para Minecraft Dungeons en inglés.*

* [DLC DE 🇩🇪](https://launchercontent.mojang.com/dungeonsDLC/de-DE.json)  
  *Contenido descargable para Minecraft Dungeons en alemán.*

* [DLC FR 🇫🇷](https://launchercontent.mojang.com/dungeonsDLC/fr-FR.json)  
  *Contenido descargable para Minecraft Dungeons en francés.*

* [DLC ES 🇪🇸](https://launchercontent.mojang.com/dungeonsDLC/es-ES.json)  
  *Contenido descargable para Minecraft Dungeons en español.*

* [DLC PT 🇧🇷](https://launchercontent.mojang.com/dungeonsDLC/pt-BR.json)  
  *Contenido descargable para Minecraft Dungeons en portugués brasileño.*

* [DLC RU 🇷🇺](https://launchercontent.mojang.com/dungeonsDLC/ru-RU.json)  
  *Contenido descargable para Minecraft Dungeons en ruso.*

* [DLC CN 🇨🇳](https://launchercontent.mojang.com/dungeonsDLC/zh-CN.json)  
  *Contenido descargable para Minecraft Dungeons en chino simplificado.*

* [DLC EN 🇺🇸 v2](https://launchercontent.mojang.com/v2/dungeonsDLC/en-US.json)  
  *Versión actualizada del DLC en inglés.*

* [DLC DE 🇩🇪 v2](https://launchercontent.mojang.com/v2/dungeonsDLC/de-DE.json)  
  *Versión actualizada del DLC en alemán.*

* [DLC FR 🇫🇷 v2](https://launchercontent.mojang.com/v2/dungeonsDLC/fr-FR.json)  
  *Versión actualizada del DLC en francés.*

* [DLC ES 🇪🇸 v2](https://launchercontent.mojang.com/v2/dungeonsDLC/es-ES.json)  
  *Versión actualizada del DLC en español.*

* [DLC PT 🇧🇷 v2](https://launchercontent.mojang.com/v2/dungeonsDLC/pt-BR.json)  
  *Versión actualizada del DLC en portugués brasileño.*

* [DLC RU 🇷🇺 v2](https://launchercontent.mojang.com/v2/dungeonsDLC/ru-RU.json)  
  *Versión actualizada del DLC en ruso.*

* [DLC CN 🇨🇳 v2](https://launchercontent.mojang.com/v2/dungeonsDLC/zh-CN.json)  
  *Versión actualizada del DLC en chino simplificado.*


---


## 🎮 APIs de Skins, Sesión y Autenticación

### Sesión y Skins

| Descripción                | Endpoint                                                                                                 |
| -------------------------- | -------------------------------------------------------------------------------------------------------- |
| Obtener skin/capa por UUID | [`/session/minecraft/profile/{uuid}`](https://sessionserver.mojang.com/session/minecraft/profile/{uuid}) |
| Obtener UUID por username  | [`/users/profiles/minecraft/{username}`](https://api.mojang.com/users/profiles/minecraft/{username})     |

### Autenticación (Yggdrasil)

| Función               | Endpoint                                                                       |
| --------------------- | ------------------------------------------------------------------------------ |
| Iniciar sesión        | [`/authenticate`](https://authserver.mojang.com/authenticate)                  |
| Refrescar token       | [`/refresh`](https://authserver.mojang.com/refresh)                            |
| Validar sesión activa | [`/validate`](https://authserver.mojang.com/validate)                          |
| Invalidar sesión      | [`/invalidate`](https://authserver.mojang.com/invalidate)                      |
| Seguridad adicional   | [`/user/security/challenges`](https://api.mojang.com/user/security/challenges) |

---

## 📚 Recursos y Librerías

* [`libraries.minecraft.net`](https://libraries.minecraft.net)
  Repositorio Maven oficial con todas las librerías usadas por el launcher.

* [`resources.download.minecraft.net`](https://resources.download.minecraft.net)
  Assets (texturas, sonidos, música) organizados por hash (SHA1).

---

## 🌐 Dominios Oficiales de Mojang — Infraestructura

Organizados por función, estos dominios componen el backend de Mojang. Útiles para monitoreo, análisis de red o desarrollo personalizado.

### 🎯 Metadatos y Versiones

| Dominio                        | Uso                                   |
| ------------------------------ | ------------------------------------- |
| `piston-meta.mojang.com`       | 📌 Meta moderno de versiones y builds |
| `launchermeta.mojang.com`      | 📦 Meta clásico/legacy                |
| `launchercontent.mojang.com`   | 📰 Contenido dinámico del launcher    |
| `redstone-launcher.mojang.com` | 🔬 Builds experimentales de launcher  |

### 📦 Librerías y Assets

| Dominio                            | Uso                             |
| ---------------------------------- | ------------------------------- |
| `libraries.minecraft.net`          | 📚 Librerías y dependencias     |
| `resources.download.minecraft.net` | 🎨 Assets y recursos multimedia |

### 🔐 Autenticación y Sesiones

| Dominio                    | Uso                         |
| -------------------------- | --------------------------- |
| `authserver.mojang.com`    | Login con token             |
| `sessionserver.mojang.com` | Validación de sesión, skins |
| `api.mojang.com`           | UUID, seguridad y usuario   |

### 🧱 Complementarios o Legacy

| Dominio                 | Estado     | Descripción                     |
| ----------------------- | ---------- | ------------------------------- |
| `skins.minecraft.net`   | 💤 Legacy  | Sistema viejo de skins sin UUID |
| `session.minecraft.net` | ❌ Obsoleto | Reemplazado por `sessionserver` |
| `mcoapi.minecraft.net`  | ⚠️ Parcial | API de Realms                   |
| `mojang.com`            | Activo     | Sitio oficial de la empresa     |

---

## ✅ Recomendaciones para Desarrolladores

* Centralizá todos estos endpoints en un módulo configurable (`mojangEndpoints.json` o similar).
* Implementá chequeos automáticos (`fetch`, `ping`, `curl`) para validar disponibilidad en tiempo real.
* Cacheá datos pesados como `version_manifest.json`, assets o listas de librerías.
* Añadí soporte para los tres entornos: producción (`/`), pruebas (`/testing/`) y legado (`launchermeta`).
* Si ofrecés compatibilidad con mods, loaders o tweaks, cargá tu propio `extraLibs.json` y mapeá `launchWrapper.json` para retrocompatibilidad.

---

> Este listado está pensado para ayudar a desarrolladores que quieran crear launchers potentes, modulares y fieles al original de Mojang, sin depender de recursos externos no oficiales.
