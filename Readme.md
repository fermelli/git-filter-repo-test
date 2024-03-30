# Prueba de git-filter-repo

Este repositorio es una prueba de git-filter-repo.

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

## Cambiar el autor de los commits

Para cambiar el autor de todos los commits de un repositorio, se puede utilizar el siguiente comando:

```bash
$ git-filter-repo --mailmap mailmap.txt
```

Donde:

- `mailmap.txt` (puede tener cualquier nombre) es un archivo que contiene el mapeo de los autores originales a los autores nuevos, con el siguiente formato:

```
Nombre Autor Correcto <correo_autor_correcto@email.com> Nombre Autor Incorrecto <correo_autor_incorrecto@email.com>
```

Si al ejecutar el comando se rechaza el cambio en el historial de commits, se puede forzar el cambio con la opción `--force`.

```bash
$ git-filter-repo --mailmap mailmap.txt --force
```

- NOTA: Si le aparece un eror como:

```bash
$ fatal: replace depth too high for object b769532341677b7c34b5adeb85a173daa0ced852
```

Puede solucionarlo con el siguiente comando:

```bash
$ git replace -d b769532341677b7c34b5adeb85a173daa0ced852
```
