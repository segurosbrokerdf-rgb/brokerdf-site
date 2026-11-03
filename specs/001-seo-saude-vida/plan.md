# Plano: Spec 001

- Site estático no GitHub Pages: páginas em pasta com `index.html`, gerando URLs limpas.
- CSS das páginas novas em `assets/paginas.css`, com as cores da home.
- `_config.yml` exclui `specs/` da publicação.
- Fluxo: branch por spec, Pull Request em rascunho, merge na `main` só após aprovação, pois a `main` publica direto.
- Verificação: JSON-LD válido, links internos resolvidos e renderização local com `npx serve`.
