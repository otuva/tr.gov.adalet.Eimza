# Adalet E-İmza

___Sign on UYAP portals with your smart card___

Adalet E-İmza is the Turkish Ministry of Justice's background service that lets browser-based UYAP systems sign with the certificate on a smart card or USB token.

---

## Manual Install and Run

Make sure you follow the [setup guide for your Linux distribution](https://flathub.org/en/setup) before installing.

```bash
flatpak install flathub tr.gov.adalet.Eimza
flatpak run tr.gov.adalet.Eimza
```

The app listens on `127.0.0.1:5975`. Remove the upstream deb or AppImage first, otherwise both try to bind the same port. It does not start at login; launch it before signing.

## Building

```bash
git clone --recurse-submodules git@github.com:flathub/tr.gov.adalet.Eimza.git
flatpak run org.flatpak.Builder build-dir --user --ccache --force-clean --install tr.gov.adalet.Eimza.yaml
```
