# Mordred-Extension — built distribution

Prebuilt, ready-to-load bundle of the **Mordred** browser extension
(Manifest V3, Chromium: Chrome / Brave / Arc / Edge). Compiled output only —
**no source code**. Source lives in the private `Mordred-Extension` repo.

Current version: **0.2.0**

## Install (load unpacked)

1. Download / clone this repository.
2. Open `chrome://extensions` (or `brave://`, `edge://extensions`).
3. Enable **Developer mode**.
4. Click **Load unpacked** and select the `dist/` folder.

Pair it with a running **Mordred-Hermes** gateway from the extension popup.

## Notes

- Each entry (background, content scripts, injected scripts, popup, sign
  window) is bundled into a single obfuscated file with opaque names, all
  identifiers mangled, string literals base64-encoded, and no source maps or
  comments.
- This is size/hygiene, **not** a security boundary: a browser extension runs
  on the user's machine and is always recoverable. Mordred's security comes
  from its architecture (signing keys stay in the Hermes keyvault / Secure
  Enclave, signing happens on the Hermes side, channel content is end-to-end
  encrypted), never from hiding client code.
