# Painel do Bonatto 48

Painel web do terminal de pagamento "Bonatto 48" (ESP32-P4 + RS485), no mesmo
visual da tela do terminal: dashboard horizontal (máquina, vendas e configuração
lado a lado, sem rolar a página).

- Fala com o terminal por dois caminhos: MQTT (servidor privado EMQX e o público
  shiftr.io, os dois ao mesmo tempo) e, de reserva, HTTPS pelo ntfy.sh.
- Configurações são versionadas: a mais nova vence. Alteração feita com o
  terminal desligado fica guardada e é aplicada quando ele volta à internet.
- Tudo é cifrado de ponta a ponta com AES-256-GCM usando o **código do painel**
  mostrado no terminal (Operador › Online). O login do servidor privado também é
  derivado desse código. A página não guarda nenhum segredo: sem o código ela não
  lê nem comanda nada.
