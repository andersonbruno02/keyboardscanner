# Adaptação para o teclado Roland Juno
Autorizada da Roland se recusou a consertar o teclado, alegando ser um modelo muito antigo e não ter mais as peças em estoque.  
Graças a esse codigo consegui tirar som dessas teclas novamente usando:  
**Arduino Mega >[Hairless MIDI](https://projectgus.github.io/hairless-midiserial/)> [loopMIDI](https://www.tobias-erichsen.de/software/loopmidi.html) > [kontakt](https://www.native-instruments.com/en/products/komplete/samplers/kontakt-6/).**  
É necessario utilizar a biblioteca [DIO2](https://github.com/FryDay/DIO2) para que tudo funcione corretamente.</p>
</p>
Um grande agradecimento ao Daniel Moura, o criador desse codigo o qual eu estou adaptando e também ao Jacob Hobbs o qual estou utilizando muito de suas sugestões de melhoria para o codigo e para Gustavo Silveira o qual estou utilizando parte do seu codigo para implementar control change.</p>

**Alterações do codigo original:**
1. Estou utilizando a função micros no lugar da millis, segundo Jacob isso proporciona uma sensibilidade mais fluida.
2. Ao apertar uma tecla com força minima foi atribuido um valor minimo no lugar de zero, o que antes dava a impressão da tecla não ser apertada, agora é tocado um som bem baixo.
3. Pedal de sustenido funciona por control change.
4. Pitchbend wheel e modulation wheel funcionais
5. Em breve adição de mais botões e potenciometros para control change</p>
 
**Placa:**</p>
![arduino](https://raw.githubusercontent.com/andersonbruno02/keyboardscanner/master/Arduino%20Mega.jpg)
<p>O fio amarelo esta ligado na porta 21 do arduino
<p>O fio vermelho esta ligano na porta GND
<p>O curto da porta 21 com ground ativa o pedal sustenido
