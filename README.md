# nvid-hardid-mod
Replace one hardware ID  with another in a video card driver verification file

Const ForReading = 1
Const ForWriting = 2

Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objFile = objFSO.OpenTextFile("C:\Scripts\Text.txt", ForReading)

strText = objFile.ReadAll
objFile.Close
strNewText = Replace(strText, "hdwid1", "hdwid2")

Set objFile = objFSO.OpenTextFile("C:\Scripts\Text.txt", ForWriting)
objFile.WriteLine strNewText
objFile.Close

Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objFile = objFSO.OpenTextFile("C:\Scripts\Text.txt", ForReading)

strText = objFile.ReadAll
objFile.Close
strNewText = Replace(strText, "hdwid3", "hdwid4")

Set objFile = objFSO.OpenTextFile("C:\Scripts\Text.txt", ForWriting)
objFile.WriteLine strNewText
objFile.Close
