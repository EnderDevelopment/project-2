# Minecraft Bedrock Economy Add-On

Community Market is a Minecraft Bedrock economy add-on made from a behavior pack and a resource pack. It adds a persistent player wallet, a global item market, player shop listings, coin transfers, and an in-game Market Ledger menu.

## Install

1. Use a Minecraft Bedrock world or Dedicated Server that supports behavior packs and the Script API. This add-on is not compatible with Java Edition servers.
2. Import or copy both `CommunityMarket_BP` and `CommunityMarket_RP` into the world’s available packs.
3. Enable both packs for the world. Enable the required Script API or Beta APIs experiments if your host requires them.
4. Start the world. The behavior pack uses `@minecraft/server` 1.16.0 and `@minecraft/server-ui` 1.3.0.

## Use

1. On first join, receive a locked Market Ledger and a $100 starting balance. Use the ledger or type `!market` to open the menu.
2. Choose Global Market to browse player and trader listings, or sell supported items to the market trader.
3. Choose My Goods / Shops to list supported items for a total price or cancel an active listing and reclaim its items. Collection requires a free inventory slot.
4. Use Transfer Money to send coins to another online player.
5. Operators can stand on a chest and type `!setmarketportal` to make it a market portal. Players can tap the chest to open the market. Stand on the chest and type `!removemarketportal` to remove it. Operators can also use `!marketnpc` to open the market menu.

---

More open source project projects by EnderDevelopment: https://github.com/EnderDevelopment

Project page: https://dash.enderdevelopment.com/community/e982c1bc-0700-4fcd-8d3f-9ee209a6cf93?utm_source=github&utm_medium=readme&utm_campaign=auto_publish&utm_content=e982c1bc-0700-4fcd-8d3f-9ee209a6cf93
