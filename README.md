# Tarefa: Docker e GitHub

Este repositorio, creado por **Martín Álvarez Comesaña**, contén un tutorial que describe o proceso de creación e xestión de contedores utilizando Docker, así como a integración con GitHub. O obxectivo é ofrecer un paso a paso claro e conciso sobre as distintas tarefas que se poden realizar.

## Contido do Tutorial

1. **Crear un novo repositorio público en Git**
   - Crea un repositorio chamado "tarefa" en GitHub.
   - Clona o repositorio no teu equipo local.

2. **Engadir un arquivo `readme2.md`**
   - Crea un arquivo chamado `readme2.md` no repositorio clonado e engade unha frase á túa elección.

3. **Usar Docker e a imaxe de Ubuntu**
   - Realiza os seguintes pasos e comandos:

### Pasos e Comandos

#### 1. Descargar e comprobar que unha imaxe está no teu equipo
   ```bash
   docker pull ubuntu
   docker images
   ```
#### 2. Crear un contenedor sen nome

   ```bash

docker run -d ubuntu sleep 3600

   - Para comprobar que está arrincado, usa:

docker ps -a
   ```
#### 3. Crear un contenedor co nome u1

   ```bash

docker run -d --name u1 ubuntu sleep 3600
   ```
    - Para acceder a el:

   ```bash

docker exec -it u1 bash
   ```
#### 4. Comprobar a súa IP e facer ping a google.com:

   ```bash
   - Para ver a ip, podemos tamén utilizar ip addr
ip addr show
ping google.com
   ```
#### 5. Crear un contenedor co nome bono

   ```bash

docker run -d --name bono ubuntu sleep 3600

    Para verificar se podes facer ping entre os contenedores:
   
bash

docker exec u1 ping bono
   ```
#### 6. Que pasa co contedor se pechas as terminais?

    Se pechas a terminal, o contedor seguirá activo se foi creado en modo background (-d). Comproba con:

    bash

    docker ps

#### 7. Cánta memoria no disco duro ocupaches?

```bash

docker system df
```
#### 8. Cánta RAM ocupan os contenedores?

```bash

docker stats
```
#### 9. Cómo fixeches para clonar o repositorio

```bash

git clone https://github.com/tu-usuario/tarefa.git
```
#### 10. Cómo engades o arquivo readme2.md

```bash

git add readme2.md
```
#### 11. Pasos para subir o arquivo que estás editando e readme2.md

```bash

git commit -m "Engadido readme2.md"
git push origin main
```
#### 12. Comprobar diferenzas entre o repositorio local e o remoto

```bash

git fetch
git diff origin/main
```
#### Conclusión

Agora sabes como utilizar Docker e Git para xestionar contedores e repositores. Este tutorial proporciona un marco de referencia para traballar con estas ferramentas de forma efectiva. Se tes dúbidas ou suxestións, non dubides en contactarme.
