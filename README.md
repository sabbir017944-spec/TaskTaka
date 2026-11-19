# TaskTaka

Firebase-backed authentication and task-submission starter for the existing Firebase project `tasktaka-7b286`.

## Included
- Firebase Authentication: Email/Password and Google sign-in.
- Firestore user profile at `users/{uid}`.
- Firestore task submissions at `taskSubmissions/{uid}_{taskId}`.
- A user can submit each sample task once; submissions start as `pending`.
- Users can read only their own profile and task submissions.
- Users cannot approve submissions, change task rewards, or credit balances from the browser.
- No real-money balance, withdrawal, or payout is enabled.

## One-time Firebase Console setup
1. Authentication → Sign-in method: enable **Email/Password** and **Google**.
2. Authentication → Settings → Authorized domains: ensure `sabbir017944-spec.github.io` is listed.
3. Firestore Database → Create database. Choose a location carefully; it cannot be changed later.
4. Firestore → Rules: copy the latest `firestore.rules` file from this repository and press **Publish**.
5. Wait for GitHub Pages deployment after each code update.

## Important safety and production requirements
This is a test/demo workflow, not a cash-rewards platform. A task submission is only a request for review; it does not earn money or points automatically. An administrator approval screen must not be trusted if it runs only in the browser. Secure approvals and balance credits require a trusted backend (for example, Firebase Cloud Functions or another server using the Admin SDK), role assignment through trusted claims, audit logs, anti-fraud checks, and lawful sponsor/payment arrangements. Real withdrawals are not implemented. Do not put service-account keys or private credentials in this repository or browser code.
