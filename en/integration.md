# 🤝 Integration with application

## Windows and Microsoft .NET

- Windows Forms - [WebBrowser][WebBrowser].Navigate(URI)
- WPF - [WebView2][WebView2].Source
- Run web browser with URI path
- Run URI with ShellAPI.[ShellExecuteW][ShellExecuteW]:
```cpp
ShellExecuteW(NULL, "open", 
  "https://helpviewer.github.io/?d=hlp%2FHelp-__.zip&p=ideas.md", 
  NULL, NULL, SW_SHOWNORMAL);
```
- Run URI with System.Diagnostics.[Process.Start][Process-Start]:
```csharp
Process.Start(new ProcessStartInfo(
  "https://helpviewer.github.io/?d=hlp%2FHelp-__.zip&p=ideas.md"
  ) { UseShellExecute = true });
```

## Web solutions

- Direct a href links to HelpViewer across your web
- HelpViewer as main UI of your web application
- Use iframe with showing of HelpViewer content

## Linux

- xdg-open 
```  
xdg-open "https://helpviewer.github.io/?d=hlp%2FHelp-__.zip&p=ideas.md"
```
- .desktop link

[WebBrowser]: https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.webbrowser?view=netframework-4.8.1 "WebBrowser"
[WebView2]: https://learn.microsoft.com/en-us/dotnet/api/microsoft.web.webview2.wpf.webview2?view=webview2-dotnet-1.0.3124.44 "WebView2"
[ShellExecuteW]: https://learn.microsoft.com/en-us/windows/win32/api/shellapi/nf-shellapi-shellexecutew "shellapi.h > ShellExecuteW"
[Process-Start]: https://learn.microsoft.com/en-us/dotnet/api/system.diagnostics.process.start?view=net-8.0 "System.Diagnostics.Process.Start"
  