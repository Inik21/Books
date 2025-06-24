# Pages of the Application and Navigation between them

Usually, most applications have multiple pages. One of the pages should be the main one, appearing first when starting the application. By default, this is the `MainPage.xaml`. 
In this Chapter, we will add a second page and see how to access it. Additionally, we will look more in detail at the `App.xaml.cs` file. 

## App.xaml.cs - setting the main page

The method `OnLaunched()` is called when the application is started. 

when going into the state *Suspend*, the method `OnSuspending` is called. This method saves the state of the application 
without knowing whether the application will be terminated or resumed with the contents of memory still intact.

To be able to load different pages and also implement the transitions between them, in the `OnLaunched()` method, an object of class `Frame` is created. 
The `Frame` takes up the entire window of the application and is responsible for the navigation between the pages

``` C#
Frame rootFrame = Window.Current.Content as Frame;
```

``` C#
rootFrame.Navigate(typeof(MainPage), e.Arguments);
```

## Creating a new Page


