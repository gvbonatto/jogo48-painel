# Painel do Jogo de 48

Painel web do terminal de pagamento "Jogo de 48" (ESP32-P4 + RS485).

- Fala com o terminal por dois caminhos, ambos na porta 443 (passam pela maioria
  das redes): MQTT sobre WebSocket (broker público shiftr.io) e, de reserva,
  HTTPS pelo ntfy.sh. Se um cair, o outro entrega.
- Configurações são versionadas: a mais nova vence. Alteração feita com o
  terminal desligado fica guardada e é aplicada quando ele volta à internet.
- Tudo é cifrado de ponta a ponta com AES-256-GCM usando o **código do painel**
  mostrado no terminal (Operador › Online). A página não guarda nenhum segredo:
  sem o código ela não lê nem comanda nada.
