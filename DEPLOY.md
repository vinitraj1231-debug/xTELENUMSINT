# TELESPOT-NUMSINT Deployment Guide / डिप्लॉयमेंट गाइड

यह गाइड TELESPOT-NUMSINT क्रोम एक्सटेंशन (Chrome Extension) को डिप्लॉय और इनस्टॉल करने के सभी तरीके स्टेप-बाय-स्टेप (Step-by-Step) समझाती है।

---

## 🇮🇳 हिंदी / Hinglish निर्देश (Deployment Steps in Hindi)

### तरीका 1: अपने ब्राउज़र में लोकल डिप्लॉय (Local / Developer Mode Deployment)

अगर आप अपने कंप्यूटर पर इस एक्सटेंशन को तुरंत चलाना चाहते हैं, तो इन स्टेप्स को फॉलो करें:

#### 1. कोड डाउनलोड करें (Download Source Code)
- अगर आपके पास Git है:
  ```bash
  git clone https://github.com/thumpersecure/xTELENUMSINT.git
  cd xTELENUMSINT
  ```
- या फिर GitHub / Repository प्रोजेक्ट की **ZIP फाइल** डाउनलोड करके किसी फोल्डर (उदा. `xTELENUMSINT`) में अनजिप (Unzip / Extract) करें।

#### 2. गूगल क्रोम (Google Chrome) खोलें
- अपने ब्राउज़र के एड्रेस बार में टाइप करें: `chrome://extensions/`
- या ऊपर दायें (Top-Right) कोने में 3 डॉट्स `⋮` -> **Extensions** -> **Manage Extensions** पर क्लिक करें।

#### 3. डेवलपर मोड (Developer Mode) ऑन करें
- ऊपर दायें कोने में **Developer mode** का टॉगल (Toggle switch) दिखेगा, उसे **ON** करें।

#### 4. एक्सटेंशन लोड करें (Load Unpacked)
- **`Load unpacked`** बटन पर क्लिक करें।
- अपने कंप्यूटर में वह फोल्डर चुनें जिसमें `manifest.json`, `popup.html`, `popup.js` आदि फाइलें मौजूद हैं।
- **Select Folder** पर क्लिक करें।

#### 5. एक्सटेंशन का उपयोग करें
- एक्सटेंशन लोड हो जाएगा! ब्राउज़र के टूलबार में एक्सटेंशन आइकन 🧩 पर क्लिक करके TELESPOT-NUMSINT को पिन (Pin) करें और इस्तेमाल करें।

---

### तरीका 2: ZIP पैकेज बनाना (Distribution ZIP File Creation)

अगर आप किसी दूसरे यूजर को एक्सटेंशन भेजने के लिए Zip फाइल बनाना चाहते हैं:

1. प्रोजेक्ट के सभी मुख्य फाइलों को सेलेक्ट करें:
   - `manifest.json`
   - `popup.html`
   - `popup.css`
   - `popup.js`
   - `content.js`
   - `concurrency.js`
   - `icons/` फोल्डर
   - `README.md` & `LICENSE` (ऑप्शनल)
2. फाइलों पर राइट-क्लिक (Right Click) करके **Compress to ZIP file** / **Add to Archive** चुनें।
3. Zip फाइल का नाम `TELESPOT-NUMSINT-v1.4.0.zip` रखें।
4. कोई भी यूजर इस ZIP को डाउनलोड और Extract करके "Load Unpacked" विधि से डिप्लॉय कर सकता है।

---

### तरीका 3: गूगल क्रोम वेब स्टोर पर डिप्लॉय करना (Chrome Web Store Publishing)

अगर आप इसे Official Chrome Web Store पर पब्लिक या प्राइवेट डिप्लॉय करना चाहते हैं:

1. **Chrome Developer Console** ([https://chrome.google.com/webstore/devconsole](https://chrome.google.com/webstore/devconsole)) पर जाएं।
2. गूगल डेवलपर अकाउंट से लॉगिन करें (यदि पहली बार है, तो वन-टाइम $5 रजिस्ट्रेशन फीस लगती है)।
3. **Add new item** पर क्लिक करें और अपनी तैयार की गई `.zip` फाइल अपलोड करें।
4. स्टोर की जानकारी भरें (Store listing detail, descriptions, screenshots, privacy policy)।
5. **Submit for Review** पर क्लिक करें। Google की समीक्षा के बाद एक्सटेंशन डिप्लॉय हो जाएगा।

---

## 🇬🇧 English Instructions

### Method 1: Local / Unpacked Deployment (Developer Mode)

1. **Obtain the Extension Files**:
   Clone the repository or download & extract the source ZIP file to a folder.
   ```bash
   git clone https://github.com/thumpersecure/xTELENUMSINT.git
   ```

2. **Open Extensions Page**:
   In Chrome / Edge / Brave, navigate to `chrome://extensions/`.

3. **Enable Developer Mode**:
   Toggle the **Developer mode** switch in the top-right corner to **ON**.

4. **Load Unpacked**:
   - Click **Load unpacked**.
   - Select the directory containing `manifest.json`.

5. **Pin & Run**:
   Click the Extensions icon in your toolbar, pin **TELESPOT-NUMSINT**, and start using it.

---

### Method 2: Packaging for Distribution (.zip)

To create a deployable ZIP package for sharing:
- Zip the core extension files (`manifest.json`, `popup.html`, `popup.css`, `popup.js`, `content.js`, `concurrency.js`, `icons/`).
- Users can unzip the archive and deploy via **Load unpacked**.

---

### Method 3: Chrome Web Store Deployment

1. Register at [Chrome Developer Dashboard](https://chrome.google.com/webstore/devconsole).
2. Click **New Item** and upload your zipped extension.
3. Fill out the store listing information, graphics, and privacy declaration.
4. Click **Submit for Review**.

---

## ❓ Frequently Asked Questions / अक्सर पूछे जाने वाले सवाल

- **Q: क्या यह Brave या Microsoft Edge पर काम करेगा?**
  - **A:** हां! Chromium आधारित सभी ब्राउज़र्स (Brave, Edge, Opera, Vivaldi) में `chrome://extensions/` या `edge://extensions/` पर जाकर Developer mode ऑन करके Load unpacked से डिप्लॉय कर सकते हैं।

- **Q: "Manifest file is missing or unreadable" एरर आये तो क्या करें?**
  - **A:** ध्यान रखें कि "Load unpacked" करते समय आपको वह फोल्डर सेलेक्ट करना है जिसके अंदर `manifest.json` फाइल सीधी मौजूद हो, न कि कोई बाहरी पैरेंट फोल्डर।
