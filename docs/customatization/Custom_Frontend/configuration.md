# /src/config.ts

This configuration file is where we receive the PLC elements to be monitored from the backend; the base interface tells us that the structure is as follows:

* `ID` : Name by which to identify the PLC element. (__Required__)
* `Name` : Name that is displayed on screen when the element is called. (__Required__)
* `Type` : Specify the type of element it is (Button, Light, Timer, Toggle). (__Required__)
* `Endpoint` : The Eset endpoint is the one that was defined and assigned from the backend to the PLC element. (opcional, si el caso aplica).
* `Command` : Endpoint to send commands, such as start or stop, just to give an example.
* `Variant` : Button colors, this is optional.
```typescript
// Ejemplo de estructura para un botón    
    {
        id: 'start',
        name: 'INICIO',
        type: 'button', // It doesn't need state, just a command.
        // endpoint: undefined, // Omitted because it is not readable
        command: '/start',
        variant: 'success',
    },
// Ejemplo para una bobina (foco/led/memoria/timer)
    {
        id: 'foco_amarillo',
        name: 'Foco Amarillo',
        type: 'light',
        endpoint: '/foco_amarillo',
        variant: 'danger'
    },
```

---

# /src/hooks/usePLCState.tsx
This file manages the connection and communication with the backend.

The modifications that can be made here include:

* The update interval at which the backend is queried/read/written to:
```typescript
    // Update every 1 second
    const interval = setInterval(() => {
      fetchAll().catch(err => console.error("Error en refresco automático:", err)); // We caught errors from the automatic refresh.
    }, 1000);
// Change 1000 to 3000 -> Update every 3 seconds
```