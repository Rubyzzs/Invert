<?php
    // Verifica se a string foi submetida pelo formulário
    if (isset($_POST['string'])) {
        // Inverte a string usando um loop
        $string_invertida = "";
        for ($i = strlen($_POST['string']) - 1; $i >= 0; $i--) {
            $string_invertida .= $_POST['string'][$i];
        }
    }
?>

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <title>Inverter string</title>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Importa os arquivos CSS do Bootstrap -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" />
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap-theme.min.css" />
</head>
<body>
    <div class="container">
        <div class="row">
            <div class="col-sm-6 col-sm-offset-3">
                <h1>Invertendo!!!</h1>
                <form method="post"  accept-charset="UTF-8">
                    <div class="form-group">
                        <label for="string">Digite algo:</label>
                        <input type="text" class="form-control" name="string" id="string" />
                    </div>
                    <div class="form-group text-right">
    					<button type="submit" class="btn btn-primary">Inverter</button>
						<?php
							// Se a string invertida existe, exibe na tela
							if (isset($string_invertida)) {
								echo "<p><b>Invertido: " . $string_invertida . "</b></p>";
							}
						?>
					</div>
                </form>
            </div>
        </div>
    </div>
    <!-- Importa os arquivos JavaScript do Bootstrap -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
</body>
</html>
