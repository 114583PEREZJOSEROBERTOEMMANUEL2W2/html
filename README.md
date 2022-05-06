<!doctype html>
<html lang="en">

<head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.1/dist/css/bootstrap.min.css"
        integrity="sha384-zCbKRCUGaJDkqS1kPbPd7TveP5iyJE0EjAuZQTgFLD2ylzuqKfdKlfG/eSrtxUkn" crossorigin="anonymous">


    <title>Alta vuelos</title>
</head>

<body>
    <ul class="nav">
        <li class="nav-item">
            <a class="nav-link active" href="index1.html">Home</a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="index2.html">Galería</a>
        </li>
        <!-- <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item">
            <a class="nav-link disabled">Disabled</a>
        </li> -->
    </ul>

    </div>
    <div class="container-fluid bg-info py-5">

        <div class="container text-white">
            <h1 class="display-3">Bienvenido</h1>
            <p class="lead">Formulario de Alta de Vuelo</p>
        </div>
    </div>

    <div class="container">
        <form id="form-alta" action="">
            <div class="form-row">
                <div class="form-group col-lg-6 col-sm-12">

                    <label for="inputName">Nombre:</label>
                    <input type="text" class="form-control" name="inputName" id="inputName">
                </div>

                <div class="form-group col-lg-6 col-sm-12">

                    <label for="inputDestiny">Destino:</label>
                    <input type="text" class="form-control" name="inputDestiny" id="inputDestiny" placeholder="ej: Buenos Aires">
                </div>

                <div class="form-group col-lg-6 col-sm-12">
                    <label for="listType">Tipo de vuelo:</label>
                    <select name="listType" class="form-control" id="listType">
                        <option value="">Selecione</option>
                        <option value="Argentina">Argentina</option>
                        <option value="Chile">Chile</option>
                        <option value="Espana">España</option>
                        <option value="USA">Estados Unidos</option>
                    </select>
                </div>

                <div class="form-group col-lg-6 col-sm-12">
                    <label for="inputPrice">Costo:</label>
                    <input type="money" class="form-control" name="inputPrice" id="inputPrice">
                </div>

                <div class="form-group col-lg-12 col-sm-12">
                    <label for="selectClass">Clase:</label>
                    <select name="selectClass" class="form-control" id="selectClass">
                        <option value="">Seleccione</option>
                        <option value="first">Primera clase</option>
                        <option value="economic">Ecónomica</option>
                        <option value="standard">Estándar</option>
                    </select>
                </div>

                <div class="form-group col-lg-4 col-sm-12">
                    <label for="inputOrigin">Origen</label>
                    <input type="city" class="form-control" name="inputOrigin" id="inputOrigin">
                </div>

                <div class="form-group col-lg-4 col-sm-12">
                    <label for="inputDate">Fecha:</label>
                    <input type="date" class="form-control" name="inputDate" id="inputDate" min="2022-04-25">
                </div>

                <div class="form-group col-lg-4 col-sm-12">
                    <label for="inputTime">Hora:</label>
                    <input type="time" class="form-control" name="inputTime" id="inputTime">
                </div>
                <div class="form-group col-lg-6 col-sm-12">
                    <button type="button" class="btn btn-success" id="save">Enviar</button>
                </div>

            </div>
        </form>
    </div>





    <script src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.slim.min.js"
        integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj"
        crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js"
        integrity="sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN"
        crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.6.1/dist/js/bootstrap.min.js"
        integrity="sha384-VHvPCCyXqtD5DqJeNxl2dtTyhF78xXNXdkwX1CZeRusQfRKp+tA7hAShOK/B/fQ2"
        crossorigin="anonymous"></script>



    <script src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/jquery-validation@1.19.3/dist/jquery.validate.js"></script>




    <script>
        $(document).ready(function () {
            $("#save").click(function () {
                if ($("#form-alta").valid()) {
                    alert("Todo ok");
                }
                else { alert("Error"); }
            })

            $("#form-alta").validate({


                rules: {
                    inputName: {
                        required: true,
                        minlength: 3,
                        maxlength: 25
                    },
                    
                    inputDestiny: {
                        required: true,
                        minlength: 4,
                    },

                    listType: {
                        required: true,

                    },

                    inputPrice: {
                        required: true,
                        min: 2000,                        
                    },

                    selectClass: {
                        required: true
                    },

                    inputOrigin: {
                        required: true,
                        minlength: 4
                    },

                    inputDate: {
                        required: true
                    },

                    inputTime: {
                        required: true
                    },
                },

                debug: true
            })
        })
    </script>

</body>

</html>
