# Gilberto Cavallini in isolamento h 24 dal 06/11/25
<html lang="it">
<head>
<meta charset="UTF-8">
<title>Orologio Gigi Cavallini</title>
<style>
  body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; }
  #timer { font-size: 2em; font-weight: bold; }
</style>
</head>
<body>

<h2>Tempo trascorso dal giorno scelto</h2>
<div id="timer"></div>

<script>
  // Imposta qui la data di partenza
  const startDate = new Date("2025-12-15T00:00:00");

  function updateTimer() {
    const now = new Date();
    const diff = now - startDate;

    const seconds = Math.floor(diff / 1000) % 60;
    const minutes = Math.floor(diff / (1000 * 60)) % 60;
    const hours = Math.floor(diff / (1000 * 60 * 60)) % 24;
    const days = Math.floor(diff / (1000 * 60 * 60 * 24));

    document.getElementById("timer").innerHTML =
      `${days} giorni, ${hours} ore, ${minutes} minuti, ${seconds} secondi`;
  }

  setInterval(updateTimer, 1000);
  updateTimer();
</script>

</body>
</html>
