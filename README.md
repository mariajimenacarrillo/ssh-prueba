# Configurar `SSH Key`

## Git Bash

Configurando las credenciales y generando una nueva SSH Key desde Git
Bash.

- [ ] Abrir Git Bash
- [ ] Correr comando `git config --global user.name "tunickdegithub"`
- [ ] Correr comando `git config --global user.email "tu_correo@ejemplo.com"`
- [ ] Correr comando `ssh-keygen -t ed25519 -C "tu_correo@ejemplo.com"`
  - Presionar `enter` cuando pida el nombre del archivo y las `passphrase`
- [ ] Correr comando `notepad.exe ~/.ssh/id_ed25519.pub`
- [ ] Cuando se abra el bloc de notas copiar el contenido tal cual

## GitHub

Agregando la SSH Key a GitHub

- [ ] Abrir GitHub
- [ ] Ir a `Settings > SSH and GPG keys`
  - [SSH and GPG keys](https://github.com/settings/keys)
- [ ] Hacer clic en `New SSH key`
- [ ] Poner un nombre que reconozcas en `title`
  - Por ejemplo: `Compu escritorio`
- [ ] Pegar el contenido que copiaste del bloc de notas en `key`
- [ ] Clic a `Add SSH key`
- [ ] Si te pide que escribas tu contraseña lo escribis

## Verificación

Para comprobar que haya funcionado volver a Git Bash y correr el
siguiente comando

```
ssh -T git@github.com
```

Si pregunta `yes/no/[fingerprint]` colocar `yes`. El prompt te va a
decir si estas autenticado o si tenés el permiso denegado.

## Buenas prácticas

Ya con esta configuración no vas a necesitar token ni loggearte con las
credenciales a GitHub desde Git Bash en tu computadora.

En caso de robo o pérdida de tu computadora podés eliminar la llave SSH
desde el menú de `SSH and GPG keys` en GitHub.

Si tenes multiples computadoras deberías repetir este proceso para todas
y tener una SSH key para cada una.

> Por último y no menos importante. Cuando asocies repositorios remotos
> a tus repositorios locales usa la dirección SSH y no la HTTPS.
> Las direcciones SSH empiezan con `git@github.com`.
> Así también cada vez que clones un repositorio deberías usar este tipo
> de dirección
