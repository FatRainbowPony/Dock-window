# Dock Window
Dock window implementation of WPF base off [Using Application Desktop Toolbars](https://learn.microsoft.com/en-us/windows/win32/shell/application-desktop-toolbars)

 ## Features
- Docking to any edge and monitor 
- Supporting automatic hiding
- Cooperating with other desktop toolbars

## Usage
Create a WPF window and select the `DockWindow` class instead of the `Window` class. Needs to done  both in XAML and code

- XAML
```xml
<dw:DockWindow 
    x:Class="DockWindowDemo.MainWindow"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:dw="clr-namespace:DockWindow.Windows;assembly=DockWindow"
    mc:Ignorable="d"
    Title="MainWindow" 
    Background="Transparent"
    BorderBrush="Transparent"
    BorderThickness="0"
    AllowsTransparency="True"
    DockWidthOrHeight="150"
    AnimationBackground="White">
    <Grid>
    </Grid>
</dw:DockWindow>
```

- Code
```csharp
namespace DockWindowDemo
{
    public partial class MainWindow : DockWindow.Windows.DockWindow
    {
        public MainWindow()
        {
            InitializeComponent();
        }
    }
}
```