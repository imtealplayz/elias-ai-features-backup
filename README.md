# Elias AI Features Backup

Source snapshot: `imtealplayz/elias` at commit `a712176307fbb1e2dcc69debb83963867e3c0dc8`.

This repository preserves the AI and utility feature source that is being separated from the main Elias bot.

## Included

### Conversational AI
- Gemini reply generation
- Groq fallback replies
- Gemini/Groq rate-limit handling
- Persistent AI memories and memory extraction
- Targeted memory forgetting and name-preference handling
- Recent conversation context
- Live web context for current-information requests
- AI conversation summarization
- Natural-language currency conversion
- Crypto price/conversion handling
- Natural-language reminders with persistent scheduling

### Discord utilities
- `.afk` handling and AFK runtime
- `.crc` / Crunchyroll currently-watching and last-watch tracking
- `.main`, `.unmain`, `.semi`, `.unsemi`, `.block`, `.unblock`, `.channels` channel modes
- Legacy memory/help command handling
- Tic-Tac-Toe AI/game logic

## Database

`supabase/ai-features-schema.sql` preserves the database tables used by the above AI/utility features. It is a schema backup only and does not modify the live Supabase project.

## Note

`src/db.js` is the shared Elias database helper, so it also contains unrelated stock/economy database functions. Those are included because the preserved AI/utility modules depend on the shared helper.
