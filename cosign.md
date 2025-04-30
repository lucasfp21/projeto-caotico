### Cosign usado para criar assinaturas que funcionam como um certificado de garantia

####    Para criar um par de chaves
            cosing generate-key-pair

####    Para adicionar um prefixo no nome da chave
            cosign generate-key-pair --output-key-prefix chaveXPTO

####    Para assinar uma image
            cosign sign --key cosign.key <imagem>:<tag>
        
####    Para adicionar informação adicionais podemos usar o parametro -a:
            cosign verify --key cosign.key -a <chave>=<valor> <imagem>:<tag>
            
####    Podemos usar variavel de ambiente para passar as chaves
            export CONSIGN_KEY=$(cat cosign.key)
            env
            cosign sign --key env://COSIGN_KEY lufertony/imagem-assinada:v1

####    Para verificar uma imagem
            cosign verify --key cosign.pub <imagem>:<tag>
            