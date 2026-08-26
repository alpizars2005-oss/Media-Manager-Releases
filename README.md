# Alpizers Releases

Public Windows distribution channel for **Alpizers**. Application development remains in a separate private repository; this repository intentionally contains release-channel documentation while installers, portable builds, and update manifests are attached to GitHub Releases.

## Español

### Archivos de cada release

Las releases actuales publican:

- `Alpizers-Setup-<version>.exe` — instalador recomendado.
- `Alpizers-Windows-portable-<version>.zip` — versión portátil.
- `update-manifest.json` — versión, URL del instalador y SHA-256 que usa el actualizador de Alpizers.

Las versiones 1.3.x y anteriores fueron publicadas bajo el nombre histórico **Media Manager** y conservan sus nombres originales para mantener íntegro el historial de releases.

### Verificar antes de ejecutar

Descarga el instalador y el `update-manifest.json` de la **misma release** y compara el SHA-256 del instalador:

```powershell
Get-FileHash -Algorithm SHA256 .\Alpizers-Setup-<version>.exe
```

La guía completa está en [`VERIFY_RELEASES.md`](VERIFY_RELEASES.md). Una coincidencia de SHA-256 demuestra integridad respecto al digest esperado; no debe presentarse como garantía absoluta de que un archivo sea seguro.

Consulta también [`SECURITY.md`](SECURITY.md) para la frontera de confianza del canal de releases.

### Idiomas y uso responsable

Alpizers mantiene interfaz e instalador en **Español / English**, con textos redactados para sonar naturales en ambos idiomas.

> Usa Alpizers únicamente con contenido que tengas derecho a descargar, compartir o almacenar. BitTorrent no es anónimo y los archivos obtenidos de terceros pueden ser inseguros.

---

## English

### Files in each release

Current releases publish:

- `Alpizers-Setup-<version>.exe` — recommended installer.
- `Alpizers-Windows-portable-<version>.zip` — portable build.
- `update-manifest.json` — version, installer URL, and SHA-256 used by the Alpizers updater.

Versions 1.3.x and earlier were published under the historical **Media Manager** name and keep their original asset names for release-history integrity and upgrade compatibility.

### Verify before running

Download the installer and `update-manifest.json` from the **same release**, then compare the installer SHA-256:

```powershell
Get-FileHash -Algorithm SHA256 .\Alpizers-Setup-<version>.exe
```

See [`VERIFY_RELEASES.md`](VERIFY_RELEASES.md) for the full procedure. A matching SHA-256 demonstrates integrity relative to the expected digest; it must not be presented as an absolute safety guarantee.

See [`SECURITY.md`](SECURITY.md) for the release-channel trust boundary.

### Language and responsible use

Alpizers provides a natural **English / Español** interface and multilingual installer.

> Use Alpizers only with content you have the right to download, share, or store. BitTorrent is not anonymous, and files obtained from third parties may be unsafe.

---

**With love,**  
**— alpizars2005-oss**
