# Sing-Song

A TUI panel for [Sing-Box](https://github.com/SagerNet/sing-box)’s API calls using websocket connection for speed.

<img width="1694" height="1128" alt="Screenshot 2026-09-24 at 14 13 59 2" src="https://github.com/user-attachments/assets/f804eb39-db11-432b-9b95-8deaaee1c69e" />

#### Features

  1. Visually pleasant minimal design.
  2. Mutliple sing-box servers can be queried at the same time.
  3. Highlights problematic connections.
  4. GeoLite2 database integration to instantly fetch and catch additional information about all outbound and inbound IP’s
  5. A simple catching system for destination IP’s based on GeoLite2 queries by country code and domain missmatch of final IP’s ASN.

Seperate versions for sing-box running on a server (sing) or local client machine (singlo)

#### Dependencies

pip3 install maxminddb websocket-client cachetools

#### Sing

for servers sing-box API

<img width="1650" height="752" alt="Screenshot 2026-09-26 at 02 37 33 2" src="https://github.com/user-attachments/assets/a062d5d1-9325-4394-b30e-4a707cfba220" />

- <b>Enter</b>  Shows a popup with queried information about selected connection
- <b>Space</b>  Pauses list update
- <b>Escape</b>  Toggles Catch list
- <b>Tab</b>  Cycles list by destination servers API and all servers together
- <b>X</b>  Adds current selection to Catch list
- <b>K</b>  Kills selected connection
- <b>C</b>  Copies destination IP
- <b>Shift+C</b>  Copies source IP
- <b>D</b>  Copies domain name
- <b>S</b>  Changes sort order

#### Song

For clients sing-box API

<img width="876" height="386" alt="Screenshot 2026-09-26 at 05 40 15" src="https://github.com/user-attachments/assets/b20dbcd2-ec7d-409d-b920-6300f0bb45d9" />

- <b>Enter</b>  Shows a popup with queried information about destinaion IP
- <b>Space</b>  Pauses list update
- <b>Escape</b>  Opens outbound proxy selector
- <b>K</b>  Kills selected connection
- <b>C</b>  Copies destination IP
- <b>D</b>  Copies domain name
- <b>S</b>  Changes sort direction and sort order by most uploaded or downloaded.

#### Information
On the first run the configuration file is created and the databases are downloaded.
Configurations are stored in ~/.config/sing-song/config.json
