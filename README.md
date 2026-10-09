# JS Tools

Duas ferramentas de GIF que rodam no navegador. [Abra o site](https://jairogd.github.io/js-tools/) e escolha a ferramenta na página inicial.

| Ferramenta | O que faz | Abrir direto |
| --- | --- | --- |
| SWF para GIF | Converte animações SWF ou sequências de imagens em GIF. Inclui prévia, opções de captura e exportação. | [SWF para GIF](https://jairogd.github.io/js-tools/swf-to-gif.html) |
| Criador de GIF | Monta um GIF animado a partir de imagens e permite ajustar o intervalo entre quadros. | [Criador de GIF](https://jairogd.github.io/js-tools/gif-creator.html) |

Os arquivos são processados no seu navegador. Para usar localmente, baixe o repositório e abra `index.html`; mantenha `gif-creator.html` e `gifshot.min.js` na mesma pasta. `swf-to-gif.html` já inclui seu renderizador SWF e codificador GIF.

## Arquivos

- `index.html`: escolha entre as duas ferramentas.
- `swf-to-gif.html`: conversor SWF e sequência de imagens para GIF.
- `gif-creator.html`: interface simples para criar GIFs a partir de imagens, transferida de `animated-Gif-creator`.
- `gifshot.min.js`: gifshot 0.3.2, usado pelo criador de GIF. Licença em `GIFSHOT-LICENSE.txt`.

## Limitações do conversor SWF

- GIF tem no máximo 256 cores por quadro, não contém áudio e só aceita transparência ligada ou desligada.
- A exportação padrão usa até 50 FPS. A opção **All frames** preserva os quadros capturados, mas alguns visualizadores reproduzem atrasos curtos mais lentamente.
- A captura começa do início da animação SWF, sem cliques ou outra interação. Animações controladas por scripts podem precisar de uma duração maior.
- A renderização depende da compatibilidade do Ruffle. Recursos externos não incorporados ao SWF não são carregados.
- Quadros capturados são limitados a 256 MB; cada quadro do GIF é limitado a 12 milhões de pixels.

O conversor SWF inclui Ruffle 0.2.0 e gifenc 1.0.3. Os avisos de licença estão na própria página da ferramenta.
