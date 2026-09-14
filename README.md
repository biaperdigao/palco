# PALCO — captura de gesto

Ação de pré-lançamento. A pessoa liga a webcam, se move, e o movimento vira um
símbolo no vocabulário gráfico da marca.

**Como usar:** abra a página, autorize a câmera, levante uma das mãos com a palma
para a câmera e faça o gesto durante os 3 segundos de captura.

**Privacidade.** Nada é enviado. A página não faz nenhuma requisição de envio —
sem `fetch` de dados, sem formulário, sem armazenamento. As únicas requisições de
rede são downloads: a biblioteca MediaPipe Tasks Vision e os dois modelos de
detecção. O vídeo da câmera é processado dentro do navegador e não sai dele.

**Diagnóstico.** Tecla `D` ou o botão DIAGNÓSTICO abre o painel de medição, com o
dado cru visível e uma linha de resumo para copiar.

**Variantes por URL**, para comparar comportamentos:

| | |
|---|---|
| `?corrente=1` | parte o gesto em arcos quando o traço enche (161°) |
| `?raio=gesto` | o arco fica com o raio do gesto, não com a faixa da fonte |
| `?coesao=1` | aproxima os arcos e força conexão entre eles |
| `?enquadra=1` | enquadra e centraliza a composição no fim |
| `?anima=0` | desliga a inércia — o resultado aparece pronto |
| `?goo=0` | desliga a fusão nas juntas |
| `?escala=px` | limiares em pixels fixos em vez de escala de corpo |

Requer HTTPS (a câmera exige) e um navegador com WebGL. Testado em Chrome.
