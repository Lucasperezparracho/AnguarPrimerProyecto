# Angular
En este ejemplo se cree un contador que decrementa o incrementa en 1
clickando unos botones.

Es un ejemplo simple peronos sirve para ver lo potente que es angular
gracias a sus componentes.

### Contador
Este componente implementa un contador que se puede incrementar y decrementar. La variable `contador` se actualiza en respuesta a los clics en los botones de incremento y decremento.

En la clase `app.component.ts`
```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-counter',
  templateUrl: './counter.component.html',
  styleUrls: ['./counter.component.css']
})
export class CounterComponent {
  contador: number = 0;
    //incrementa
  increment() {
    this.contador++;
  }
    //decrementa
  decrement() {
    this.contador--;
  }
}
```
## 
Este archivo de plantilla HTML muestra el valor actual del contador y proporciona botones para incrementar y decrementar el contador.

En la clase `counter.component.html`

````angular2html
<p>Contador: {{ contador }}</p>
<button (click)="increment()">Incrementar</button>
<button (click)="decrement()">Decrementar</button>

````
Este componente CounterComponent es un ejemplo de cómo se puede actualizar una 
variable (contador) desde varios componentes en Angular. Cuando se hace clic en los 
botones de incremento o decremento, la variable contador se actualiza y se refleja 
automáticamente en la plantilla HTML. Esto demuestra la comunicación efectiva entre 
diferentes componentes en una aplicación Angular.
