# IBM-Modelerflow-hands-on

# Introducción
Este tutorial explica cómo crear y evaluar gráficamente modelos de aprendizaje automático utilizando la función de SPSS Modeler flow en IBM® Watson™ Studio. Estos flujos proporcionan un entorno interactivo para construir rápidamente canalizaciones de aprendizaje automático que traten los datos desde la ingesta a la transformación hasta la construcción y evaluación de modelos, sin necesidad de ningún código. Este tutorial presenta los componentes de SPSS Modeler flow y explica cómo puede utilizarlos para crear, probar, evaluar e implementar modelos.

# Prerrequisitos
* Necesitas una cuenta de IBM Cloud. 
* Crear el servicio de IBM Watson Machine learning.
* Crear un servicio de IBM Cloud object storage.
* Crear el servicio gratuito de Watson Studio.
* Subir el conjunto de datos a Watson Studio, ubicados en la carpeta dataset.

# Crear el modelo en modeler flow

  1. Desde la pesataña de **Assets** o **Activos**, haga clic en añadir al proyecto.   <img width="133" alt="icono_addpjc" src="https://user-images.githubusercontent.com/46906169/85602284-d78a7d00-b614-11ea-8d5d-f34c3498fdaa.PNG">
  2. En la ventana **Seleccionar tipo de arrchivo**, seleccione **Modeler flow**.
  3. En la página **New modeler flow**, seleccione la pestaña **New**.
  
<img width="953" alt="new_modeler" src="https://user-images.githubusercontent.com/46906169/86167357-005eb680-badc-11ea-86d5-242a6e6e5f16.PNG">
  
  4. Importante seleccionar como runtime **IBM SPSS Modeler**
  5. Seleccione el data set desde nuestro equipo.
  
  ![subir el data set](https://user-images.githubusercontent.com/46906169/86168874-63e9e380-bade-11ea-8ee5-b7de2ff6ca48.png)
  
  6. Agrege nuestro data set al flujo.
  
  ![data import](https://user-images.githubusercontent.com/46906169/86169232-ea9ec080-bade-11ea-8d09-01030120c615.png)

  7. Abrimos la confuguración del nodo, nos paramos sobre el nodo y damos **clic derecho** y luego clic en **open**.
  8. Damos clic al boton. <img width="73" alt="change data asset" src="https://user-images.githubusercontent.com/46906169/86169833-db6c4280-badf-11ea-94da-fd0f5673c05b.PNG">
  9. Seleccionamos en la barra izquierda **Data assets** y luego **data set example.csv** que corresponde al archivo que cargamos previamente.
  10. Agregamos un nodo de tipo ***derive*** que se encuentra en la sección **Field Operations**.
  
  ![nodo derive](https://user-images.githubusercontent.com/46906169/86172245-ad88fd00-bae3-11ea-86d4-ae6937f09dae.png)

  11. Abrimos la confuguración del nodo, nos paramos sobre el nodo y damos **clic derecho** y luego clic en **open**.
  12. Damos un nombre en el campo **Derived Field Name** Na_to_K y damos entramos al campo de **Expression**.
  
  ![dervie configuraation](https://user-images.githubusercontent.com/46906169/86173732-09ed1c00-bae6-11ea-97cf-466bda777b80.png)
  
  13. En la sección de **Expression** ingresamos la expresión **'Na'/'K'** y damos clic al boton. <img width="78" alt="save" src="https://user-images.githubusercontent.com/46906169/86174178-cc3cc300-bae6-11ea-95c4-5df503325fef.PNG">
  
  14. Añadimos un nodo de tipo ***filter***  encuentra en la sección **Field Operations**.
  
  ![filter](https://user-images.githubusercontent.com/46906169/86174672-b380dd00-bae7-11ea-8de8-5d3c2ab39b46.png)

  15. Abrimos la confuguración del nodo, nos paramos sobre el nodo y damos **clic derecho** y luego clic en **open**.
  16. Seleccionamos en el area de **Select Fields** el Boton **Add Columns**.
  17. Marcamos las casillas de Na y K luego damos clic a **OK** para guardar cambios.
  <img width="335" alt="filter columns" src="https://user-images.githubusercontent.com/46906169/86177008-86cec480-baeb-11ea-9042-9fe8112dbca2.PNG">

  18. Añadimos un nodo de tipo ***type***  encuentra en la sección **Field Operations**.
![type](https://user-images.githubusercontent.com/46906169/86177299-ffce1c00-baeb-11ea-9911-60d36b3d6490.png)

  19. Abrimos la confuguración del nodo, nos paramos sobre el nodo y damos **clic derecho** y luego clic en **open**.
  20. En la columna **Role** cambiamos el tipo a **Target** y damos clic en el botón. <img width="78" alt="save" src="https://user-images.githubusercontent.com/46906169/86174178-cc3cc300-bae6-11ea-95c4-5df503325fef.PNG">
  
  ![type config](https://user-images.githubusercontent.com/46906169/86178239-a535bf80-baed-11ea-9204-3c73a515e762.png)

  21. Añadimos un nodo de tipo ***C5.0***  encuentra en la sección **Modeling**.
  
  ![c5](https://user-images.githubusercontent.com/46906169/86179468-ecbd4b00-baef-11ea-8fc9-3f7ef1d822e7.png)
  
  23. Corremos el modelo.
  ![play](https://user-images.githubusercontent.com/46906169/86179733-71a86480-baf0-11ea-90ee-bd36dbdf3bb9.png)
  

  



  










