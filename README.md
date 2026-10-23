# QR Code Generator

Make QR codes in the browser and download them as PNG or SVG.

**Live:** https://rocketflash-net.github.io/qr-generator/

## Content types

| Type | Encodes as |
|---|---|
| Link | URL (adds `https://` if missing) |
| QRIS payment | Your QRIS string, CRC-checked. Optionally set an amount: fills tag 54, switches tag 01 to dynamic (12) and recalculates the CRC |
| Text | Plain text (full UTF-8, including emoji) |
| Contact | vCard 3.0 |
| Wi-Fi | `WIFI:T:…;S:…;P:…;;` with escaping |
| Location | Google Maps link from an address or coordinates |
| WhatsApp | `wa.me` link, `08…` numbers normalised to `628…` |
| Email | `mailto:` with subject and body |
| Phone | `tel:` |
| SMS | `SMSTO:` |
| Event | iCalendar `VEVENT` |

Options: foreground and background colour (with a contrast warning), error correction L/M/Q/H, quiet zone, PNG size.

Everything runs locally. Nothing you type is sent anywhere or stored.

To inspect a QRIS payload tag by tag, use the [QRIS TLV Decoder](https://rocketflash-net.github.io/qris-tlv-decoder/).

## Credits

QR encoding by [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) by Kazuhiko Arase (MIT), vendored in `vendor/qrcode.js`. QR Code is a registered trademark of DENSO WAVE INCORPORATED.

---

Built by [Daniel Aldo Pratama](https://rocketflash-net.github.io/it/).
