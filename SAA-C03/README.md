# Guia de revisão SAA-C03

- `material-original.md`: material-fonte revisado com mapa das 14 tarefas oficiais, método para cenários, correções de disponibilidade de serviços em 2026 e questões de múltipla resposta; o nome foi mantido para preservar o fluxo de geração.
- `ebook.html`: e-book autônomo, com sumário, tabelas e flashcards expansíveis.
- `output/pdf/saa-c03-guia-de-revisao.pdf`: versão para impressão.

Para atualizar o HTML depois de editar o Markdown:

```bash
python3 -m pip install markdown-it-py beautifulsoup4
python3 gerar_ebook.py
```

Para regenerar o PDF neste repositório:

```bash
python3 gerar_pdf.py
```

O script usa o Google Chrome/Chromium em modo headless (sem dependências Python extras). Opções: `--input`, `--output` e `--chrome /caminho/do/executável` (ou a variável `CHROME_BIN`).

Os links no formato `[[nota do Obsidian]]` foram mantidos como texto porque os arquivos das notas não vieram com o material.
