# 🧩 Modular Test System – Card Template

A modular KiCad project for a Modular Test System (MTS) interface card.  
Includes the full layout, schematic, configuration files, and zipped Gerber files ready for manufacturing.

---

## 📦 Project Contents

- `.kicad_pro` – Project file
- `.kicad_sch` – Schematic
- `.kicad_pcb` – PCB layout
- `*-backups/*.zip` – Gerber backup ZIPs for production
- `.gitignore`, `LICENSE`, `README.md`

---

## 🛠 Requirements

- [KiCad 8.x](https://www.kicad.org/)
- Optional: [Gerber Viewer](https://gerbv.geda-project.org/) or JLCPCB/PCBWay web viewer

---

## 🚀 Open the Project

```bash
# Clone the repository
git clone https://github.com/StyriaElectronics/MTS_Card_Template.git

# Open the project in KiCad
open MTS_Card_Template.kicad_pro
```

---

## 🧪 Export Gerber Files

To export new Gerber files from KiCad:

1. Open the `.kicad_pcb` file in KiCad
2. Go to File > Plot > Gerber
3. Optionally, ZIP the result:
   ```bash
   zip -r Gerber_Export.zip <folder>
   ```

---

## 📃 License

This project is licensed under the  
**[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)** license.

> You may use, modify, and share the project – **as long as you give proper credit to the author**.

Author: **Styria Electronics András Nagy**  
Website: [styria-electronics](https://styria-electronics.at)

---

## 🤝 Contributing

Pull requests, issues, and forks are always welcome!

---

## ⭐️ If You Like It...

... give this project a star ⭐️ on GitHub!
