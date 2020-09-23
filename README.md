<div align="center">

## Get Server Variable Info


</div>

### Description

To gather all server variables, and display them nicely in a readable format.
 
### More Info
 
Create a page where you want all the server variable information to display.

Nothing, just copy and paste.

This code returns all the server variable information and displays them with alternating row color.

None that I am aware of.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Matt Khoury](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/matt-khoury.md)
**Level**          |Intermediate
**User Rating**    |4.5 (27 globes from 6 users)
**Compatibility**  |ASP \(Active Server Pages\), HTML, VbScript \(browser/client side\)

**Category**       |[ASP Server Object Model](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/asp-server-object-model__4-32.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/matt-khoury-get-server-variable-info__4-6684/archive/master.zip)

### API Declarations

Just include my name, and information where you use this code.


### Source Code

```
<TABLE WIDTH="100%" BORDER="1" CELLSPACING="0" CELLPADDING="0">
<%
'--Created by: Matthew J. Khoury
Dim strSV, intRowColor
For Each strSV In Request.ServerVariables
	If intRowColor = 0 Then
		Response.Write "<TR bgcolor=""#ddddfc"">"
		intRowColor = 1
	Else
		Response.Write "<TR bgcolor=""#ffffff"">"
		intRowColor = 0
	End if
Response.Write "<TD> " & strSV & "=" & Request.ServerVariables(strSV) & "</TD></TR>"
Next
%>
</TABLE>
```

