# Bus de mensajes
Wrapper de EventEmitter para emitir y escuchar eventos asincronicos. Los valores retornados por los suscriptores son ignorados.

![alt text](https://github.com/poximan/mom-nucleo/tree/master/imagenes/nucleo.png "Arquitectura")<br/>

## Caso de estudio
Aqui https://github.com/poximan/mama_node hay caso de estudio completo que implementa este modulo.<br/>

## Parametros
no necesita

## Modo de uso

### Alta bus de mensajes
```
var bus = require("mom-bus-comunic");
```
Con esto se solicita una instancia de bus mensajes, para emitir o escuchar mensajes en el. No tiene dependencias con el negocio.

### emitir
```
bus.emit({nombre_evento}, {mensaje});
```
emision de un evento, el comportamiento es identico a https://nodejs.org/api/events.html#events_emitter_emit_eventname_args

### escuchar
```
bus.on({nombre_evento}, function({mensaje}) {
  // aqui va el codigo que debe ejecutarse para este evento
  });
```
escucha de un evento, el comportamiento es identico a https://nodejs.org/api/events.html#events_emitter_on_eventname_listener
