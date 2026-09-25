# AWS Well-Architected Framework — e-book

## Gerar o PDF

É necessário ter Google Chrome ou Chromium instalado. O script usa a versão de impressão do `ebook.html`, incluindo capa, sumário, respostas e numeração das páginas.

```bash
python3 gerar_pdf.py
```

O arquivo é salvo em `output/pdf/ebook-aws-well-architected.pdf`. Para escolher outro destino ou outro HTML:

```bash
python3 gerar_pdf.py --input ebook.html --output meu-ebook.pdf
```

Se o navegador não for encontrado automaticamente, passe `--chrome /caminho/para/chrome` ou defina `CHROME_BIN`.
