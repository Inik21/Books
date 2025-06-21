# Chapter 1: Set up of the environment for developing mobile applications

## Visual Studio

Various possible applications for development:

- Console applications
- Windows applications
- Android applications

> "Faster development in Visual Studio compared to Android Studio" - Author's experience

## Set Up

### Installing Universal Windows Tools

As UWP is deprecated in Visual Studio 2022, it is recommended to use Visual Studio 2019 or lower version

1. Go to the Visual Studio Installer
2. Modify your version of Visual Studio
3. Select `Universal Windows Platform Development`
4. Click `Modify`

### Enabling Developer Mode

When opening your first `Blank App (Universal Windows)` project, you will be prompted to activate Developer Mode in the settings.

## Project Structure

### 1. MainPage.xaml

Contains the structure of the application's main page, written in XAML.

### 2. MainPage.xaml.cs

Contains the code for the `Mainpage.xaml`, written in C#. The code for each page is located in a file named `<page's name>.xaml.cs`

> Using the [MVVM](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel) (Model-View-ViewModel) architectural pattern allows the page's file to be almost empty and all the Business Logic to be separated in other classes

### 3. App.xaml

The Project File of the object for the Windows Store Application, written in XAML. It doesn't have any visual representation, but instead keeps the data and settings for the whole application. It can contain fonts, resources, themes - light and dark, etc.

```
<Application
    x:Class="App1.App"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:local="using:App1"
    RequestedTheme="Dark">

</Application>
```

### 4. App.xaml.cs

Contains the code for the `App.xaml` file. It processes different events - launch, activation, deactivation, etc. 

It also selects the page, which will be shown first in the application:

```
rootFrame.Navigate(typeof(MainPage), e.Arguments);
```

> This is the same `MainPage.xaml` page

### 5. Package.appxmanifest

This is the [Manifest](https://en.wikipedia.org/wiki/Manifest_file) file for the application. Here a lot of settings can be managed - title, paths to Tiles and Splash Screen, orientation of the screen, logo, etc. 
