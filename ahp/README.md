# AHP Decision Calculator

Web app for the Analytic Hierarchy Process (Saaty): criteria and alternatives can be added, renamed and evaluated
step by step (Guided input), with consistency check (CR ≤ 0.10), three priority methods, results and sensitivity analysis.

* **Live page:** https://niedaoducnguyen.github.io/ahp/
* **Editable texts:** press **✎ Edit texts** to change the title, tab names, descriptions and guide texts.
* **Per-account storage:** press **Sign in with Google**. Texts and projects are stored in one private Cloud Firestore
  document per Google account (`users/{uid}`); the security rules in `firestore.rules` allow only the owner to read or write it.
  Without signing in, data are kept in the browser.

## Configuration (once)
1. Create a Firebase project, add a **Web app** and copy its configuration into `firebase-config.js`.
2. Authentication → Sign-in method → enable **Google**; Settings → Authorized domains → add `niedaoducnguyen.github.io`.
3. Firestore Database → create (production mode, region `asia-southeast1`) → Rules → paste `firestore.rules` → Publish.

The page uses only plain HTML/CSS/JavaScript; the Firebase SDK (v10.12.2) is loaded from `www.gstatic.com`.
