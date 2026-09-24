# Cobertura funcional em relação ao manual do WinMerge

Esta matriz compara o FirawMerge 0.2.0 com as funções descritas no manual oficial do WinMerge. Os nomes **Texto, Tabela, Binário, Imagem e Página da Web** correspondem às cinco opções de abertura que aparecem na imagem enviada pelo usuário. O FirawMerge implementa essas categorias com código próprio, sem prometer compatibilidade completa com o WinMerge.

| Área do manual | Incluído agora | Ainda não incluído |
| --- | --- | --- |
| [Abertura e tipos](https://manual.winmerge.org/en/Open_paths.html) | Dois ou três caminhos em quaisquer campos, pastas ou arquivos, detecção automática, troca de tipo por arquivo e comandos no menu clássico e no menu principal do Explorador no Windows 11. Trabalho salvo em `.firawmerge` e reaberto a partir dos arquivos locais. | O menu principal requer instalação do pacote assinado da extensão; arquivos de projeto do WinMerge não são lidos. |
| [Pastas](https://manual.winmerge.org/en/Compare_dirs.html) e [filtros](https://manual.winmerge.org/en/Filters.html) | Comparação recursiva, opção de excluir subpastas, máscara simples como `*.txt;*.csv`, busca na lista e status por hash. | Filtros por expressão, método de comparação por data/tamanho, operações em lote de mover/excluir/copiar. |
| [Texto](https://manual.winmerge.org/en/Compare_files.html) | Diferenças, merge de três versões, escolhas por bloco, edição do resultado e ocultação das linhas iguais. | Detecção de blocos movidos, filtros de linha, opções completas para espaços/capitalização e sincronização avançada de navegação. |
| [Tabela](https://manual.winmerge.org/en/Compare_table.html) | CSV/TSV em colunas; vírgulas, tabulações, aspas duplicadas e quebras de linha em campos; merge por registro. | Delimitador e caractere de aspas configuráveis, redimensionamento das colunas e edição direta por célula. |
| [Binário](https://manual.winmerge.org/en/Compare_bin.html) | Hexadecimal com offset, bytes diferentes em destaque, ocultação de blocos iguais e cópia integral da versão escolhida. | Edição byte a byte, busca hexadecimal e múltiplas configurações de exibição. |
| [Imagem](https://manual.winmerge.org/en/Compare_images.html) | Imagens comuns lado a lado, sobreposição alfa, modo de diferença e zoom; cópia integral da versão escolhida. | Destaque por blocos e limiar de cor, páginas de PDF/TIFF e OCR. |
| [Página da Web](https://manual.winmerge.org/en/Compare_webpages.html) | URLs HTTP(S) ou HTML local, prévia isolada, código-fonte com diferenças e exportação offline da captura. | Captura visual da página inteira, árvore de recursos, sincronização de cliques e navegação. O próprio manual chama esse modo de experimental. |

O relatório HTML independente permite abrir, alternar e baixar versões com dois cliques, inclusive para tabela, binário e imagem. A prévia de páginas no relatório não executa scripts nem carrega recursos externos; o arquivo exportado guarda o HTML capturado no momento da comparação.

## Limites de tamanho

- Texto, tabela e página web: 2 MB por versão.
- Binário e imagem: 8 MB por versão; o painel hexadecimal mostra até 64 KB.
- Relatório interativo: até 30 MB de dados dos arquivos modificados.

Os limites evitam que a interface ou um HTML compartilhado tente carregar arquivos grandes em memória. Os originais continuam intactos durante a comparação.
