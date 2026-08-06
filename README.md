# strut-dl

Instagram/TikTok in-app-browser escape page for Strut.

Social in-app browsers swallow `apps.apple.com` links: Apple redirects to the
`itms-appss://` scheme and the WebView cannot hand that off, so the user gets a
blank page. The only reliable escape is a genuine user tap on a native-scheme
anchor, which is what this page is.

- Safari / Chrome / desktop -> redirected straight to the App Store, no page shown.
- Instagram / TikTok / Snapchat / Facebook on iOS -> one tap on `itms-apps://`.
- Android -> "iPhone only" notice.

Do NOT add an `x-safari-https://` escape: dead in Instagram since 2026-03-03
(shalanah/inapp-debugger#16).
