# Prueba de git-filter-repo

Este repositorio es una prueba de git-filter-repo. El objetivo es cambiar el autor de todos los commits de un repositorio.

## Prerrequisitos

- git >= 2.22.0 como mínimo
- python3 >= 3.5 ([Notas para windows](https://github.com/newren/git-filter-repo/blob/main/INSTALL.md#notes-for-windows-users))

## Instalación

### Instalacion simple (descarga del script)

Descargar el script [git-filter-repo](https://github.com/newren/git-filter-repo/blob/main/git-filter-repo), manteniendo el mismo nombre y sin extensión. Luego puede ejecutar cualquier comando de la siguiente manera:

```bash
$ python3 git-filter-repo --analyze
```

Si coloca el script en su $PATH, puede ejecutarlo sin el prefijo `python3`:

```bash
$ git-filter-repo --analyze
```

### Instalacion via Package Manager

```bash
$ PACKAGE_MANAGER install git-filter-repo
```
