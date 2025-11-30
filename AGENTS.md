# Repository Guidelines

Contributor quick-start for maintaining the course materials stored here.

## Project Structure & Module Organization
- `assets/` contains all course content in Portuguese; Markdown is the source of truth and PDFs are checked in for distribution.
- File names follow `modulo{n}-<tema>.md` and related PDFs mirror the same name; keep numbering aligned with the course sequence.
- Keep supportive material (images, spreadsheets) alongside the matching module file inside `assets/` and reference them with relative links.

## Build, Test, and Development Commands
- No build pipeline is required; edit Markdown directly and keep PDFs in sync when relevant. Use `-M print_link='assets/<file>.pdf'` and `-M author='Iúri Leão'` when running pandoc to exibir o botão “Versão para impressão” e preencher metadados.
- Ao gerar HTML via pandoc, informe `-M module_title="Módulo X"` e `-M module_url="modulo-x.html"` para os materiais de módulo; use `-M breadcrumb_text` apenas se precisar nome customizado no último nível.
- Example PDF export (if you use Pandoc locally): `pandoc assets/modulo1-desenvolvendo-pensamento-estrategico.md -o assets/modulo1-desenvolvendo-pensamento-estrategico.pdf`.
- Use your editor’s Markdown preview to validate headings, lists, and tables before committing.

## Coding Style & Naming Conventions
- Prefer one `#` title per document, `##` for main sections, and concise bullet lists for steps or summaries.
- Write instructional content in Portuguese to match existing modules; keep terminology consistent across modules.
- Use descriptive alt text for any images and keep relative paths (e.g., `![Esquema](./assets/modulo2-diagrama.png)`).
- Keep line breaks where they improve readability; avoid trailing spaces. Update PDFs only after finalizing the Markdown.

## Testing Guidelines
- Proofread for clarity, consistency between modules, and broken internal references before publishing.
- When updating PDFs, open them to confirm the export kept headings, lists, and page breaks legible.
- If you add links, click through from a Markdown preview to verify they resolve correctly.

## Commit & Pull Request Guidelines
- Commit messages: imperative mood, short scope-first subject (e.g., `Atualiza guia do modulo2`). Group related Markdown and PDF updates together.
- Pull requests: include a brief summary of module(s) touched, highlight any structure changes, and note whether PDFs were regenerated. Add screenshots of key page sections if layout or imagery changed.

## Security & Content Hygiene
- Do not commit sensitive learner data or external assets without confirming reuse rights. Strip personal metadata from PDFs before adding them.
- Large binary files increase repository size; prefer compressed assets and keep Markdown as the canonical source whenever possible.

## Histórico recente de alterações (nov/2025)
- Link da marca no template volta para `index.html`; script de capitalização automática de headings removido; rodapé padrão retirado do template (apenas o index mantém data manual).
- Botão “Versão para impressão (PDF)” exibido no hero quando `print_link` é informado na geração via pandoc; metadados de autor/descrição incluídos no head; favicon `favicon.svg` adicionado.
- Navbar: link “Plano” aponta para `plano-de-curso.html` (não mais para âncora interna); link “Módulos” permanece em `index.html#modulos`.
- Breadcrumbs em materiais de módulo seguem `Início › Módulos › Módulo X › Documento/Guia`; template `doc-template.html5` suporta `module_title/module_url` para preencher essa trilha.
- Documento de referência dos módulos 1–4 disponível; guias práticos publicados para módulos 1 e 2; slides atualizados apenas para módulo 1.
- Landing e páginas de módulos redesenhadas para mobile first, com cards linkáveis e badges de status.
- HTML gerado via pandoc com template unificado (`doc-template.html5`); apenas `.md` e `.pdf` permanecem em `assets/`.
- Referências bibliográficas dos módulos 1–3 com links “Acesso externo” em nova aba.
- Badges de “Em desenvolvimento” posicionados no canto inferior direito dos cards pendentes.
- Navegação ajustada com `scroll-margin-top` em headings para ancoragem correta.
- Links externos padronizados para abrir em nova aba com `target=\"_blank\"` e `rel=\"noopener noreferrer\"`; template `doc-template.html5` aplica o comportamento automaticamente.
- Tabelas e blocos `<pre>/<code>` são roláveis horizontalmente apenas com CSS para evitar estouro em mobile; manter a regra em `styles.css` ao exportar novos HTMLs.
