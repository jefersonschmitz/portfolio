# Portfólio de Jeferson Schmitz

Site estático em português, com o NexTek como projeto principal. Todos os arquivos publicados estão em `public/`. O site não depende de pacotes npm.

## Rodar localmente

Execute `python3 -m http.server 4173 --directory public` e abra `http://localhost:4173`.

## Publicar com GitHub e Cloudflare Pages

1. Crie um repositório no GitHub e envie o conteúdo desta pasta para a branch `main`. Preserve a estrutura de `public/`.
2. Na Cloudflare, abra **Workers & Pages**, crie um projeto **Pages** com a opção de importar de um repositório Git e selecione o repositório. Se for necessário autorizar a integração, limite a seleção a este repositório.
3. Configure **Production branch** como `main`, **Framework preset** como `None`, use `exit 0` em **Build command** e use `public` como **Build output directory**. A raiz do projeto é a raiz do repositório.
4. Depois do primeiro deploy, abra a URL `pages.dev` que a Cloudflare informar. Verifique a página, a imagem do NexTek e o botão de currículo.
5. No projeto Pages, em **Custom domains**, adicione `jeferson.syrum.com.br`. Se a zona `syrum.com.br` estiver na mesma conta, use o fluxo do painel. Se estiver em outro provedor ou conta, o administrador do DNS deve criar o CNAME de `jeferson` para o endereço `pages.dev` indicado. Aguarde a ativação do domínio e teste o HTTPS.

[Integração Git no Cloudflare Pages](https://developers.cloudflare.com/pages/get-started/git-integration/) · [Domínios personalizados](https://developers.cloudflare.com/pages/configuration/custom-domains/)

## Conteúdo

- `public/index.html`: apresentação, projeto, competências, experiência, formação e contato.
- `public/styles.css`: layout e estilos responsivos.
- `public/assets/nextek.webp`: imagem da demonstração do NexTek.
- `public/assets/Curriculo_Jeferson_Schmitz.pdf`: versão do currículo para o site, com contato profissional por e-mail e links.
