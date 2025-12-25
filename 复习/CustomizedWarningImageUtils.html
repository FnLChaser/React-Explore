# create WPF window
Add-Type -AssemblyName PresentationCore
Add-Type -AssemblyName PresentationFramework
Add-Type -AssemblyName System.Windows.Forms
Add-Type -AssemblyName WindowsBase

$global:OverlayShow = $true
$global:OverlayWindow = $null

$xaml = @'
<Window
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    Title="Battery Warning"
    Width="640"
    Height="340"
    WindowStartupLocation="CenterScreen"
    WindowStyle="None"
    ResizeMode="NoResize"
    Background="#F2F2F2">

    <Border CornerRadius="12"
            Background="#F2F2F2"
            BorderBrush="#D0D0D0"
            BorderThickness="1">

        <Grid>
            <Grid.RowDefinitions>
                <!-- Header -->
                <RowDefinition Height="48"/>
                <!-- Content -->
                <RowDefinition Height="*"/>
                <!-- Footer -->
                <RowDefinition Height="72"/>
            </Grid.RowDefinitions>

            <!-- ================= Header ================= -->
            <Grid Grid.Row="0" Background="#E6E6E6">
                <Grid.ColumnDefinitions>
                    <ColumnDefinition Width="*"/>
                    <ColumnDefinition Width="Auto"/>
                </Grid.ColumnDefinitions>

                <!-- Left title -->
                <TextBlock Text="User Account Control"
                           VerticalAlignment="Center"
                           Margin="16,0,0,0"
                           FontSize="14"
                           Foreground="#666"/>

                <!-- Right HSBC -->
                <StackPanel Grid.Column="1"
                            Orientation="Horizontal"
                            VerticalAlignment="Center"
                            Margin="0,0,16,0">

                    <!-- HSBC Logo (vector placeholder) -->
                    <Polygon Points="0,10 10,0 20,10 10,20"
                             Fill="#D32F2F"
                             Width="16"
                             Height="16"
                             Margin="0,0,6,0"/>

                    <TextBlock Text="HSBC"
                               FontSize="14"
                               FontWeight="Bold"
                               Foreground="#D32F2F"/>
                </StackPanel>
            </Grid>

            <!-- ================= Content ================= -->
            <Grid Grid.Row="1" Margin="32">
                <Grid.ColumnDefinitions>
                    <ColumnDefinition Width="120"/>
                    <ColumnDefinition Width="*"/>
                </Grid.ColumnDefinitions>

                <!-- Warning icon -->
                <StackPanel Grid.Column="0"
                            HorizontalAlignment="Center"
                            VerticalAlignment="Center">

                    <Polygon Points="50,0 100,86 0,86"
                             Fill="#D32F2F"/>

                    <TextBlock Text="!"
                               FontSize="48"
                               FontWeight="Bold"
                               Foreground="White"
                               HorizontalAlignment="Center"
                               Margin="0,-70,0,0"/>
                </StackPanel>

                <!-- Text and battery -->
                <StackPanel Grid.Column="1"
                            VerticalAlignment="Center"
                            Margin="24,0,0,0">

                    <TextBlock Text="Critical Battery Level: 35%"
                               FontSize="20"
                               FontWeight="Bold"
                               TextWrapping="Wrap"
                               Margin="0,0,0,12"/>

                    <TextBlock Text="Please connect the power adapter immediately to avoid data loss."
                               FontSize="14"
                               Foreground="#444"
                               TextWrapping="Wrap"
                               Margin="0,0,0,20"/>

                    <!-- Battery graphic -->
                    <Grid Width="120" Height="36" HorizontalAlignment="Left">
                        <Border BorderBrush="#555"
                                BorderThickness="2"
                                CornerRadius="4"/>

                        <Border Background="#D32F2F"
                                Width="40"
                                Margin="4"/>

                        <Rectangle Width="8"
                                   Height="16"
                                   Fill="#555"
                                   HorizontalAlignment="Right"
                                   VerticalAlignment="Center"
                                   Margin="0,0,-10,0"/>
                    </Grid>
                </StackPanel>
            </Grid>

            <!-- ================= Footer ================= -->
            <Grid Grid.Row="2">
                <Button Name="CloseWarning"
                        Content="Close Warning"
                        Width="180"
                        Height="42"
                        Background="#1976D2"
                        Foreground="White"
                        FontSize="16"
                        FontWeight="Bold"
                        BorderThickness="0"
                        HorizontalAlignment="Center"
                        VerticalAlignment="Center"/>
            </Grid>

        </Grid>
    </Border>
</Window>
'@

try {
    $reader = [System.Xml.XmlReader]::Create((New-Object System.IO.StringReader $xaml))
    $window = [System.Windows.Markup.XamlReader]::Load($reader)
    $reader.Close()

    if ($window -is [System.Windows.Window]) {
        $global:OverlayWindow = $window

        $closeWarningButton = $window.FindName("CloseWarning")
        if ($null -ne $closeWarningButton) {
            $closeWarningButton.Add_Click({
                $global:OverlayShow = $false
                if ($global:OverlayWindow -ne $null) {
                    $global:OverlayWindow.Close()
                }
            })
        }

        # bind top-right close button as well
        $topCloseButton = $window.FindName("TopClose")
        if ($null -ne $topCloseButton) {
            $topCloseButton.Add_Click({
                $global:OverlayShow = $false
                if ($global:OverlayWindow -ne $null) {
                    $global:OverlayWindow.Close()
                }
            })
        }

        $window.Topmost = $true
        $window.ShowDialog() | Out-Null
    } else {
        throw "Loaded XAML is not a Window object."
    }

} catch {
    Write-Error "Error occurs: $_"
    $global:OverlayShow = $false
}



