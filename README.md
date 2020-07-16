# T2
Calcular si una persona es mayor de edad 

- Se realiza programa para calcular si una persona es mayor de edad.
- Se instala el WebPack pasado por el profesor en clase, ya que no se uso la libreria de boostrap sola.
- Sin la libreria 

![5](https://user-images.githubusercontent.com/61033465/87612760-0c986580-c6d1-11ea-84fb-0f2b0384e352.png)

- Instalando la libreria

![5](https://user-images.githubusercontent.com/61033465/87613243-55045300-c6d2-11ea-86f4-b3309705f81f.png)

- Iniciando con el (npm run start)

![5](https://user-images.githubusercontent.com/61033465/87613280-7402e500-c6d2-11ea-82aa-2e3085489aa0.png)

- Cargado con la libreria

![6](https://user-images.githubusercontent.com/61033465/87613459-00ada300-c6d3-11ea-8697-1a5feb172f43.png)



 <!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>T2</title>
</head>

<body>
    <div class="container">
 

        <div class="card-deck">

            <div class="card">

            </div>
            <div class="card">
                <div class="card-body">
                    <h5 class="card-title">Identificar si una persona es mayor de edad</h5>
                    <div class="form-inline">
                        <label for="">Por favor ingrese su edad</label>
                        <input type="text" class="form-control" id="Edad">
                        <div class="form-inline">
                            <button class="btn btn-success" onclick="main()">Validar</button>
                        </div>
                        <div>
                            <span>Resultado : </span>
                            <h5 id="result2" class=""> </h5>
                        </div>
                    </div>

                </div>
            </div>

        </div>

    </div>

</body>
<script>
    /*Ejercicio 2*/
    const edad = document.getElementById("Edad");
    const message = document.getElementById("result2");

    function main() {

        const age = parseInt(edad.value);

        if (!age) {
            error();
        } else {
            evaluate(age);
        }
    }

    function error() {

        message.innerHTML = "Por favor ingrese una edad valida";
        message.classList.add("text-danger");
    }

    function evaluate(edad) {

        if (edad < 18) {
            menor(edad);
        } else {
            mayor(edad);
        }
    }

    function mayor(edad) {
        message.classList.remove("text-danger");
        message.innerHTML = ` Tienes ${edad} años, eres mayor de edad`;
        message.classList.add("text-success");
    }

    function menor(edad) {
        message.classList.remove("text-danger");
        message.innerHTML = ` Tienes ${edad} años, eres menor de edad`;
        message.classList.add("text-info");

    }
</script>

</html>


