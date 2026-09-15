# SAAS_Clean Xataface Theme Extension

`SAAS_Clean` delivers a modern SaaS/Gmail-inspired visual overhaul for Xataface applications. It features a flat, minimal interface designed to stay out of the user's way. Custom application headers can be added seamlessly using standard Xataface hooks (**global_header.html** file).

## Prerequisites & Disclaimers

* **Disclaimer:** Provided as-is. Tested in production across multiple applications running **Xataface 4.0.0 (build 5006)**. Ensure you test in your own environment before deploying.
* **Safe Deployment:** This is a UI theme extension only. It will **not** alter or modify any database data.
* **Customization:** Feel free to modify the source files to fit your application's aesthetic needs.

---

## Installation

### Download

You are able to download a ZIP using the green "< > Code" button above then selecting "Download ZIP".  Or you may view the files and create them yourself.

### 1. Upload Theme Directory

Upload the `saas_clean` folder (containing two files and one directory) to your application's `themes` directory. If the `themes` directory does not exist, create it in your root Xataface folder:

```text
[Xataface Application Root]/themes/saas_clean

```

### 2. Update `conf.ini`

Open your application's `conf.ini` file and ensure the `g2` module is enabled under `[_modules]`, then register the theme under `[_themes]`:

```ini
[_modules]
modules_g2=modules/g2/g2.php

[_themes]
saas_clean="themes/saas_clean"

```

Save and upload the modified `conf.ini` to your server.

### 3. Clear Compiled Templates

Purge all cached files inside the `templates_c` directory. Via SSH, run the following from your Xataface application root:

```bash
sudo rm -Rf templates_c/*

```

### 4. Verify & Clear Browser Cache

Navigate to your Xataface application in the browser.

> **Important:** Clear your browser cache before loading the page. Some Xataface form assets and JavaScript components cache aggressively.

### 5. Multi-App Deployment

Repeat steps 1–4 for any additional Xataface applications.

---

## Uninstallation

1. Remove the theme registration from your `conf.ini`:
```ini
[_themes]
saas_clean="themes/saas_clean"

```


2. Clear all files inside the `templates_c/` directory.
3. Remove the `themes/saas_clean` directory from your server.
