# Simulador de chat — LiveCraft Bridge

Página de teste do [LiveCraft Client Bridge](https://github.com/joaopaulomsa). Ela **não**
se conecta a nada: apenas reconstrói o DOM que o YouTube Live Chat produz, para que o
observador do mod possa ser testado sem depender de presentes reais chegando numa live.

Acesse em `/live_chat/`.

## Como o mod aceita esta página

Por padrão o mod só injeta seu script em frames do YouTube. Para usar este simulador, crie
no perfil do Minecraft o arquivo:

```
config/livecraft_client_bridge/test-origin.txt
```

com uma linha contendo o host desta página. Continuam valendo HTTPS, porta padrão e a
exigência de que o caminho contenha `live_chat`.

**Apague esse arquivo ao terminar o teste** — enquanto ele existir, este host pode injetar
eventos no seu mundo.
