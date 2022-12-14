# appmovilesFinal

Se agrego la pantalla distribucion.js 

la misma realiza un mapstatetoprops hacia dogpublicfilterDB

la misma la trae del store de redux.

Se declaro una funcion actualizarListaFotos(0) que permite traer todas las fotos.

Se declaro una funcion submit(filterText) recibe por parametro el valor del tipo de estado de perro (transitar, perdidos, encontrados, adoptar)

la misma va a setear el valor contenido en filterData:
   const submit = (filterText) => {
    //adoptar 0 //transitar 1 //perdidos 2  // encontrados 3
    if (filterText==""){
      setfilterData(props.dogsPublicFilterDB)
      
    }
    else{
      setfilterData(props.dogsPublicFilterDB.filter(e=>e.estado==filterText))
    }

  }
  
Luego el flatlist recibe el filterData y cuando hace el submit permite indicar el cambio
