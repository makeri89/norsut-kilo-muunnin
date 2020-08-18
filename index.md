<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat&display=swap" rel="stylesheet">
    <title>Kiloista norsuiksi</title>
</head>
<body>
    <header>
        <h1>Muunna jokapäiväisessä elämässäsi vastaan tulevat suuret painot norsuiksi!</h1>
        <h3>Tällä muuntimella selvität kätevästi monenko norsun painoa mikäkin kilomäärä vastaa.</h3>
    </header>
    <main id="main">
        <p>
            <label>Syötä kilomäärä:</label><br>
            <input id="inputKilot" type="number" placeholder="14500000" oninput="Converter(this.value)"
                onchange="Converter(this.value)">kg
        </p>
        <h3>Syöttämäsi paino vastaa norsuissa</h3>
        <p>Aasiannorsunaaraita: <span id="outputAasiaNaaras"></span></p>
        <p>Aasiannorsu-uroksia: <span id="outputAasiaUros"></span></p>
        <p>Savanninorsunaaraita: <span id="outputSavanniNaaras"></span></p>
        <p>Savanninorsu-uroksia: <span id="outputSavanniUros"></span></p>
    </main>

    <script>
        function Converter(valNum) {
            document.getElementById('outputAasiaNaaras').innerHTML = (Math.round(valNum / 2700 * 100) / 100).toFixed(2);
            document.getElementById('outputAasiaUros').innerHTML = (Math.round(valNum / 4000 * 100) / 100).toFixed(2);
            document.getElementById('outputSavanniNaaras').innerHTML = (Math.round(valNum / 3000 * 100) / 100).toFixed(2);
            document.getElementById('outputSavanniUros').innerHTML = (Math.round(valNum / 6000 * 100) / 100).toFixed(2);
        }
    </script>
</body>
</html>
