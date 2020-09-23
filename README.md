<div align="center">

## ReadFile


</div>

### Description

Read an entire text file into a string in one call.
 
### More Info
 
sFileName As String

String containing file contents.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[James Vincent Carnicelli](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/james-vincent-carnicelli.md)
**Level**          |Unknown
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[String Manipulation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/string-manipulation__1-5.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/james-vincent-carnicelli-readfile__1-3964/archive/master.zip)





### Source Code

```
Public Function ReadFile(ByVal sFileName As String) As String
  Dim fhFile As Integer
  fhFile = FreeFile
  Open sFileName For Binary As #fhFile
  ReadFile = Input$(LOF(fhFile), fhFile)
  Close #fhFile
End Function
```

