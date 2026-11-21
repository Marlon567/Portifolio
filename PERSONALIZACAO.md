# Personalização do portfólio

A identidade usa Marlon Prado, nome disponível no perfil desta tarefa. O arquivo `client/src/lib/site.ts` centraliza o nome, e-mail, WhatsApp, foto e origem pública do site. Para usar outra identidade, altere também a marca textual em `Brand`, dentro de `client/src/pages/Home.tsx`, a marca vetorial em `client/public/brand.svg` e os títulos e metadados em `client/index.html`.

## Contato configurado

O portfólio exibe `marlonprado2001@gmail.com` e `(16)99626-2395`. Esses valores foram configurados a pedido do proprietário. A propriedade `whatsappDisplay` guarda o texto visível; `whatsapp` contém apenas dígitos no formato internacional, `5516996262395`, usado como destino de `wa.me`. Mantenha os dois valores alinhados se editar o número.

O formulário valida os campos e prepara uma mensagem para revisão. O visitante pode abrir o aplicativo de e-mail ou WhatsApp com o briefing preenchido. O site não envia e-mail por servidor nem armazena os dados em banco.

## Foto e projetos

Em `profilePhoto`, use um caminho público ou URL da sua foto real. O espaço atual com iniciais é intencional e não pretende representar uma fotografia do desenvolvedor.

Os seis projetos da galeria são conceitos de demonstração, com marcas fictícias e stacks propostas. Substitua-os pelos seus trabalhos reais quando disponíveis. Os dados estão em `client/src/components/portfolio/ProjectGallery.tsx`. O botão de visualização abre uma demonstração visual, não um site externo funcional.

## Domínio e publicação

Após definir seu domínio público, preencha `publicOrigin` com a origem HTTPS real. O script `scripts/prerender.tsx` gera o conteúdo inicial e usa essa configuração para emitir canonical e `og:url`, sem inventar endereço público. Salvar uma versão e publicar são ações distintas; o portfólio pode ser conferido no painel Preview antes da publicação.

## Desenvolvimento

Execute `pnpm dev:static` para desenvolvimento, `pnpm check` para verificar tipos e `pnpm build:static` para pré-renderizar e compilar a versão de publicação. O HTML inicial contém as seções públicas para não depender apenas da execução de JavaScript.
