# 💰 RBAvatar Market & Affiliate System (`package-market`)

Turn your Roblox experience into a passive income generator. This package provides a plug-and-play, secure way to sell RBAvatar Global Skins directly within your game.

By using this package, you can earn a **40% Affiliate Commission** on every skin sold through your experience, paid automatically by Roblox.

## 🚀 Why Use This Package?

- **Earn Robux (40% Cut):** When a player sees a cool RBAvatar skin in your game and buys it via this system, Roblox's `MarketplaceService` automatically splits the revenue: 30% to the Creator, **40% to YOU (the Game Owner)**, and 30% to Roblox.
- **100% Safe & Transparent:** The code is completely open-source. No hidden fees, no backdoors. It utilizes native Roblox API (`PromptPurchase`) to handle transactions securely.
- **Optional & Modular:** This package is completely decoupled from the `package-aura` system. You can use the visual auras without selling them, or you can sell skins without using the auras. It's entirely up to you.
- **Global Avatars:** Players who purchase skins here receive them in their primary Roblox Inventory and can wear them in _any_ game across the platform.

## 📂 How It Works

The system is designed to be as lightweight as possible. It primarily uses Roblox's `MarketplaceService:PromptPurchase()` function.

We provide examples of how to implement this via:

1. **Screen GUI (Shop Buttons):** A standard shop interface where players can browse and buy skins.
2. **Proximity Prompts:** Allowing players to walk up to an NPC (or another player wearing the skin) and press "E" to buy the outfit instantly.

## 🛠️ Installation

1. Download the **RBAvatar Market Package** from the Roblox Toolbox (or copy scripts from this repository).
2. Place the UI components into `StarterGui` or the Proximity Prompt scripts into your designated parts/NPCs.
3. Open the main script and replace the `AVATAR_ASSET_ID` variable with the actual ID of the skin you wish to promote.

```lua
-- Example implementation
local MarketplaceService = game:GetService("MarketplaceService")
local player = game.Players.LocalPlayer
local AVATAR_ASSET_ID = 123456789 -- Replace with the RBAvatar skin ID

script.Parent.MouseButton1Click:Connect(function()
    MarketplaceService:PromptPurchase(player, AVATAR_ASSET_ID)
end)
```

## 🤝 Synergy with `package-aura`

We highly recommend using this alongside our [package-aura](https://github.com/RBAvatar/package-aura) repository. When players see the stunning visual effects of an RBAvatar skin running in your game, they are much more likely to click the buy button—earning you that 40% commission!

## ⚖️ License

MIT License - Free to use in any Roblox experience.
