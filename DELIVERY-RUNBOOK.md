# AI Kamai — Delivery Runbook (PRIVATE)

> Access keys live in this file only. Do not paste them into chats, notes, or messages
> to beyond — paste them only into the buyer's WhatsApp DM at delivery time.
> Rotated 2 Oct 2026: old keys (KAMAI-V7X2 / KIT-V9B2 + old Kit backups) were shared in a
> chat and are dead. If a key leaks again: tell beyond, one re-encrypt + redeploy rotates it.

## Live access keys

- Vault (₹499) primary key: `KAMAI-TJCQ`
- Agency Kit (₹999) primary key: `KIT-TAYY`
- Agency Kit backup key 1: `KIT-Y4VC`
- Agency Kit backup key 2: `KIT-MSNL`

Use the primary key in buyer links. Backups exist only so a lost/typo'd key never blocks
delivery; they are not for buyers.

## Delivery messages (copy-paste)

**Prompt Vault (₹499):**

> Payment mil gaya. Ye raha access link — kholo aur bookmark kar lo:
> https://somilsharma2000.github.io/aikamai/vault/?key=KAMAI-TJCQ
> Phone yaad rakh lega (ek baar khula to agli baar seedha khulega). Naye prompts add hote
> rahenge — lifetime updates free. Thanks!

**Agency Kit (₹999):**

> Payment received. Agency Kit access:
> https://somilsharma2000.github.io/aikamai/kit/?key=KIT-TAYY
> Playbook tab se shuru karo, phir Scripts. Koi tab atake to message kar dena.

**SaaS Starter Kit (₹4,999):**

> Payment received. Starter Kit delivery:
> 1. Zip main WhatsApp pe bhej raha hoon (ya GitHub read-access invite — jo easy lage).
> 2. README.md me 4-step setup hai — 15 min me running.
> 3. Docs me REBRAND + VERTICAL_SWAP guides hain. Error aaye to screenshot bhejo, main khud help karunga.

## After refund

Founder tells beyond the buyer's key — beyond removes that wrap and pushes; buyer ka access
second-wise band, baaki buyers unaffected. (For per-buyer keys: each buyer gets their own
generated key wrapped into vault-data/kit-data on delivery. Today we run shared keys above.)

## Key rotation procedure (for beyond)

1. Decrypt current blob with a live key (wrap layer → cek → blob).
2. New random key(s), same format (KAMAI-/KIT- + 4 chars, no 0/O/1/I).
3. Re-encrypt with new cek, one wrap per key (Kit keeps 3 wraps: primary + 2 backups).
4. Deploy vault/vault-data.js and kit/kit-data.js to this repo (Pages auto-deploys).
5. Update the keys in this file, delete old keys from this file.
6. Verify live: old key rejected, new key unlocks (Vault 200 prompts / 15 categories; Kit 10 sections).
