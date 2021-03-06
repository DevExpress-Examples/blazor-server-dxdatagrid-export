*Files to look at*:

* [Index.razor](./CS/DxDataGridExportingWithReports/Pages/Index.razor)
* [ExportMiddleware.cs](./CS/DxDataGridExportingWithReports/Helpers/ExportMiddleware.cs)
* [ReportHelper.cs](./CS/DxDataGridExportingWithReports/Helpers/ReportHelper.cs)
* [ExportButtons.razor](./CS/DxDataGridExportingWithReports/Components/ExportButtons.razor)

### DataGrid for Blazor - Server application - How to implement the exporting functionality using DevExpress Reporting tools 

This example illustrates how to use DevExpress Reporting tools to export DxDataGrid's content to different formats (*.pdf*/*.xlsx*/*.docx*) in the Blazor Server applications.


This example demonstrates how to apply the [ExportMiddleware](./CS/DxDataGridExportingWithReports/Helpers/ExportMiddleware.cs) type to the application's request pipeline. Requests are handled via this middleware, and the file of the corresponding type is returned in the response.

The export buttons are located within the [ExportButtons](./CS/DxDataGridExportingWithReports/Components/ExportButtons.razor) components. Each of them contains an [URI to this project](./CS/DxDataGridExportingWithReports/Pages/Index.razor#L32). The request with this URI will be processed by the mentioned middleware. Also, this URI contains DataGrid's options, so the created report will only contain data that is displayed in the grid after sorting and filtering are applied.

The [ReportHelper.CreateReport](./CS/DxDataGridExportingWithReports/Helpers/ReportHelper.cs#L9) method is used to create a report that is exported to the file of the corresponding type using the [ExportToPdf(String)](https://docs.devexpress.com/XtraReports/DevExpress.XtraReports.UI.XtraReport.ExportToPdf(System.String))/[ExportToXlsx(Stream)](https://docs.devexpress.com/XtraReports/DevExpress.XtraReports.UI.XtraReport.ExportToXlsx(System.IO.Stream))/[ExportToDocx(Stream)](https://docs.devexpress.com/XtraReports/DevExpress.XtraReports.UI.XtraReport.ExportToDocx(System.IO.Stream)) method.

See also:

[DataGrid for Blazor - Client side - How to implement the exporting functionality using DevExpress Reporting tools](https://supportcenter.devexpress.com/ticket/details/t854758/datagrid-for-blazor-client-side-how-to-implement-the-exporting-functionality-using)

[How to use DevExpress Reporting Components in Blazor applications](https://supportcenter.devexpress.com/ticket/details/t834711/how-to-use-devexpress-reporting-components-in-blazor-applications)
