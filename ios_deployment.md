---
Author: Muammar Al Farabi
---
# iOS App Deployment Documentation v1.0

```
> Prerequisite:
  - Apple Developer account
  - Macbook with Xcode
  - Project for deployment
```
# Preparation

## Step 1: Set the Bundle ID, Version Number, and Build String

Whenever you generate project template from React Native or Xcode, the bundle ID, which uniquely identifies your app throughout the system, defaults to the organization ID appended to the app name that you enter in reverse-DNS format—for example, the bundle ID becomes _com.example.mycompany.HelloWorld_.

### About Bundle ID

To distribute your app through TestFlight and the App Store, you create an app record in App Store Connect and enter a bundle ID that matches the one in your project. After you upload your first build to App Store Connect, you **can’t change the bundle ID**, so **carefully choose the organization ID when you create the project**, or edit the bundle ID afterward. You can edit the name of the app until you submit the app to App Review.

### About Version Number and Build String

The version number and build strin uniquely identify the build of your app throughout the system. For apps distributed through TestFlight or the App Store, the report service generates crash, energy, and metrics reports for each build of an app version. The version number also appears in the App Store, and for macOS apps the version number and build string appear in the About window.

The version number and build string are expected to be in the format **[Major].[Minor].[Patch]** where Patch is a maintenance release, as in **10.14.1**. Both keys are required by the App Store. Set the version number and build string after you create the project. Increment the build string before you archive a build that you want to distribute. Then increment the version number when you create a new version of your app—for example, create a new app version in App Store Connect.

Set the bundle ID, version number, and build string for an app target on the General tab of the project editor, in the Identity section.

<img src="https://docs-assets.developer.apple.com/published/f9dd5c3b87db2857ef320e323d0e3fa0/preparing-your-app-for-distribution-1@2x.png" />

<br/>

## Step 2: Set the App Category

Choose a category from the App Category pop-up menu in the Identity section on the General pane of the project editor. For guidance with choosing the most accurate and effective categories, see Choosing a Category.

<img src='https://docs-assets.developer.apple.com/published/324491778129989b2ba79cc3f2dc6e1c/preparing-your-app-for-distribution-2@2x.png' />

<br/>

## Step 3: Edit Deployment Info Settings

Edit deployment info settings because some settings—such as the operating system and devices your app supports—are used by the App Store later.

Choose the earliest operating-system version that can run your app, from the Target pop-up menu under the Deployment Info settings on the General pane of the project editor.

<img src="https://docs-assets.developer.apple.com/published/a04109ac9e3b75de65879e9ba58b6850/preparing-your-app-for-distribution-4@2x.png" />

<br/>

## Step 4: Add an App Icon and App Store Icon

In the App Icons and Launch Images section of the General pane, click the arrow next to the AppIcon image set to open the asset catalog. Then drag variations of the app icon to the wells in the detail area of the asset catalog.

<img src="https://docs-assets.developer.apple.com/published/0b6b75825a1da2772f3f159f48307b84/preparing-your-app-for-distribution-5@2x.png"/>

<br/>

# Deployment

Based on this tutorial (<a href="https://www.youtube.com/watch?v=fXeDe9tafG8">How to Submit an App to the App Store! (2021 | Xcode) ー Jared Davidson</a>), here's the summary:

- In the Xcode, select Product > Archive
- On the Archives, select your app that you want to distribute, and then click Distribute App
- Select App Store Connect for method and then next
- Select Upload and then click next
- Click Next until Re-sign, select Automatically manage signing, and click next
- Re-check everything and then click Upload

If there is an Error **"App Store Connect Operation Error" "No suitable application records were found. Verify your bundle identifier '<your.app.bundle.id>' is correct."** You must add login to your Apple Developer account and add new application first. Here's how to do it:

- Open https://appstoreconnect.apple.com > click + icon > click "New App"
- Fill the information for your app, and make sure to select Full Access for User Access, and then click next
- Back to Xcode, click Upload, and it should be uploading

After Uploading, back to App Store Connect:

- Select your apps, and then click "App Store" tab
- Fill your app information, screenshot, copyright, etc
- And then click Submit for Review

> Note: App Store Review is reviewed by human and takes 3 days, so if the apps is still buggy, you probably will get the rejection message.

