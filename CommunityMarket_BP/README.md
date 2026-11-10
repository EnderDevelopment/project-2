# Community Market Behavior Pack

A Bedrock behavior pack for Minecraft 1.21.51 with a persistent server-side wallet, global listings, player shops, a starter ledger book, player-to-player coin transfers, and an NPC-style market buyback.

## Install

Use a Bedrock Dedicated Server host that supports behavior packs and the Script API. Aternos support depends on the server software available for your account; this pack is not a Java plugin and cannot run on Java/Paper/Purpur servers. Add both the `CommunityMarket_BP` behavior pack and the `CommunityMarket_RP` resource pack, enable both for the world, and enable Beta APIs / Script API experiments if the host requires them. The behavior pack imports `@minecraft/server` 1.16.0 and `@minecraft/server-ui` 1.3.0.

## Use

- The first-time player receives the custom `community_market:ledger` Market Ledger book and $100. Use the book or type `!market` to open the menu.
- Global Market shows catalog prices, available listings, and permits buying player listings or selling supported items to the market trader.
- To create a personal shop listing, open the book, choose `My Goods / Shops`, then `Create a listing`. Select a supported item, quantity, and total price. The selected items leave the inventory and are held by the market until sold.
- Buyers see the seller name and total price in the global listing menu. After a sale, the item goes to the buyer and the full price is added to the seller's wallet. A player cannot buy their own listing.
- To cancel an active shop listing, open `My Goods / Shops`, select the listing marked `Cancel`, and collect the item back. The player needs one free inventory slot.
- Supported shop items are iron ingots, gold ingots, diamonds, emeralds, oak logs, wheat, and cooked beef. Each listing can contain up to 64 items.
- Market buyback accepts the same items. Buyback is 70% of the current unit price; NPC listings are priced above the payout.
- Coin transfers go to online players.
- Operators stand on a chest and type `!setmarketportal` to add a portal. A floating red down arrow and gold `•Рынок•` label appear above it; tapping the chest opens the market. Use `!removemarketportal` while standing on that chest to remove the portal and label.
- Operators can use `!marketnpc` to open the same market menu.

## Compatibility notes

The ledger item is locked in the inventory and hidden from the Creative item menu. The script also checks online players periodically and restores a missing ledger when an inventory slot is available, covering loss through death, destruction, or other removal paths. Keep at least one free inventory slot if a removed book needs to be restored. Listings and balances persist in world dynamic properties. Shop items are held in the saved listing data while active. Portal labels are invisible armor stands with visible name tags and are restored when the world loads; the marker uses Minecraft's standard armor stand model rather than a custom model.
