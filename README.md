//  Ejemplo práctico que ilustra cómo implementar un sistema de notificaciones utilizando el paradigma basado en eventos en Node.js

const EventEmitter = require('events'); // [cite: 27, 37]

// 1. Crear el emisor de eventos extendiendo la clase base [cite: 38, 39]
class SistemaNotificaciones extends EventEmitter {}
const sistema = new SistemaNotificaciones(); // [cite: 40]

// 2. Registrar los listeners (observadores) para reaccionar al evento [cite: 41]
// Este bloque define qué hacer cuando ocurra el evento 'nuevoUsuario' [cite: 42]
sistema.on('nuevoUsuario', (nombre) => {
    console.log(`Notificación: El usuario ${nombre} se ha unido al sistema.`); // [cite: 43]
});

// 3. Disparar (emitir) el evento [cite: 122]
// En una aplicación real, esto sucedería tras una acción del usuario o señal de I/O [cite: 3]
sistema.emit('nuevoUsuario', 'Carlos');
