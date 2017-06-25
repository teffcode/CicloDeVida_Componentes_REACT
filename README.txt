🐣  CICLO DE VIDA DE UN COMPONENTE 🐔 

   Se basa en:


	🍊  MONTADO:

		- Cuando se crea y se pone en la UI.
		- Tiene varios métodos:

			1. constructor(props):
			   - El constructor recibe los props y permite
			   - Inicializar el estado, bindear eventos
			
			2. componentWillMount():
			   - Se ejecuta desps del constructor 
			   - Permite ejecutar código antes de que el componente se renderice
			   - Aquí no hay DOM, no hay UI
			   - No realizar acciones asíncronas (peticiones HTTP)
			
			3. render():
			   - Se genera la UI
			   - Se instancian los elementos 
			   - Las etiquetas de HTML que usemos

			4. componentDidMount():
 			   - Peticiones AJAX
			   - Mapas de GoogleMaps por ejemplo
			   - Cosas que necesitemos del DOM
			     (Donde el DOM ya existe) 
			   

	🍊  ACTUALIZACIÓN:

		- Cuando el componente ya está creado
		  y se actualizan datos internos o externos.
		- Tiene varios métodos:

			1. componentWillReceiveProps(nextProps):
			   - Podemos validar si los props cambiaron
			   - Antes de que el componente se actualice
			
			2. shouldComponentUpdate(nextProps, nextState)
			   - Recibimos TRUE o FALSE
   			     TRUE: En el caso de que el componente necesite actualizarse
			     FALSE: En caso de que el componente NO necesite actualizarse

			3. componentWillUpdate(nextProps, nextState)
			   - Similar al anterior

			4. render()
			   - Se vuelve a renderizar el JSX de nuestro componente


			5. componentDidUpdate(prevProps, prevstate)
			   - Se puede volver a asignar algo	


	🍊  DESMONTADO:

		- Cuando el componente se va a eliminar.
		- Tiene algunos métodos:

			1. componentWillUnmount():
			   - Se ejecuta antes de que el componente se borre de la UI
			   - Permite limpiar para no tener problemas de memoria

