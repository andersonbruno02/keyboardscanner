# Adaptação para o teclado Roland Juno
Autorizada da Roland se recusou a consertar o teclado, alegando ser um modelo muito antigo e não ter mais as peças em estoque.  
Graças a esse codigo consegui tirar som dessas teclas novamente usando:  
**Arduino Mega >[Hairless MIDI](https://projectgus.github.io/hairless-midiserial/)> [loopMIDI](https://www.tobias-erichsen.de/software/loopmidi.html) > [kontakt](https://www.native-instruments.com/en/products/komplete/samplers/kontakt-6/).**  </p>
É necessario utilizar a biblioteca [DIO2](https://github.com/FryDay/DIO2) para que tudo funcione corretamente.</p>
</p>
Um grande agradecimento ao Daniel Moura criador desse codigo o qual eu estou adaptando e também ao Jacob Hobbs o qual estou utilizando muito de suas sugestões de melhoria para o codigo.</p>

**Alterações do codigo original:**
1. Estou utilizando a função micros no lugar da millis, segundo Jacob isso proporciona uma sensibilidade mais fluida.
2. Ao apertar uma tecla com força minima foi atribuido um valor minimo no lugar de zero, o que antes dava a impressão da tecla não ser apertada, agora é tocado um som bem baixo.
3. Estou fazendo algumas alterações no pedal de sustenido pois antes não havia funcionado comigo.
4. Em um futuro proximo pretendo tentar implementar no codigo a utilizaçao dos potenciometros e dos botões para ajudar no controle do kontakt 
