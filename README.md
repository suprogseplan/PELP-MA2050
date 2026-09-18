# Painel PELP Maranhão 2050

Painel gerencial (HTML autocontido — sem backend, sem build) de acompanhamento da revisão do Plano Estratégico de Longo Prazo Maranhão 2050 (SUPROG/SEPLAN).

## Arquivos deste pacote

- `Dashboard_PELP_Maranhao_2050.html` — o painel (nome de referência usado nas atualizações)
- `index.html` — cópia idêntica, para o GitHub Pages servir na raiz do site automaticamente
- `.nojekyll` — desativa o processamento Jekyll do GitHub Pages (garante que o arquivo seja servido tal como está, sem transformações)

## Como publicar no GitHub Pages (uma vez só)

1. Crie um repositório novo no GitHub (pode ser público ou privado, desde que o plano do GitHub permita Pages em repositório privado).
2. Suba os três arquivos acima para a raiz do repositório (`git add .` → `git commit` → `git push`, ou arraste os arquivos pela interface web do GitHub).
3. No repositório, vá em **Settings → Pages**.
4. Em "Build and deployment", selecione **Deploy from a branch**, escolha a branch `main` (ou `master`) e a pasta `/ (root)`.
5. Salve. Em 1–2 minutos o GitHub mostra a URL pública, algo como:
   `https://seu-usuario.github.io/nome-do-repositorio/`

Essa URL vai abrir direto o `index.html` — ou seja, o painel completo, sem precisar digitar o nome do arquivo.

## Como atualizar (a cada nova versão da planilha)

1. Eu gero a nova versão do `Dashboard_PELP_Maranhao_2050.html` (e do `index.html`, idênticos).
2. Você substitui os dois arquivos no repositório pela versão nova, mantendo os mesmos nomes.
3. Faça commit e push. O GitHub Pages atualiza automaticamente em 1–2 minutos — **a URL não muda**.

## Observações técnicas

- O único recurso externo carregado é a fonte do Google Fonts (`fonts.googleapis.com`) — funciona normalmente em qualquer hospedagem estática, GitHub Pages incluído.
- Não há dependência de servidor, banco de dados ou build step: é um único arquivo HTML com CSS e JavaScript embutidos, mais os dados do cronograma também embutidos como JSON.
- Funciona igual em ambos os arquivos (`Dashboard_PELP_Maranhao_2050.html` e `index.html`) — são cópias idênticas, mantidas só por conveniência de acesso.
