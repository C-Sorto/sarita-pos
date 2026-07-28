# Sarita POS

Demo público de un sistema de ventas creado para un kiosco de helados en El Salvador. La versión privada se utiliza todos los días para apoyar el registro de ventas y continúa mejorando a partir de las necesidades del negocio.

**[Probar el demo](https://c-sorto.github.io/sarita-pos/)**

> Este repositorio es exclusivamente demostrativo. Utiliza un catálogo de prueba, una vendedora ficticia y no guarda ventas en el sistema de producción.

## Problema que resuelve

El kiosco necesitaba una herramienta sencilla para registrar ventas desde un teléfono, reducir errores durante el cobro y consultar el resultado de la jornada sin depender de un sistema complejo.

Sarita POS organiza el proceso en un flujo corto: seleccionar productos, preparar la orden, elegir el método de pago, calcular el cambio y confirmar la venta.

## Funciones disponibles en el demo

- Catálogo organizado por categorías.
- Selección de productos, sabores y cantidades.
- Preparación y cancelación de órdenes.
- Métodos de pago: efectivo, tarjeta y Pedidos Ya.
- Cálculo automático del cambio.
- Validaciones antes de confirmar una venta.
- Resumen local del día por método de pago.
- Interfaz adaptable a teléfonos.
- Datos separados del entorno real.

## Mi aporte al proyecto

Mi participación se concentra en el análisis funcional y la operación del sistema:

- Identificación de necesidades junto al dueño y las vendedoras.
- Definición de reglas de negocio y del flujo de venta.
- Organización del catálogo y de los datos necesarios.
- Pruebas manuales de los casos de uso y validaciones.
- Detección, reporte y seguimiento de errores.
- Validación del sistema durante su uso diario.
- Propuesta y priorización de mejoras.
- Documentación y control de cambios con Git y GitHub.

Este proyecto demuestra mi capacidad para comprender un problema real, convertirlo en requisitos claros, probar una solución y acompañarla después de su puesta en uso.

## Tecnologías presentes en la solución

- HTML, CSS y JavaScript.
- Google Apps Script.
- Google Sheets.
- Git y GitHub.
- GitHub Pages para publicar el demo.

Las tecnologías anteriores describen la solución. Mi enfoque personal en este proyecto es el análisis, las reglas funcionales, las pruebas y la mejora continua.

## Cómo funciona el demo

```text
Usuario
  |
  v
Interfaz web en GitHub Pages
  |
  +--> Catálogo de demostración
  |
  +--> Venta simulada y resumen local

Producción: repositorio, datos y accesos separados
```

Las ventas simuladas permanecen en el navegador del visitante. El demo no contiene acceso al Google Sheet, al panel administrativo ni a la aplicación utilizada en el negocio.

## Capturas

<img width="424" height="518" alt="Selección de productos en Sarita POS" src="https://github.com/user-attachments/assets/9354f71b-2f39-41e7-ad8d-181d5ed537b3" />
<img width="429" height="395" alt="Proceso de cobro en Sarita POS" src="https://github.com/user-attachments/assets/dfd8db58-3163-4bd2-9509-22eced1123a1" />

## Ejecutarlo localmente

No requiere herramientas de compilación.

```bash
git clone https://github.com/C-Sorto/sarita-pos.git
cd sarita-pos
```

Después, abre `index.html` en un navegador.

## Próximas mejoras

- Documentar casos de prueba.
- Incorporar una guía visual completa del flujo.
- Mejorar accesibilidad y mensajes de validación.
- Registrar mejoras y errores mediante Issues.

## Autor

**Christian Sorto**

Estudiante de Ingeniería en Sistemas

[LinkedIn](https://www.linkedin.com/in/christian-sorto-cortez/)
