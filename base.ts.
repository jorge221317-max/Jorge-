<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ChatGPT + HeyGen Avatar</title>
  <style>
    body { font-family: Arial; margin: 20px; }
    input, button { padding: 10px; margin: 5px 0; width: 100%; }
    video { margin-top: 20px; width: 100%; max-width: 500px; }
  </style>
</head>
<body>
  <h1>Avatar HeyGen + ChatGPT 5-mini</h1>
  <input type="text" id="prompt" placeholder="Escribí tu mensaje aquí..." />
  <button onclick="generarVideo()">Generar video</button>

  <p id="respuesta"></p>
  <video id="video" controls></video>

  <script>
    async function generarVideo() {
      const prompt = document.getElementById("prompt").value;
      const res = await fetch("/generate", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({ prompt })
      });
      const data = await res.json();
      document.getElementById("respuesta").innerText = "ChatGPT dice: " + data.respuesta;
      document.getElementById("video").src = data.videoURL;
    }
  </script>
</body>
</html>
