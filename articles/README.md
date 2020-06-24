# <a name="articles"></a>Artigos

Neste diretório, você pode encontrar os artigos para a documentação do kit de desenvolvimento do Quantum. Esse diretório contém:

- **Diretórios de artigos**: contêm os artigos para cada seção da documentação. Nesses diretórios, você pode encontrar o seguinte conteúdo:
  
  - Cada diretório contém um `toc.yml` arquivo para exibir o conteúdo do diretório no sumário principal (TOC).
  - Redução de artigos que contêm a documentação. Esses artigos devem seguir as diretrizes do [Guia do colaborador do Microsoft docs](https://docs.microsoft.com/en-us/contribute/).
  - Subdiretórios de artigos. Esses subdiretórios também devem conter seu próprio `toc.yml` arquivo.

> :p encil: embora seja possível referenciar os `*.md` arquivos diretamente no `TOC.yml` arquivo pai, para manter as coisas ordenadas, apenas os referimos a partir do `toc.yml` seu diretório atual.

- ** `TOC.yml` Arquivo de Sumário principal (TOC)**: nesse arquivo, as seções do Sumário do site são listadas junto com a referência ao arquivo principal `toc.yml` do diretório de cada seção.
- **`index.yml`** YAML com a configuração da página de aterrissagem da documentação.
- **`\media`**: Um diretório para armazenar todas as imagens usadas na documentação. Ele contém um `\media\src` subdiretório para armazenar arquivos de origem das imagens.
- **Arquivos de licença**: arquivos que contêm licenças legais
- **Arquivos técnicos**: arquivos que contêm macros e metadados.

## <a name="guidelines"></a>Diretrizes

Algumas diretrizes gerais sobre a organização deste diretório para colaboradores:

- Cada diretório ou subdiretório deve conter seu próprio `toc.yml` arquivo no qual são referidos artigos de mesmo nível ou os `toc.yml` arquivos de seus diretórios filho.
- A organização dos diretórios do repositório deve ser o mais próximo possível da organização do Sumário do site da documentação.
- Todas as imagens devem ser armazenadas em `articles\media` e não na pasta artigos.
- Os títulos dos artigos, os nomes no sumário e a *UID* dos metadados devem ser o mais próximo possível entre eles e representam claramente o cabeçalho H1 do documento de redução.

## <a name="adding-images"></a>Adicionando imagens

Para que as imagens sejam renderizadas corretamente no modo escuro, você deve evitar transparências.
- Para `*.jpg` arquivos, você não precisa fazer nada, pois o formato de arquivo não dá suporte a elementos transparentes.
- Para `*.png` arquivos, você deve adicionar um plano de fundo branco ou alterar o valor do canal alfa para 100. A maneira mais fácil de fazer isso no Windows é abrir o arquivo no Paint e salvar, substituindo o arquivo original.
- Para `*.svg` arquivos, você deve adicionar um retângulo branco na camada mais baixa. Você pode fazer isso com Inkscape:
  - Abra o arquivo `*.svg` .
  - Selecione a ferramenta Criador quadrado e desenhe um retângulo branco na parte superior da figura original.
  - Selecione a ferramenta "selecionar e transformar objetos" clicando na seta escura ou pressionando F1.
  - Ao selecionar o retângulo, clique no elemento da barra de ferramentas "seleção inferior para inferior (final)".
  - Ajuste o retângulo com o mouse ou as teclas de direção.
