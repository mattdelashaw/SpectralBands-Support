# SpectralBands Support & Issue Tracking

Welcome to the public support hub for **SpectralBands**, a high-performance SDR client for iOS.

This repository is dedicated to **issue tracking, feature requests, and community discussions**. Please note that the source code for SpectralBands is currently private.

## 📡 Quick Links
- **Official Website:** [bytes-and-bolts.info/spectral-bands](https://bytes-and-bolts.info/spectral-bands)
- **Privacy Policy:** [Privacy Statement](https://bytes-and-bolts.info/spectral-bands/privacy)
- **Terms of Service:** [Terms](https://bytes-and-bolts.info/spectral-bands/terms)

## 🐛 Bug Reports & Feature Requests
We use GitHub Issues to track bugs and plan new features. Before opening a new issue, please:
1. **Search existing issues** to see if your concern has already been addressed.
2. **Use the provided templates** for Bug Reports or Feature Requests.
3. **Include details** about your hardware (e.g., RTL-SDR v3/v4, WebSDR server version) and your iOS device/version.

[**Open an Issue**](https://github.com/mattdelashaw/SpectralBands-Support/issues/new/choose)

## 📖 Server Setup & Configuration

SpectralBands supports two primary protocols for connecting to SDR hardware over the network.

### 1. WebSDR (Recommended)
Our high-performance WebSocket protocol. It abstracts hardware control and provides pre-decimated audio, making it more bandwidth-efficient and secure for public access.

- **Port:** Default 8080 (TCP).
- **Setup:** Use a compatible WebSDR server (like `rtlsdr-next`).
- **Command example:** `./websdr --port 8080`

### 2. rtl_tcp
The industry-standard protocol for raw IQ streaming. Note that this protocol provides direct hardware access and is best suited for local networks.

- **Port:** Default 1234 (TCP).
- **Setup:** Install `rtl-sdr` tools.
- **Command example:** `rtl_tcp -a 0.0.0.0 -p 1234`

## 🛠 Troubleshooting
- **Connection Refused:** Ensure your server is running and your router/firewall is allowing traffic on the specified port.
- **Laggy Waterfall:** Ensure you have a stable network connection. For `rtl_tcp`, a 5GHz Wi-Fi or wired connection is recommended due to high IQ data rates.
- **No Audio:** Ensure your iOS device is not on "Silent" mode and the in-app Audio icon is toggled to ON.

## ⚖️ License
Content in this repository (documentation, issue templates, and assets) is licensed under the [MIT License](LICENSE). 
*SpectralBands (the application) is a separate, proprietary product.*
