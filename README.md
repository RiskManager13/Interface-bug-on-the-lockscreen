# Interface-bug-on-the-lockscreen
FaceID remains visible and appears enabled in MyTonWallet Air even when disabled in iOS settings for the app

If FaceID access is disabled for MyTonWallet Air via iOS system settings, the app still behaves as if FaceID is enabled:
The FaceID button remains visible on the lock screen.
The FaceID toggle in the app settings stays active (enabled), as if permission wasn't revoked.
No notification is shown to the user about the system-level restriction.
This behavior can mislead users and violates proper UI/UX expectations.

Expected Behavior
The FaceID button should disappear from the lock screen when system access is revoked.
The in-app FaceID toggle should be disabled or greyed out once FaceID is denied at the system level.
Optionally, the app should display a warning like:
"FaceID is disabled in iOS settings. Please enable access in system settings to use this feature."

Actual Behavior
The FaceID button remains visible on the lock screen even when the permission is denied in iOS settings.
The FaceID toggle in app settings stays active, giving a false impression that FaceID is functional.
This behavior can mislead users and violates proper UI/UX expectations.

Steps to Reproduce
Install MyTonWallet Air on an iPhone with FaceID.
Go to iOS Settings → MyTonWallet app → Disable FaceID access.
Launch the app.

Observe:
The FaceID button is still visible on the lock screen.
The FaceID toggle in the app settings remains active.

Environment
Device: iPhone 13 Pro Max
OS: iOS 18.5
App version: MyTonWallet Air 3.7.4 (209)
Protection method: PIN + FaceID
