# Tapo Smart plug script

De Tapo P115 smart plug werkt met home assistant en een extern script.

## python-kasa
`python-kasa`: [Manual](https://python-kasa.readthedocs.io/en/latest/index.html)
- Verbind met de tmp-wifi van de plug.
- Installeer in een virtualenv en draai `uv run kasa discover`
- `uv run kasa --host $IP wifi scan`, waarschijnlijk is het IP `192.168.0.1`
- `uv run kasa --host $IP wifi join $netwerk` en vul wifi-type en wachtwoord in (wifi-type staat in de data uit vorige stap)

> [!NOTE]
> Het joinen van een netwerk kan een foutmelding geven, dit lijkt echter geen probleem.

## Home Assistant
[Integration manual](https://www.home-assistant.io/integrations/tplink)
- In homeassistant: voeg integration toe voor tp-link (zoek op Tapo)
- Vul geen host in, dan probeert de integration autodiscovery
- Profit
