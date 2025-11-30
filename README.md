# Gestão Estratégica em Saúde – Site de apoio

Este site reúne, em um só lugar, todo o material do curso de Gestão Estratégica em Saúde: plano completo, documentos de referência, guias práticos e PDFs para impressão. É estático (HTML/CSS) e pensado para funcionar bem no celular e no computador.

## Como navegar
- Página inicial (`index.html`): traz o panorama do curso, lista dos módulos e contato do instrutor.
- Navbar fixa em todas as páginas leva ao plano (`plano-de-curso.html`) e à lista de módulos (`index.html#modulos`).
- Plano de curso (`plano-de-curso.html`): objetivos, ementa, cronograma e bibliografia.
- Páginas dos módulos (`modulo-1.html` … `modulo-4.html`): resumo, capacidades-chave e links diretos para cada material.
- Em cada documento ou guia há breadcrumb completo (Início › Módulos › Módulo X › Material) e botão “Versão para impressão (PDF)” para baixar/abrir o PDF correspondente.
- Links externos são abertos em nova aba para manter a navegação no site.

## Materiais disponíveis
- Plano de curso: HTML e PDF.
- Módulo 1: documento de referência, guia prático e slides (PDF).
- Módulo 2: documento de referência e guia prático.
- Módulo 3: documento de referência.
- Módulo 4: documento de referência.

## Estrutura de arquivos (para quem precisar editar)
- `assets/`: originais em Markdown e PDFs.
- `modulo*-*.html` e `plano-de-curso.html`: gerados a partir dos Markdown (via pandoc).
- `modulo-1.html` … `modulo-4.html`: páginas de navegação de cada módulo.
- `styles.css`: tema visual.
- `doc-template.html5`: template usado nas conversões; já inclui metadados, botão de impressão e favicon, aceita `module_title`, `module_url` e `breadcrumb_text` para preencher a trilha de navegação, e força links externos a abrirem em nova aba com `rel=\"noopener noreferrer\"`.
- `favicon.svg`: ícone usado no site.
