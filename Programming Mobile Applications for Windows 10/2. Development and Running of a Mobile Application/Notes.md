
# Development and Running of a Mobile Application

Developing your first mobile application - an application to calculate the expenses of gas for a vehicle

Things to learn:

- How to position components on the form
- How to change the properties of a component
- How to select a target device
- How to create a handler for a specific event
- How to correctly transform data types

## The Graphical Interface

To open the Graphical Interface (XAML Designer) for any  `.xaml` file, double-click on it

![image](https://github.com/user-attachments/assets/2715c55c-b85e-4212-ae06-0d8025d25c27)

In the upper left corner, the device type and size can be changed.

In the Toolbox Panel, there are various elements to choose from:

- TextBlock - a block of text
- TextBox - an input field for text
- Button - a button
- etc.

![image](https://github.com/user-attachments/assets/36c2d863-13a7-4ab9-a827-5046a2a21db4)

In the Properties Panel, the properties of the selected component can be changed

![image](https://github.com/user-attachments/assets/08be292a-d29f-4601-b33c-7cad31a58bb3)'

*The properties of a `TextBlock` component*

## Handling the Click of a Button

This is the current layout of the application

![image](https://github.com/user-attachments/assets/8c6ecec0-970c-49dd-bfd7-d3a302c90b11)

By double-clicking the `Button` component, the `MainPage.xaml.cs` file will be opened and a method `Button_Click` will be generated for the button. We will write the logic for the application there.

``` C#
private void Button_Click(object sender, RoutedEventArgs e)
        {
            double dMileage = Double.Parse(mileage.Text);
            double dLiters = Double.Parse(liters.Text);
            double dConsumption = 100 * dLiters / dMileage;
            consumption.Text = dConsumption.ToString("##.##");
        }
```

Here, `mileage`, `liters` and `consumption` are the names of the three `TextBox` components, and we are using their `Text` property to get the inputs and also to set the output.

> The `Button_Click` method and the `Button` component are connected by specifying which method to call on the `Click` action in the `MainPage.xaml` file
> ``` XAML
> <Button Content="Calculate" Margin="61,315,0,0" VerticalAlignment="Top" Width="95" Click="Button_Click"/>
> ```

## Compiling and Running the Application

Just click on the `Local Machine` button, and the application will be built and start running. After that, you have a working calculator for the expenses of a car (granted, a very simple one)











