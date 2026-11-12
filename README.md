# Encarte — Supermercado Irene

Página estática, sem login, JavaScript, dependências ou compilação.

## Publicação

Envie para o repositório do GitHub esta estrutura, incluindo os arquivos de configuração:

```text
public/
  index.html
  Capa.jpeg
  Verso.jpeg
vercel.json
.vercelignore
README.md
```

Importe o repositório na Vercel. Use **Framework Preset: Other**, **Build Command: vazio**, **Install Command: vazio** e **Output Directory: public**, com Root Directory na raiz do repositório. O `vercel.json` já define essas opções. Confira se o domínio de produção está público em Deployment Protection.

## Trocar o encarte semanalmente

1. No GitHub, abra a pasta `public` da branch de produção conectada à Vercel.
2. Use **Add file → Upload files** para enviar os dois novos originais, com os nomes exatos **Capa.jpeg** e **Verso.jpeg**, substituindo os anteriores.
3. Confirme em **Commit changes**. Se estiver usando outra branch, faça o merge na branch de produção.
4. Aguarde o deploy automático da Vercel concluir e recarregue o site.

Mantenha as letras maiúsculas e a extensão `.jpeg`: os nomes diferenciam maiúsculas de minúsculas na hospedagem. Substituir apenas os arquivos no computador não atualiza o site; é necessário enviá-los ao GitHub.

O endereço de produção permanece o mesmo, sem data. Um QR Code apontando para esse endereço continua válido a cada semana. Use o domínio de produção, não uma URL de preview ou de um deploy antigo.

O HTML e as imagens têm cache configurado como `no-store` na Vercel. Quem já estiver com a página aberta precisa recarregá-la; não há atualização automática de abas abertas.

As imagens são exibidas inteiras, capa primeiro e verso abaixo, com zoom nativo permitido. Se as dimensões dos novos originais forem diferentes de 2480 × 3508 px, ajuste os atributos `width` e `height` no HTML para reservar o espaço correto durante o carregamento; o CSS mantém a proporção natural das imagens.

## Conferência

Abra `public/index.html` para conferir localmente. Após publicar, teste o endereço em uma janela anônima e no celular, incluindo os dois links “Abrir imagem para ampliar”.

Esta configuração é para **GitHub como repositório e Vercel como hospedagem**. O GitHub Pages não utiliza o `vercel.json` nem seus cabeçalhos de cache.
