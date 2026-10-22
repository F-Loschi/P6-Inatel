- São redes geradas a partir de outras redes
- Redes privativas
- Usa um dos octetos para diferenciar uma rede da outra
## Cálculo de Sub-Redes IPv4
- Permite dividir os blocos de endereços de redes em segmentos menores(sub-redes), dando uma maior flexibilidade de endereçamento ao administrador da rede
- Se era /24(256 endereçamentos), ao quebrar, eu tenho duas de /25(cada uma com 128 endereçamentos). Ao quebrar de novo, eu fico com dois de /26(cada um com 64 endereçamentos)
- Para dividir a rede em sub-redes, usa-se uma máscara de sub-rede adequada
- Para criar um endereço de sun-rede, toma-se bits do campo Host_Id, a partir do bit mais significativo, e os designa para o campo Net_Id da sub-rede
- A quantidade máxima de bits que podem ser emprestados é qualquer valor que deixe pelo menos 2 bits para o campo Host_Id