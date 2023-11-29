# How-to-zoom-Y-axis-or-X-axis-alone

This article explains how to customize the zoom for the y-axis or x-axis individually in the [Blazor Chart](https://www.syncfusion.com/blazor-components/blazor-charts).

**Customizing the zoom mode**

You can customize the zoom mode by using the [Mode](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartZoomSettings.html#Syncfusion_Blazor_Charts_ChartZoomSettings_Mode) property in [ChartZoomSettings](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartZoomSettings.html) determines whether the chart can scale along the horizontal or vertical axes. The default value of the mode is XY (both axis).

[Mode](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartZoomSettings.html#Syncfusion_Blazor_Charts_ChartZoomSettings_Mode) property in includes the following zooming mode option:

- X - Allows us to zoom the chart horizontally.
- Y - Allows us to zoom the chart vertically.
- XY - Allows us to zoom the chart both vertically and horizontally. 

In the below code example, the [Mode](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartZoomSettings.html#Syncfusion_Blazor_Charts_ChartZoomSettings_Mode) property is set to X. This will allow you to zoom only along X-axis while the zooming along Y axis is restricted.

**C#**

 ```cshtml

 @using Syncfusion.Blazor.Charts

<SfChart Title="Sales History of Product X">

    <ChartPrimaryXAxis ValueType="Syncfusion.Blazor.Charts.ValueType.Category"></ChartPrimaryXAxis>

    <ChartZoomSettings EnableSelectionZooming="true" Mode="ZoomMode.X"></ChartZoomSettings>

    <ChartSeriesCollection>
        <ChartSeries DataSource="@SalesReports" XName="X" YName="YValue" Type="ChartSeriesType.Column"></ChartSeries>
    </ChartSeriesCollection>

</SfChart>

@code {
    public class ChartData
    {
        public string X { get; set; }
        public double YValue { get; set; }
    }

    public List<ChartData> SalesReports = new List<ChartData>
    {
        new ChartData { X= "USA", YValue= 46 },
        new ChartData { X= "GBR", YValue= 27 },
        new ChartData { X= "CHN", YValue= 15 },
        new ChartData { X= "UK", YValue= 20 },
        new ChartData { X= "AUS", YValue= 50 },
        new ChartData { X= "IND", YValue= 26 },
        new ChartData { X= "DEN", YValue= 30 },
        new ChartData { X= "MEX", YValue= 26 },
    };
}

```

The following screenshot illustrate the output of the above code snippet.

**Output:**

![](/Zooming-X-or-Y-Axis.gif)

 **Conclusion**

I hope you enjoyed learning how to zoom X-axis or Y-axis alone in Blazor Chart Component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!







