UPLOAD THROUGH GITHUB WEB

Upload the CONTENTS of this folder to the root of:
https://github.com/kulfoldi-kaszino/firebase-web

Required repository structure after upload:
.github/workflows/firebase-hosting.yml
.gitignore
.firebaserc
firebase.json
public/...

IMPORTANT:
- The real workflow is .github/workflows/firebase-hosting.yml
- macOS Finder hides .github by default. Press Cmd+Shift+. to show hidden files.
- firebase-service-account.json in this package is intentionally EMPTY.
- Do NOT put the real Admin SDK JSON into the repository.
- Add it in GitHub:
  Settings -> Secrets and variables -> Actions
  Secret name: FIREBASE_SERVICE_ACCOUNT_KULFOLDI_KASZINO
  Value: the full Firebase Admin SDK JSON.

After the workflow file and secret exist, every push to main will deploy public/ to:
https://kulfoldi-kaszino.firebaseapp.com/
https://kulfoldi-kaszino.web.app/

The visible file firebase-hosting-workflow-COPY.yml is only a backup copy in case Finder hides .github.
GitHub does not execute that root copy.
