# Roblox Auto-Walk & Speed Booster Script

A lightweight, production-ready Luau script for Roblox that injects a toggleable Graphical User Interface (GUI) into the player's screen. It automates moving forward at an extreme velocity, perfect for simulator games, testing physics, or automating path movements.

---

## 🚀 Features

*   **One-Click Automation:** Instantly toggles continuous forward movement with a clean screen button.
*   **Insane Speed Boost:** Changes default character speed to a custom value (`100,000` by default).
*   **Respawn Proof:** Automatically binds to the new character configuration when the player resets or respawns (`ResetOnSpawn = false`).
*   **Frame-Rate Independent:** Uses `RunService.RenderStepped` for smooth execution tied directly to the client's rendering loop.

---

## 🛠️ Installation & Usage

1. Open your Roblox exploit executor (e.g., Wave, Solara) or use it inside **Roblox Studio** for local testing.
2. Create a new **LocalScript** if you are testing inside Studio (place it in `StarterPlayerScripts` or `StarterGui`).
3. Copy the script code and paste it into your editor.
4. Execute the script or start the game.
5. Click the green **"Ходить вперёд"** button at the bottom of the screen to activate. Click the red **"Стоп"** button to halt.

---

## ⚙️ Configuration

You can easily customize the speed behavior by modifying the variables at the top of the script:

```lua
-- Change this value to adjust your boost velocity
local boostedSpeed = 100000 

-- Customize UI button placement or size if needed
button.Size = UDim2.new(0, 150, 0, 50)
button.Position = UDim2.new(0.5, -75, 0.9, 0)
```

---

## 📝 Code Breakdown

*   **`ScreenGui.ResetOnSpawn = false`**: Ensures that the button element does not disappear from the UI layout when the character dies.
*   **`Humanoid:Move()`**: Continuously translates the character model relative to its `HumanoidRootPart.CFrame.LookVector` orientation.
*   **`RenderStepped`**: Fires every frame before rendering, ensuring the auto-walk prompt never stutters or drops input signals.

---

## ⚠️ Disclaimer

Using scripts that drastically modify `WalkSpeed` (especially values like `100,000`) in public servers will likely trigger server-side Anti-Cheats (such as rubber-banding protections or instant kicks). Use this script responsibly in your own places, private servers, or games with disabled physics checks. 
