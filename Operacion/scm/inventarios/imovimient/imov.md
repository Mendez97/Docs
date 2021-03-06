---
layout: default
title: Movimientos de inventario
permalink: /Operacion/scm/inventarios/imovimient/imov
editable: si
---

# Movimientos de Inventario - IMOV

Esta aplicación permite la ejecución de los principales movimientos que afectan el inventario, tales como entradas por compra, salidas por remisiones, salidas por consumo.  

![](imov1.png)

**Documento:** Nombre de documento parametrizado con anterioridad en la aplicación **BDOC**.  
**Número:** Numero consecutivo del movimiento.  
**Ubicación:** Número de ubicación de la empresa en donde se encuentra el producto.  
**Concepto:** Concepto del movimiento.  
**Motivo:** Motivo del movimiento.  
**Fecha:** Fecha en la que se realizará el movimiento.  
**Tercero:** Tercero asociado al movimiento.  
**Nombre de Tercero:** Nombre de tercero asociado al movimiento.  
**Moneda:** Tipo de moneda que se utilizara en el movimiento de inventarios.  
**Estado:** Estado en el que se encuentra el movimiento (Activo, procesado, Anulado).  
**Vendedor:** Tercero que está registrado como vendedor.  
**Tipo de precio:** Tipo de precio registrado con anterioridad en la aplicación **FBTP**.  
**Ubicación de destino:** Ubicación a donde será cargado el movimiento de productos.  

En el detalle:

![](imov2.png)

**Renglón:** Renglón de detalle asociado al movimiento.  
**Producto:** Código asignado al producto, anteriormente parametrizado en **BPRO**.  
**Nombre del Producto:** Nombre de producto.  
**Cantidad:** Cantidad por producto.  
**Costo unitario:** Costo por unidad de producto.  
**Unidad Medida:** Hace referencia a la unidad de medida del producto ejemplo, nidad.  
**Localización:** Identificación numérica de la localización de un producto.  
**Característica:** Código de la característica que se puede atribuir al producto.  
**Presentación:** Forma de presentación del producto.  
**Vencimiento:** Fecha de vencimiento del producto.  
**Control:** Número de serial o consecutivo asignado a productos que vende la empresa y poder así identificarlos y llevar un control sobre ellos.  
**Lote:** Si los productos pertenecen a un lote en específico.  


## [Vista Previa](http://docs.oasiscom.com/Operacion/scm/inventarios/imovimient/imov#vista-previa)

La funcionalidad de _Vista Previa_ muestra los movimientos de inventario despachado, relacionando la información diligenciada en la aplicación.  

Para acceder a la vista previa, seleccionamos un registro del maestro de la aplicación y damos click en el botón _Presentación preliminar_ ![](lupa.png) ubicado en la barra de herramientas.  

![](imov9.png)

En seguida, se podrá ver el documento del movimiento de inventario seleccionado.  

El documento podrá ser exportado en formato de Excel, PDF o Word.  

![](imov10.png)

Al exportarlo en formato PDF.  

![](imov11.png)


## [Producción](http://docs.oasiscom.com/Operacion/scm/inventarios/imovimient/imov#producción)

Una vez validada la información del pedido se procesa el documento y se realiza un traslado de los insumos a la bodega requerida, para realizar este movimiento se debe ingresar a la aplicación _IMOV – movimientos de inventarios_.  

**Documento:** SA correspondiente a salida de inventario.  
**Ubicación:** 3 correspondiente a la ubicación de donde saldrá la mercancía.  
**Concepto:** TR correspondiente a traslado.  
**Tercero:** Tercero correspondiente.  
**Ubicación Destino:** 1 La ubicación a la que se requiere llevar la mercancía.  
**Documento1:** LD Documento del pedido creado automáticamente en **LPED**.  
**Número1:** 2 Número del pedido correspondiente al campo anterior.  
**Ubicación1:** 1 Ubicación del pedido correspondiente al campo anterior.  

![](imov3.png)

Cabe resaltar que, si al momento de realizar este registro no recordamos el número del pedido, en el campo número 1 se puede realizar doble clic y el sistema abre una ventana emergente con los pedidos relacionados a ese tercero y en esa respectiva ubicación:  

![](imov4.png)

Se da clic en el botón aceptar y el sistema nos arroja el 2 en el campo número1.  

Al guardar el registro el sistema nos arroja automáticamente el detalle de acuerdo al pedido generado anteriormente, cabe resaltar que para que el sistema realice esto es necesario diligenciar los campos de color naranja de la imagen anterior para identificar a que pedido está asociado.  

![](imov5.png)

Se procesa el registro   

![](imov6.png)


## [Inventario Periódico e Inventario Cíclico](http://docs.oasiscom.com/Operacion/scm/inventarios/imovimient/imov#inventario-periódico-e-inventario-cíclico)

En la aplicación **IMOV** se validarán los documentos de ajuste generados por la aplicación [**IFAJ - Genera Ajustes**](http://docs.oasiscom.com/Operacion/scm/inventarios/ifisico/ifaj), estos deberán ser procesados con el fin de adecuar correctamente el inventario realizado.  

Para consultar los documentos filtraremos por la fecha en que se realizó el inventario.  

![](imov7.png)

En la aplicación se generó un documento _EN - Entradas al inventario_ por concepto _EA - Entrada por ajuste_, el cual corresponde a las unidades que se encuentran físicamente pero que no estaban registradas en el sistema. Por otro lado, también se generó el documento _SA - Salidas del inventario_ por concepto _SA - Salida por ajuste_, el cual corresponde a las unidades de más que se encuentran registradas en el sistema pero que no existen físicamente. En el detalle de cada documento se podrán ver los productos a los cuales se les realizó ajuste.  

Validada la información procesamos los documentos dando click en el botón _Procesar_ ![](procesar.png) ubicado en la barra de herramientas, esto permitirá que el inventario sea ajustado correctamente.  

![](imov8.png)

Para verificar que el inventario haya sido ajustado correctamente ingresaremos a la aplicación [**ISPL - Saldos por Localización**](http://docs.oasiscom.com/Operacion/scm/inventarios/isaldo/ispl#inventario-periódico-e-inventario-cíclico).  



