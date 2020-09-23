<div align="center">

## Enter Key in ASP\.NET


</div>

### Description

This article is solving very common problem when ASP.NET developers wants to get button "clicked" and submit a form when web site visitor hit an Enter key. That is useful when you want to build Login screen, web site search, pool etc.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Richard Bean](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/richard-bean.md)
**Level**          |Intermediate
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C\#, VB\.NET, ASP\.NET
**Category**       |[Controls/ Forms/ Dialogs/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-dialogs-menus__10-3.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/richard-bean-enter-key-in-asp-net__10-4236/archive/master.zip)





### Source Code

```
You can have only one text box and one button on a web form, but it is possible to have a lot of those elements (e.g. you can have on the same page web site search, login and pool).
We need to specify exactly what button will be "cliked" when visitor press Enter key, according to what textbox currently has a focus. The solution could be to add onkeydown attribute to textbox control:
 TextBox1.Attributes.Add("onkeydown", "if(event.which || event.keyCode){if ((event.which == 13) || (event.keyCode == 13)) {document.getElementById('"+Button1.UniqueID+"').click();return false;}} else {return true}; ");
This line of code will cause that button Button1 will be "clicked" when visitor press Enter key and cursor is placed in TextBox1 textbox.
On this way you can "connect" as many text boxes and buttons as you want.
Full research of Enter key problem in ASP.NET, including ASP.NET 2.0 you can see on http://www.beansoftware.com/ASP.NET-Tutorials/Accept-Enter-Key.aspx
```

