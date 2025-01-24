En el video [[Never use git pull]] se explica como reacciona el programa cuando se hace un pull y hay cambios tanto en el repositorio remoto como en el local. Primero se hará una rama con los cambios provenientes del remoto, y se hará un merge entre la rama main y la nueva creada, para luego pasar a eliminar la rama temporal. Esto genera un historial no tan limpio de versiones, por lo cual es mejor utilizar git pull --rebase. En general:

```bash
git pull --rebase
```

Si falla debido a que existen conflictos entre las versiones, hacemos un rollback con:
```bash
git rebase --abort
```

Entonces, utilizamos
```bash
git pull
```

Con lo cual podremos resolver todos los conflictos que existan
