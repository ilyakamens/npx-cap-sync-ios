## Minimal repo

### Created for

https://github.com/ionic-team/capacitor/issues/7662

### Created with

```bash
npm init @capacitor/app
npm install @capacitor/ios
npx cap add ios
```

### To repro

```bash
# Select a real device from the dropdown.
npm run build && npx cap run ios
# Make an app (HTML) change... and then select the same device.
npm run build && npx cap run ios
```

Notice that the app hasn't restarted and that one must force-close the app twice for the change to
be visible. (The first force-close after `npx cap run ios` doesn't actually force-close the app for
reasons I don't understand.)
