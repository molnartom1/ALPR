# 🚗 Plate Gate – Intelligens rendszámfelismerő kapunyitó rendszer

**Plate Gate** egy könnyen telepíthető, offline működő rendszámfelismerő kapunyitó rendszer  
**OpenALPR** és **Flask** alapokon, Windows környezetre optimalizálva.

---

## 🔧 Fő funkciók
- ✅ Rendszámfelismerés Dahua IP kameráról (RTSP)
- ✅ Whitelist alapú engedélyezés (CSV fájl)
- ✅ Automatikus vagy kézi kapunyitás
- ✅ Relé támogatás (USB HID)
- ✅ Webes kezelőfelület valós idejű eseményekkel
- ✅ Szimulációs mód (kamerát és relét nem igényel)

---

## 🖥 Telepítés (Windows)
1. Telepítsd a [Python 3.10+](https://www.python.org/downloads/) verziót  
2. Másold a projektet ebbe a mappába:
   ```
   C:\plate_gate
   ```
3. Nyiss CMD-t:
   ```bash
   cd C:\plate_gate
   pip install -r requirements.txt
   ```
4. Állítsd be az `app.py`-ben a kamera URL-t:
   ```python
   CAMERA_URL = "rtsp://admin:Admin123@192.168.1.108:554/cam/realmonitor?channel=1&subtype=0"
   ```
5. Indítsd:
   ```bash
   python app.py
   ```
6. Nyisd meg a böngészőben:
   ```
   http://127.0.0.1:5000
   ```

---

## ⚡ Tesztelés (szimulációval)
Ha nincs csatlakoztatva kamera vagy relé:
- A főoldalon használható a **„Teszt felismerés”** funkció  
- A rendszám és confidence megadásával teljes folyamat szimulálható

---

## 🧰 Fejlesztési terv
- Több kamera kezelése  
- Email / SMS értesítés  
- Felhőnapló és jogosultsági szintek  
- Hang- vagy fényjelzés nyitáskor  

---

## 🖼 Képernyőkép (opcionális)
![Dashboard Screenshot](docs/screenshot.png)

*(A `docs/screenshot.png` fájl opcionális, ide teheted a kezelőfelület képét, ha lesz róla mentés.)*

---

## 🧑‍💻 Készítette
**Plate Gate Project**  
© 2025 – Nyílt forrású, oktatási és ipari célokra is szabadon bővíthető.
