# Réseau Cedar — New Version

## Included
- Firebase email/password accounts
- Signed-in users can read school messages
- Teacher/admin accounts can send announcements
- Admins can post external links and delete messages globally
- Permissions are enforced by Realtime Database rules

## Before using
1. Replace placeholders in `firebase-config.js` with the exact Firebase web config values.
2. In Firebase Console > Realtime Database > Rules, publish `database.rules.json`.
3. In GitHub repository Settings > Pages, deploy branch `main`, folder `/ (root)`.
4. Create your own app account, then find its UID in Firebase Authentication > Users.
5. In Realtime Database > Data, create `/admins/YOUR_UID` with boolean value `true`. To assign teachers, create `/teachers/TEACHER_UID` with boolean `true`. Never let app users edit these nodes.

## Limitations
File uploads and voice messages are not active. Cloud Storage needs separate setup and may require upgrading Firebase billing. Do not upgrade or add payment details unless you accept potential charges. Test with non-sensitive data before school use.
