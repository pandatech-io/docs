```
author: Arian Nurrahman
```

# LAUNCHING YOUR REACT NATIVE APPS TO GOOGLE PLAY STORE


1. Share your built app to tester
   1. Build command. Make sure you are in root project directory 
      ```sh
      react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res
      ```
   1. Go to android directory `cd android`
   1. Build your app ./gradlew assembleRelease 
   1. Share your app on this directory: projectName/android/app/build/outputs/apk/debug/app-debug.apk 
2. Create a google developer account and turn on 2-Step Verification.
3. On Google Console Dashboard go to All Apps > Create App > Fill the form.
4. On App Dashboard page, on the sidebar go to App Content
1. Go to App Access : 
   1. If your apps has some restrictions choose “All or some functionality is restricted” > and fill up the form (Will be used by Google to review)
   2. Else choose “All Functionality is available without special access”. 
2. Go To Ads :
   1. Do your apps contain ads?
3. Go To Content Rating :
   1. Fill up the questionnaire.
4. Go To Target Audience :
   1. Fill up the form and privacy policy(optional but best practice) unless your app is not targeting under 13 years old.
5. Go To News Apps :
   1. Do your apps news apps?
5. On App Dashboard page, on the sidebar go to Store Presence
1. Go To Store Setting :
   1. Fill up the form and choose value carefully because it would help users to discover your apps.
   2. Check external marketing, since it's free and beneficial.
2. Go To Main Store Listing :
   1. Using the right keyword would play a big role in your apps. 
   2. Pay attention to the graphic requirements.
   3. Check the manage translation if necessary
6. On App Dashboard page, on the sidebar go to Production
1. Manage countries/region release location
2. Go To Release :
   1. Play app signing, choose continue
   2. Upload your release.apk
   3. Fill up the form
   4. Save
   5. Review Release
   6. Start roll-out to production
   7. Wait for your apps to be reviewed by google, usually takes 2-3 days.


7.  Open developer content privacy if your apps rejected or your account suspended