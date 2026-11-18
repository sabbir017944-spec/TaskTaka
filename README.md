# TaskTaka

Firebase-backed authentication starter for the existing Firebase project `tasktaka-7b286`.

## Included
- Firebase Authentication: Email/Password and Google sign-in.
- Firestore user profile at `users/{uid}`.
- Password reset email.
- Basic Firestore rules that prevent users from changing balances or other users' profiles.
- Dashboard task balances remain local demo data and are NOT real money.

## One-time Firebase Console setup required
1. Authentication → Get started → Sign-in method: enable **Email/Password** and **Google**.
2. Authentication → Settings → Authorized domains: ensure `sabbir017944-spec.github.io` is listed.
3. Firestore Database → Create database. Choose a location carefully; it cannot be changed later.
4. Firestore → Rules: publish the contents of `firestore.rules` from this repository.
5. Wait for GitHub Pages deployment after the commit.

## Important
This is not a production cash-rewards system. No SMS phone auth or bKash payouts are implemented. Do not store payout balances in client-controlled fields. A production reward ledger requires trusted server-side functions, anti-fraud checks, privacy review, and lawful sponsor/payment arrangements.
