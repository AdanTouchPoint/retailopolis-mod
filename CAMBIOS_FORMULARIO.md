# Registro Desactivado

## Cambios Realizados

El formulario de registro inicial (captura de "leads") en la pantalla de inicio se ha desactivado para permitir que los usuarios vayan directamente a la selección de jugadores. 

Los cambios específicos en el archivo `app/components/SetupScreen.tsx` fueron los siguientes:

1. **Cambio de Estado Inicial**: Se modificó el valor por defecto del estado `step` (paso) en el componente de `1` a `2`. Esto hace que, al cargar la página, la interfaz salte directamente a la pantalla de selección de jugadores ("Step 2").
    ```typescript
    // Antes
    const [step, setStep] = useState<1 | 2>(1);
    
    // Ahora
    const [step, setStep] = useState<1 | 2>(2);
    ```

2. **Eliminación del Botón de Retorno**: Se eliminó el botón "← Volver" que se encontraba en el "Step 2", el cual permitía regresar al formulario de registro del "Step 1". Al removerlo, el usuario ya no puede navegar hacia atrás a la pantalla del formulario de manera manual.

Estos cambios logran que el formulario de recolección de datos sea completamente ignorado sin necesidad de borrar permanentemente el código, lo que facilita reactivarlo en el futuro si así se desea.
