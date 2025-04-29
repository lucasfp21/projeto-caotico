## Usando o trivy para tratamento de vulnerabilidades no docker

#### Para rodar o scan inicial
    trivy config </diretorio>
    trivy config ./src/

#### para scanear uma imagem
    trivy image <imagem>:<tag>

#### para definir o que scanear
    trivy image --scanners vuln,misconfig,secret,license <image>:<tag>

#### para pegar um inventario de pacotes da imagem (sbom)
    trivy image --format spdx-json --output resut-spdx.json <image>:<tag>