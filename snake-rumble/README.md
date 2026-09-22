# Snake Rumble 🐍

A snake.io-style multiplayer-feel arena game built for **Facebook Instant Games** (also runs in any browser).

## Game rules
- Eat glowing orbs to grow longer. As you grow you **level up** (Lv 1 → Lv 14).
- If a snake's **head (mouth) touches another snake's body**, the snake that hit dies.
- A dead snake bursts into **gold coins** along its whole body. Eat them to grow fast.
- Head-to-head: the smaller snake dies.
- Hitting the red arena wall kills you.
- **Boost** (hold mouse / Space / ⚡ button on phones) makes you fast but costs length.
- Every KO (kill) counts toward **KO Training**, which unlocks new skins (Zebra 3, Ninja Star 10, Galaxy 25, Gold King 50).
  Account level unlocks more (Candy Lv 3, Lava Lv 5, Frost Dragon Lv 10).
- Game over screen shows rank, top 4, KOs, best streak, next unlock and XP.

Controls: mouse or touch to steer, arrow keys / A-D also work.

## Files
| File | What it is |
|------|------------|
| `index.html` | The whole game (HTML + CSS + JS in one file). It loads the Facebook SDK `fbinstant.7.1.js` |
| `fbapp-config.json` | Facebook Instant Games config (landscape, challenge message template) |

## Test on your computer
Just open `index.html` in Chrome. Without Facebook, the game still works: progress is saved in the browser.

## Upload to Facebook (Bangla)
1. **developers.facebook.com** এ যাও → *My Apps* → *Create App* → টাইপ **Gaming** সিলেক্ট করো → অ্যাপের নাম দাও (যেমন: Snake Rumble)।
2. অ্যাপ ড্যাশবোর্ডে **Instant Games** প্রোডাক্ট *Set up* করো।
3. এই ফোল্ডার থেকে zip বানাও (zip এর ভিতরে সরাসরি `index.html` থাকতে হবে, ফোল্ডার না):
   ```bash
   cd snake-rumble
   zip -r ../snake-rumble.zip index.html fbapp-config.json
   ```
   Windows এ: `index.html` আর `fbapp-config.json` দুটো সিলেক্ট করে Right click → *Send to → Compressed (zipped) folder*।
4. **Instant Games → Web Hosting** এ গিয়ে *Upload Version* চাপো → zip ফাইলটা দাও → আপলোড শেষ হলে ⭐ (*Push to Testing*) চাপো।
5. ফোনে/কম্পিউটারে Facebook এ গিয়ে টেস্ট করো (Web Hosting পেজে যে লিংক দেয়)।
6. **Details** ট্যাবে গেমের নাম, বর্ণনা, আইকন (1024×1024), স্ক্রিনশট দাও, Category = *Arcade*।
7. সব ঠিক থাকলে *Push to Production* করো এবং **Submit for Review** দাও। Facebook approve করলে সবাই খেলতে পারবে।

Optional: Instant Games → **Leaderboards** এ `BestLength` নামে একটা leaderboard বানালে গেম অটোমেটিক সেখানে স্কোর পাঠাবে।

On Facebook the game also uses the player's Facebook name and photo, saves progress to their Facebook account, and shows **Challenge** (send a challenge to a friend in Messenger) and **Share score** buttons.
