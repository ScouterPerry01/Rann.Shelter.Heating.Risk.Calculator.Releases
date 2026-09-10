# RANN Shelter Heating Risk Calculator — downloads

Residual-risk assessment for heating soft-walled and hard-walled shelters —
wall tents, tipis, cabins, bunkhouses, pavilions.

**18 heat sources · 312 risks · 990 controls. Works entirely offline.**

This repository exists to host the downloads. **It contains no application
source.** Releases are on the [Releases page][releases].

[releases]: https://github.com/ScouterPerry01/Rann.Shelter.Heating.Risk.Calculator.Releases/releases

---

## Getting it

**Windows** — from the Microsoft Store. Store packages are signed by
Microsoft, so there is no security warning to click past.

**Linux** — from [Releases][releases], x86-64:

| File | For |
| --- | --- |
| `…-x64.AppImage` | Any modern distribution. No install step. |
| `…_amd64.deb` | Debian, Ubuntu and derivatives. Adds a desktop entry. |

### Running the AppImage

```
chmod +x shelter-heating-risk-calculator-0.2.0-x64.AppImage
./shelter-heating-risk-calculator-0.2.0-x64.AppImage
```

### Installing the .deb

```
sudo apt install ./shelter-heating-risk-calculator_0.2.0_amd64.deb
```

Use `apt` rather than `dpkg -i`: `apt` pulls the dependencies and `dpkg`
does not. It is a plain package rather than a repository, so it will not
update itself — watch the Releases page.

### Checking what you downloaded

Every release carries a `SHA256SUMS.txt`. To verify:

```
sha256sum -c SHA256SUMS.txt
```

---

## What it does

You describe the shelter and the appliance heating it. The application scores
the risks that apply, shows which controls your description already puts in
place, lets you select the rest, reports the risk that remains, and produces a
Word document you can file.

It makes **no network requests of any kind** — not for licensing, not for
updates, not for telemetry. That is not a statement of intent: outbound
requests are blocked inside the application, and an automated test fails the
build if any code attempts one. Everything you record lives in a single file
on your own machine.

A searchable user manual is built in, under **Help → User manual**, and opens
in a window of its own so it can sit beside the work.

## What it is not

Structured judgement for comparing control sets. **Not a certification, and
not an inspection.** It measures nothing — every figure comes from you. The
heat-loss figures are order-of-magnitude planning numbers from nominal
material R-values and assumed air-change rates, **not a load calculation**.
CSA B365 is referenced for solid-fuel clearances and CSA B149.1 and B149.2 for
gas; the application does not certify compliance with any of them.

---

## Reporting a problem

This repository hosts downloads and does not take issues. Write to the
address in the package metadata — `dpkg -I` on the .deb prints it — or use
the contact route on the product page. Please say which version, which
platform, and what you expected to happen.

---

## Licence

Copyright © 2026 Perry Schippers. All rights reserved.

The application, its risk register, its rating logic and its supporting text
are copyright and may not be reproduced or redistributed without permission.
The binaries here are provided for use of the application; publishing them
does not place the source, the register or the ratings in the public domain.
