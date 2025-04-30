### Para mudar listar o capability
    man 7 capabilities

### Para adicionar uma capability:
    docker container run -it --cap-add=SYS-ADMIN <imagem>:<tag> /bin/bash

### Executar container em modo priviligiado
    docker container run -it --privileged <imagem>:<tag> /bin/bash

### imagem distroless (sem se de um distribuição, só o basico realmente)
    https://edu.chainguard.dev/chainguard/chainguard-images/getting-started/node/

mudar Dockerfile com as partes indicadas na documentacao e depois buildar uma nova imagem e subir o container