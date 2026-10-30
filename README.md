# BMAH.lua  —  ALE-compatible rewrite  

Forked from: https://github.com/Youpeoples/Black-Market-Auction-House

## Updated for ALE by: Dad's MMO Lab

**ADMIN GUIDE:**
  1. Run **sql/BMAH_Up.sql** against **acore_world** to create the vendor NPC
  2. Copy this **BMAH.lua** to your **lua_scripts/** directory
  3. RESTART the worldserver (required for new creature_template rows to load)
  4. The DB table is created automatically on first load (acore_characters)
  5. Reload Lua: `.reload ale`  (in-game GM command)
  6. Spawn the NPC: `.npc add 2069430`
  7. Client addon: copy "**Client Files/AddOns/BlackMarketUI**" → "**<WoW>/Interface/AddOns/**"  
  NOTE: `.reload creature_template` will NOT load brand-new entries — full restart required.

**GM COMMANDS (whisper yourself or the NPC):**
- IMPORTANT: run  `.gm on`  in chat before using these  
  — IsGM() requires GM mode to be active, not just a high security level.
1. `bmah_fill`   — manually fill the auction table (only when empty)
2. `bmah_flush`  — award won items via mail and wipe the table
3. `bmah_diag`   — print system state to GM chat (use when NPC/gossip won't work)
