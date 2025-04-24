 PedidosApp es un sistema de gestión de pedidos que calcula automáticamente el costo y método de envío basado en reglas de negocio.

 Proceso Principal:
     
     Entrada de Datos:
El usuario completa el formulario:

Nombre del cliente (txtCliente).

Tipo de producto (cmbProducto: tecnología, accesorio o componente).

Peso (nudPeso), distancia (nudDistancia), y urgencia (chkUrgente).

    Cálculo de Envío:

Al hacer clic en "Calcular", se crea un objeto Pedido.

La clase EntregaFactory decide el método de envío usando estas reglas:

Dron: Si es producto tecnológico y urgente (costo: $20/km).

Motocicleta: Para accesorios o por defecto (costo: $10/km).

Camión: Si es componente o peso > 10kg (costo: $5/km).


    Resultado:

Muestra en lblResultado el método seleccionado y el costo total.


    Componentes Clave:

    Patrones de Diseño:

Factory Method (EntregaFactory): Crea la estrategia de envío.

Singleton (RegistroPedidos): Gestiona los pedidos globalmente.

      Validaciones:

Campos obligatorios (nombre, producto seleccionado).

Manejo de errores 









