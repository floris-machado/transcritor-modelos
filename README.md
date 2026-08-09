# transcritor-modelos

Artefatos de modelos de tradução automática convertidos para
[CTranslate2](https://github.com/OpenNMT/CTranslate2) (quantização int8),
usados pelo aplicativo **Transcritor** (uso pessoal). Este repositório contém
apenas artefatos derivados de modelos públicos — nenhum código do aplicativo.

## Artefatos (release `opus-mt-ct2-20260809`)

| Artefato | Modelo original | Licença | SHA-256 |
|---|---|---|---|
| `opus-mt-romance-en-ct2.tar.gz` | [Helsinki-NLP/opus-mt-ROMANCE-en](https://huggingface.co/Helsinki-NLP/opus-mt-ROMANCE-en) | Apache-2.0 | `6d299ba16e5c08f0f483c7eaf93c2c55d9080f24e36929ba9a465f18b9bc8e0f` |
| `opus-mt-en-pt-ct2.tar.gz` | [Helsinki-NLP/opus-mt-tc-big-en-pt](https://huggingface.co/Helsinki-NLP/opus-mt-tc-big-en-pt) | [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) | `108e12466b739f5aca25889768568d36a3fcc9c0d95db2c6ed087348a6f29ed1` |
| `opus-mt-en-es-ct2.tar.gz` | [Helsinki-NLP/opus-mt-en-es](https://huggingface.co/Helsinki-NLP/opus-mt-en-es) | Apache-2.0 | `62f1f5573ed5a02ef84ed8eb41138f995f6e19fb8d1dd4ce2794879c33604669` |
| `opus-mt-es-en-ct2.tar.gz` | [Helsinki-NLP/opus-mt-es-en](https://huggingface.co/Helsinki-NLP/opus-mt-es-en) | Apache-2.0 | `09886c346d900ca7fb64165d30d973803d61f4d50a2d877f0f7f4d6c44df6c92` |

## Atribuição e alterações

Modelos originais do projeto **OPUS-MT** — Language Technology Research Group
at the University of Helsinki (Helsinki-NLP); Tiedemann & Thottingal (2020),
*OPUS-MT — Building open translation services for the World*.

Alterações em relação aos originais: conversão do formato Marian/transformers
para CTranslate2 com quantização int8 (`ct2-transformers-converter`;
CTranslate2 4.8.1, transformers 5.14.1, torch 2.13.0, em 2026-08-09), com os
tokenizadores SentencePiece copiados sem alteração. Cada `tar.gz` embute um
`ATTRIBUTION.txt` com a fonte, o commit exato e a licença. Os artefatos são
redistribuídos sob as mesmas licenças dos modelos originais.

## Canal de atualização do catálogo

O diretório [`catalog/`](catalog/) publica o catálogo vigente do Transcritor
(`models.json`, `providers.json` e o schema). O aplicativo consulta esta
fonte por HTTPS (REQ-028) e valida cada candidato antes de qualquer
aplicação: versão estritamente maior, schema compatível, nenhuma entrada
instalável sem SHA-256, preços de API só com data de verificação. A
atualização nunca é aplicada sem confirmação do usuário diante do diff.
