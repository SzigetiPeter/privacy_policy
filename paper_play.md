# Privacy Policy for PaperPlay

**Last updated:** April 12, 2026
**Effective date:** April 12, 2026

This Privacy Policy describes how **PaperPlay** (the "App", "we", "us", or "our") handles information when you use our Android application. Please read it carefully.

---

## 1. Summary

PaperPlay is a fully offline, local application. **We do not collect, transmit, or store any personal data on external servers.** All data created or processed by the App lives exclusively on your device and is under your full control.

---

## 2. Who Uses This App

PaperPlay is operated by a **parent or guardian** (the "User") who sets up NFC-based audio experiences for young children. The child interacts with the physical NFC tags; the parent/guardian controls the App configuration.

The App is not directed at children. Children do not create accounts, enter personal information, or interact with the App interface directly. Any interaction by a child is limited to tapping NFC tags to trigger audio playback — no data is collected from or about the child in this process.

We do not knowingly collect any personally identifiable information from children under 13 (or the applicable age threshold in your jurisdiction). If you believe a child has inadvertently submitted personal information through the App, please contact us immediately so we can remove it.

---

## 3. Data Stored Locally on Your Device

All App data is stored in your device's local app storage and your device's local SQLite database. This includes:

### 3.1 NFC Tag Configuration
- Tag name (chosen by you)
- File path or URI pointing to an audio file on your device
- File path or URI pointing to an image file on your device (optional)
- Volume setting
- Whether the tag is in record mode

### 3.2 Audio Recordings
- If you use the recording feature, audio files are saved to your device's external app-specific directory (`Android/data/com.szigeti.audiotrackbynfctag/files/`)
- Recording files are named with a timestamp (e.g. `REC_20260412_143022.3gp`)
- Recordings are never transmitted anywhere

### 3.3 Play History (Statistics)
- Each time a tag triggers audio playback, a record is written to the local database containing: the tag ID, a Unix timestamp, and the playback duration
- This data never leaves your device
- You can delete statistics for individual tags from the Statistics screen at any time

### 3.4 Disclaimer Acceptance Record
- When you accept the Safety Disclaimer, the App stores locally: the version number of the disclaimer accepted and the date/time of acceptance
- This is stored in the device's SharedPreferences (`paperplay_prefs`)
- It is used only to avoid showing the disclaimer again on subsequent launches and to re-show it if the disclaimer text is materially updated
- This data never leaves your device

---

## 4. Permissions Used

| Permission | Why It Is Required |
|---|---|
| `NFC` | To read NFC tag IDs when a tag is scanned |
| `RECORD_AUDIO` | To record audio when a record-mode tag is scanned |
| `READ_MEDIA_AUDIO` (Android 13+) | To allow you to select audio files from your device |
| `READ_MEDIA_IMAGES` (Android 13+) | To allow you to select images from your device |
| `READ_EXTERNAL_STORAGE` (Android 12 and below) | To allow you to select audio and image files from your device |
| `CAMERA` | To allow you to take a photo directly within the App to use as tag artwork |
| `WAKE_LOCK` | To keep the device CPU active in Toddler Mode so NFC remains responsive when the screen is off |
| `INTERNET` | Required by the ExoPlayer (Media3) and Coil image-loading libraries included in the App. The App uses this permission to stream audio from HTTP/HTTPS URLs **if you manually enter one** as a tag's audio source. No data is sent to any server by the App itself. |

No permission data is transmitted to us or any third party.

---

## 5. Third-Party App Handoff

If you configure a tag with a **Spotify URI** (`spotify:…` or `https://open.spotify.com/…`) or a **YouTube URL**, tapping that tag will open the Spotify or YouTube application on your device (or your default browser if those apps are not installed).

- The App passes only the URI you provided to the operating system via a standard Android `Intent`
- From that point, your interaction is governed by **Spotify's Privacy Policy** or **YouTube's/Google's Privacy Policy** respectively
- PaperPlay does not receive any data back from those applications

---

## 6. Third-Party Libraries

The App includes the following open-source libraries. These libraries do not collect analytics or transmit data to third parties in this App's configuration:

| Library | Purpose |
|---|---|
| ExoPlayer / Media3 | Local and streaming audio playback |
| Coil | Image loading from local URIs |
| Room (SQLite) | Local database for tag and statistics storage |
| Hilt (Dagger) | Dependency injection framework |
| Gson | JSON serialisation for tag import/export |

None of these libraries are configured to send data to remote servers. No analytics SDK, crash reporting SDK, or advertising SDK is included in this App.

---

## 7. Data You Share Voluntarily

The App includes an optional **Export / Share** feature that allows you to:

- Export a JSON file containing your tag configuration (names, audio URIs, image URIs, volume settings)
- Export a PDF of your tag artwork

These files are generated locally and shared only when you explicitly trigger the share action. The App uses Android's standard share sheet — you choose where the file goes. We do not receive a copy.

**Note:** Exported tag configuration files may contain file paths to audio or image files on your device. Be mindful of what you share if those paths reveal personal information.

---

## 8. Data Security

Because all data is stored locally on your device, its security depends on your device's security (screen lock, encryption, etc.). We recommend:

- Keeping your device OS and App up to date
- Using your device's screen lock feature

We have no access to the data stored on your device and cannot recover it if it is lost or deleted.

---

## 9. Your Rights and Data Control

You have full control over all data this App stores. You can:

- **Delete individual tags** — removes the tag and its associated data from the local database
- **Delete play statistics** — available per-tag from the Statistics screen
- **Delete all App data** — via Android Settings → Apps → PaperPlay → Storage → Clear Data. This permanently removes all tags, recordings, statistics, and the disclaimer acceptance record
- **Delete recordings** — individual recording files can be deleted from the app's files directory using any file manager

Since we hold no data on our servers, there is nothing to request from us under data subject access rights (GDPR Art. 15 etc.). All data resides on your device and is accessible and deletable by you directly.

---

## 10. Changes to This Privacy Policy

We may update this Privacy Policy when the App's functionality changes materially. The "Last updated" date at the top of this page will reflect any revision. If changes are significant, we will note them in the App's release notes on Google Play.

Continued use of the App after a policy update constitutes acceptance of the updated policy.

---

## 11. Contact

If you have questions or concerns about this Privacy Policy, please open an issue on the project's GitHub repository or contact the developer directly via the Google Play Store listing.

---

*PaperPlay is an independent, free application developed by Szigeti Péter. It is not affiliated with Spotify, YouTube, Google, or any other third-party service mentioned in this document.*
