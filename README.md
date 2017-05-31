# Desktop Bridge Session Demos for BuildTour 2017


## Setup

1. Install the following apps from The Windows Store

    * [Winforms AppService](https://www.microsoft.com/en-us/store/p/winforms-appservice/9p7d9b6nk5tn)

    * [AutoClick ComServer](https://www.microsoft.com/store/apps/9nm1gvnkhjnf)

    * [WPF App as ShareTarget](https://www.microsoft.com/en-us/store/p/wpf-app-as-sharetarget/9pjcjljlck37)

    * [The Hack Checklist](https://www.microsoft.com/en-us/store/p/the-hack-checklist/9n1b7mhnd7m1)


1. Install the app in the TestClient_1.0.3.0_Test folder

    * Right click on Add-AppDevPackage.ps1
    * Select Run with PowerShell
    

## Before each session

1. Make sure the FlightTracker App is uninstalled on the computer

1. Install the FlightTracker signing certificate.

    1. Right-click on FlightTracker-AppX\auto-generated.cer, select Install Certificate

    1. Select Local Machine. Click Next

    1. Select Place all certificates in the following store.  Click Browse

    1. Select Trusted Publisher or Trusted People. Click Next

    1. Click Finish then OK


1. Remove all files (if the folder exists) in 
    
    C:\Users\<username>\AppData\Local\Packages\17855StefanWick.WPFAppasShareTarget_bvbr2n7re90hg\LocalState
    
# Demos   
## Sideloading Demo

1. Open the FlightTracker-AppX folder

1. Double-click on FlightTracker.appx

1. Install the app. Point out that the UWP version is exactly the same as the original WinForms versions

1. Uninstall the app. Uninstall leaves the computer the way it was before installing the app

## Modernize Demos

### WPF as Share Target App

**Key Point:** The WPF Photo app was modernized by adding a XAML UI that enabled integration into the Window 10 Sharing feature.

1. Open the desktopbridge-demos folder

1. Doubleclick on the Build_Tour_2017_Collage.jpg.

1. You want the Windows Photos app (or any other app that can share photos) to launch

1. Right click on the image and select Share from the popup menu

1. Select the WPF as Share Target app from the Share options

1. A WPF as Share Target XAML windows will appear. 

1. Click on the Share to WPF App

1. The Desktop Bridge WPF as Share Target App will appear with the image in the photo list.

1. Click on the image in the photo list to display it in the center.

1. Close the app.

### Hack CheckList App

Key Point: The Hack Checklist App for the Hackathon is a desktop bridge app. It was modernized by adding a XAML UI that communicates using a UWP App Service with a Win32
app that checks the user's computer for the required software.

1. Launch the Hack Checklist app. Point out the XAML UI. 

1. Click on the Check Now button. Point out that the tests are happening in a UWP background task that is running a Windowsless Win32 app. Communication between the apps
is enabled by using a UWP App Service.

1. Close the app.

### Winforms AppService Data Exchange

**Keypoint:** The orginal WinForms Data app was modernized with the Desktop Bridge and the use of an App Service to share its data with other UWP apps.

1. Launch the Winforms Data App

1. Launch the Test Client for the Winforms AppService App

1. In the Test Client app click on Connect

1. Click on the Submit Button. Data for the requested record will be displayed.

1. In the Winforms Data App create and save a new record.

1. In the Test Client app enter the neew record number and click Submit.

1. The new record will appear.


## Packaged Com Demo (if there is time)

**Key Points:**

In this example, we packaged the ACDual Com Server app for the Desktop Bridge. 
ACDual is an MFC OLE sample that shipped in earlier versions of Visual Studio. A
CDual.exe is a COM server with a Document CoClass that implements the IDualAClick interface. 
In the foreground is a simple WinForms client app that is using these COM interfaces. 
This demo is available from the Window Store and also from GitHub,
The keys to enabling this functionality are the new app manifest extension categories “windows.comServer” and “windows.comInterface.” 
1. Launch Packaged-Com-Demo\WindowsFormsApp2.exe

1. It will launch the Desktop Bridge COM Server ACDual

1. Click on the Get All button. The text and position of the text will be retrieved.

1. Change the text to Hello and X and Y to 100. 

1. Click the Set All button. The text will change and move in the ACDual Com Server app.








