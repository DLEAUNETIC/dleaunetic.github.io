
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MAC-Formatierer</title>
    <script>
        function formatMAC() {
            let mac = document.getElementById("macInput").value;
            
            if (mac.length !== 12) {
                alert("Die MAC-Adresse muss genau 12 Zeichen lang sein.");
                return;
            }
            
            let formattedMac = mac.match(/.{1,2}/g).join(":");
            document.getElementById("formattedMac").innerText = formattedMac;
        }
    </script>
</head>
<body>
    <h2>MAC-Formatierer</h2>
    <p>Geben Sie eine unformatierte MAC-Adresse ein:</p>
    <input type="text" id="macInput" placeholder="z.B. 001122334455">
    <button onclick="formatMAC()">Formatieren</button>
    <p>Formatierte MAC-Adresse: <span id="formattedMac"></span></p>
</body>
</html>
