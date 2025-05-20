# 🚀 ROM Builder by frn

A powerful GitHub Actions workflow that automates the process of building custom Android ROMs like LineageOS, crDroid, and more — directly from your device tree.

---

## 📦 Features

- 🛠️ Build ROMs with GitHub Actions
- ⚙️ Fully customizable input fields
- 💻 OpenJDK 11, repo setup, and environment handled
- 💾 Uploads built ROMs to GitHub Releases
- 🧠 Uses swap memory for resource efficiency
- ⏱️ Parallel sync and build jobs for speed

---

## 🧰 Usage

1. **Fork this repository**.
2. Go to the **Actions tab**, click **"ROM Builder by frn"**, then click **Run workflow**.
3. Fill in the following fields:

| Input            | Description                          | Example |
|------------------|--------------------------------------|---------|
| `ROM_NAME`        | Short name of ROM                    | `lineage`, `crdroid` |
| `MANIFEST_URL`    | Git manifest repo URL                | `https://github.com/LineageOS/android.git` |
| `MANIFEST_BRANCH` | ROM branch                           | `lineage-20.0` |
| `DEVICE_NAME`     | Codename of your device              | `daisy` |
| `DEVICE_TREE`     | Git repo URL of your device tree     | `https://github.com/yourname/device_xiaomi_daisy.git` |
| `DEVICE_BRANCH`   | Branch of the device tree            | `lineage-20.0` |
| `DEVICE_PATH`     | Path where device tree should be cloned | `device/xiaomi/daisy` |
| `BUILD_TARGET`    | Build command target                 | `bacon` (for LineageOS) |

---

## 📝 Example Config

```yaml
ROM_NAME: lineage
MANIFEST_URL: https://github.com/LineageOS/android.git
MANIFEST_BRANCH: lineage-20.0
DEVICE_NAME: daisy
DEVICE_TREE: https://github.com/frn-dev/device_xiaomi_daisy.git
DEVICE_BRANCH: lineage-20.0
DEVICE_PATH: device/xiaomi/daisy
BUILD_TARGET: bacon
📤 Output
ROM zip file will be uploaded to the GitHub Releases section of your repo automatically once the build completes.

🧠 Notes
GitHub-hosted runners have a 6-hour time limit and 14 GB RAM. Use a minimal manifest or shallow sync for large projects.

For long builds, consider using self-hosted runners.

Ensure your device tree is clean and compatible with the selected ROM and manifest branch.

🧑‍💻 Credits
🧠 Workflow by frn

📘 Based on LineageOS build guide

🛠 Inspired by GitHub ROM builders and TWRP automation

❤️ Contributing
Feel free to open a PR or issue if you want to add more features (like vendor/kernel auto clone, OTA support, or manifest generator).

📜 License
This project is licensed under the MIT License. Feel free to fork and modify!

yaml
Copy code

---

Would you like a badge (like build status or GitHub Action trigger button) added to the top of this README?
















FARHAN can make mistakes. Check important
