# Turniket Report – Ubuntu 26 LTS .deb Package

Kompletný Debian balík na konverziu CSV exportu z Integriti do formátovaného XLSX reportu.

## Rýchla inštalácia

Na Ubuntu 26 LTS jednoducho spusti:

```bash
chmod +x install.sh
./install.sh
```

To:
1. Nainštaluje všetky potrebné závislosti (pandas, openpyxl, python3-tk)
2. Zostaví `.deb` balík
3. Nainštaluje aplikáciu

## Ručné spustenie buildu

Ak chceš len zostaviť `.deb` bez inštalácie:

```bash
chmod +x build.sh
./build.sh
```

Vytvorí: `turniket-report_1.0.0_all.deb`

## Inštalácia existujúceho .deb

```bash
sudo dpkg -i turniket-report_1.0.0_all.deb
```

## Spúšťanie aplikácie

### GUI mód (interaktívny):
```bash
turniket-report
```

### CLI mód s parametrami:
```bash
turniket-report raw.csv --label BBC5
turniket-report raw.csv -p permissions.csv -n "Accenture" -l "BBC5" -o report.xlsx
turniket-report raw.csv --from 01.10.2026 --to 31.10.2026
```

## Oddinštalácia

```bash
sudo apt-get remove turniket-report
```

## Obsah balíka

- `/usr/bin/turniket-report` – spustiteľná aplikácia
- `/usr/share/applications/turniket-report.desktop` – menu záznam
- `/usr/share/doc/turniket-report/` – dokumentácia

## Závislosti

Automaticky sa nainštalujú:
- `python3 >= 3.8`
- `python3-pandas`
- `python3-openpyxl`
- `python3-tk`

## Podporované Ubuntu verzie

- Ubuntu 26 LTS (Noble)
- Ubuntu 24.04 LTS (Jammy)
- Ubuntu 22.04 LTS (Focal)

## Licencia

MIT
