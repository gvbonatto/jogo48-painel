# Painel do Jogo de 48

Painel web do terminal de pagamento "Jogo de 48" (ESP32-P4 + RS485).

- Fala com o terminal por MQTT (broker público com TLS).
- Tudo é cifrado de ponta a ponta com AES-256-GCM usando o **código do painel**
  mostrado no terminal (Operador › Online). A página não guarda nenhum segredo:
  sem o código ela não lê nem comanda nada.
