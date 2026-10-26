# outer-joins-ministore

¿Por qué usaste LEFT JOIN para la Consulta 1 y no INNER JOIN? ¿Qué se perdería si usaras INNER JOIN?
-- Utilicé LEFT JOIN para conservar todos los registros de la tabla productos y visualizar sus ventas asociadas, tengan o no ventas registradas. Si utilizase INNER JOIN, perdería los productos sin ventas, ya que solo devolvería los registros que tienen coincidencias en ambas tablas.

¿Por qué usaste RIGHT JOIN para la Consulta 2? ¿Qué tabla está a la izquierda y cuál a la derecha en tu consulta?
-- Utilicé RIGHT JOIN porque el objetivo era conservar todos los registros de ventas y comprobar si tenían un producto asociado en el catálogo. La tabla de la izquierda es productos y la de la derecha es ventas. De esta forma, las ventas sin un producto correspondiente también aparecen, mostrando NULL en las columnas de productos.


¿Qué representan los valores NULL en cada resultado? Explicá con un ejemplo concreto de los datos qué significa que venta_id sea NULL en la Consulta 1 y que producto_id de productos sea NULL en la Consulta 2.
--Los valores NULL indican que no se encontró una coincidencia entre ambas tablas. En la primera consulta, cuando venta_id es NULL, significa que el producto existe en el catálogo pero no tiene ventas registradas. En la segunda consulta cuando producto_id de productos es NULL significa que existe una venta cuyo producto no figura en el catálogo, lo que indica un error de carga de datos.

¿Cuándo usarías FULL OUTER JOIN en un caso real de negocio?
-- En un caso real de negocio, utilizaría FULL OUTER JOIN para realizar una auditoría entre el catálogo de productos y las ventas registradas. Esto permitiría identificar tanto productos sin ventas como ventas sin productos asociados, detectando posibles inconsistencias que podrían afectar los resultados del análisis.
