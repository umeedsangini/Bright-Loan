# Bright Loans — GitHub se Android APK

Yeh project aapke `Bright Loans` HTML app ko Capacitor ke through Android app mein package karta hai. GitHub Actions APK build karega.

## GitHub par upload

1. ZIP extract karein.
2. GitHub par naya repository banayein, jaise `bright-loans-app`.
3. Is folder ke **andar ke saare files aur folders** repository ke root mein upload karein. `.github/workflows/build-apk.yml` bhi upload hona chahiye.
4. Repository mein **Actions** tab kholein.
5. `Build Bright Loans APK` workflow select karke **Run workflow** dabayein. `main` branch par push karne se bhi build automatically chalega.
6. Build complete hone par workflow run ke neeche **Artifacts** mein `bright-loans-debug-apk` download karein.
7. ZIP artifact extract karne par `app-debug.apk` milega. Isse Android phone par install kar sakte hain (unknown-app installation permission lag sakti hai).

## Important

- Yeh **debug APK** hai testing/install ke liye. Play Store release ke liye signed release APK/AAB aur signing key alag se configure karni hogi.
- App ka HTML `www/index.html` mein hai. Future changes isi file mein karein.
- App mein maujood payment/PIN flow source ke mutabik simulation hai; yeh real bank, UPI, loan provider ya payment network se connected nahi hai.
- Package ID: `com.brightloans.app`. Publish karne se pehle ise apne final unique package ID se badlein.
