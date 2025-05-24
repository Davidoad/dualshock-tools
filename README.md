# dualshock-tools
git clone https://github.com/yourusername/dualshock-tools.git
cd dualshock-tools
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>DualShock Tools</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>DualShock Tools</h1>
  <p>Test your controller and view input data.</p>
  <script src="script.js"></script>
</body>
</html>
window.addEventListener("gamepadconnected", (e) => {
  console.log("Gamepad connected:", e.gamepad);
});

function updateGamepad() {
  const gamepads = navigator.getGamepads();
  const gp = gamepads[0];
  if (gp) {
    console.log("Axes:", gp.axes);
    console.log("Buttons:", gp.buttons.map(btn => btn.pressed));
  }
  requestAnimationFrame(updateGamepad);
}

updateGamepad();
git add .
git commit -m "Initial site with Gamepad API"
git push origin main
