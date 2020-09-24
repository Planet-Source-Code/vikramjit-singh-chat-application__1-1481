<div align="center">

## Chat application


</div>

### Description

Create a simple chat application betweenany two computers whose IP addresses you know. The DEMO here shows how to chat with your own computer .you can substitute your own IP with that of another person's IP and create a seperate EXE running on his computer to chat with him /her

COOL!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Vikramjit Singh](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/vikramjit-singh.md)
**Level**          |Unknown
**User Rating**    |4.2 (161 globes from 38 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Internet/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-html__1-34.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/vikramjit-singh-chat-application__1-1481/archive/master.zip)





### Source Code

```
'Open a project Exe. Put a winsock, and two textbox control ,named text2 and 'text3. Paste this code in it.
Private Sub Form_Load()
With Winsock1
.RemoteHost = "your machine IP" 'put your or someone else's IP here
.RemotePort = 1001
.Bind 1002
End With
chat1.Show
End Sub
Private Sub Text3_Change()
Winsock1.SendData Text3.Text
End Sub
Private Sub Winsock1_DataArrival(ByVal bytesTotal As Long)
Dim strData As String
Winsock1.GetData strData
Text2.Text = strData
End Sub
'********************************************************************
'paste code below into another form having 2 text boxes and winsock
'control in the SAME project
'********************************************************************
Private Sub Form_Load()
With Winsock1
.RemoteHost = "your machine IP" 'put your or someone else's IP here
.RemotePort = 1002
.Bind 1001
End With
End Sub
Private Sub Text3_Change()
Winsock1.SendData Text3.Text
End Sub
Private Sub Winsock1_DataArrival(ByVal bytesTotal As Long)
Dim strData As String
Winsock1.GetData strData
Text2.Text = strData
End Sub
```

