<div align="center">

## Delphi Text Editor Code


</div>

### Description

Here's all the code to create your own editor!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[N/A](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/empty.md)
**Level**          |Intermediate
**User Rating**    |4.0 (32 globes from 8 users)
**Compatibility**  |Delphi 5, Delphi 4, Pre Delphi 4
**Category**       |[Complete Applications](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/complete-applications__7-27.md)
**World**          |[Delphi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/delphi.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/delphi-text-editor-code__7-64/archive/master.zip)





### Source Code

<p> </p>
<table>
 <tr>
 <td><b><font color="#000099"><font face="Verdana">Bold</font></font></b><font face="Verdana"><br>
  CurrText.Style := CurrText.Style + [fsBold];<br>
  <b><font color="#000099">Regular</font></b><br>
  CurrText.Style := CurrText.Style - [fsBold];</font></td>
 </tr>
 <tr>
 <td><b><u><font color="#000099" face="Verdana">To insert the Date and Time
  in a Editor:</font></u></b>
  <p><font face="Verdana">procedure TForm1.Date1Click(Sender: TObject);<br>
  begin<br>
      Editor.SelText := (FormatDateTime('ddd, mmm d, yyyy ',
  Now));<br>
  end;<br>
  procedure TForm1.Time1Click(Sender: TObject);<br>
  begin<br>
      Editor.SelText := (FormatDateTime('hh:mm AM/PM ',
  Now));<br>
  end;<br>
   </font></p>
 </td>
 </tr>
 <tr>
 <td><b><u><font color="#000099" face="Verdana">Paste from Clipboard:</font></u></b>
  <p><font face="Verdana">procedure TForm1.Paste1Click(Sender: TObject);<br>
  begin<br>
      Editor.PasteFromClipboard;<br>
  end;<br>
   </font></p>
 </td>
 </tr>
 <tr>
 <td><b><u><font color="#000099" face="Verdana">Copy to the Clipboard:</font></u></b>
  <p><font face="Verdana">procedure TForm1.Copy1Click(Sender: TObject);<br>
  begin<br>
      Editor.CopyToClipboard;<br>
  end;<br>
   </font></p>
 </td>
 </tr>
 <tr>
 <td><b><u><font color="#000099" face="Verdana">Cut to the Clipboard:</font></u></b>
  <p><font face="Verdana">Editor.CutToClipboard;<br>
   </font></p>
 </td>
 </tr>
 <tr>
 <td><b><font color="#000099"><font face="Verdana">Editor Alignments. Left -
  Right - Center.</font></font></b><font face="Verdana"><br>
  begin<br>
      Editor.Alignment := taLeftJustify;<br>
  end;<br>
  begin<br>
      Editor.Alignment := taRightJustify;<br>
  end;<br>
  begin<br>
      Editor.Alignment := taCenter;<br>
  end;</font></td>
 </tr>
 <tr>
 <td><font face="Verdana"><b><font color="#000099">Counting Characters in a
  text file (Editor).Using a Dialog.</font></b><br>
  begin<br>
    MessageDlg (Format (<br>
      'The text has %d characters', [Memo1.GetTextLen]),<br>
      mtInformation, [mbOK], 0);<br>
  end;</font></td>
 </tr>
 <tr>
 <td><b><font color="#000099" face="Verdana">SetFocus:</font></b>
  <p><font face="Verdana">Editor.SetFocus;<br>
  Memo1.SetFocus;<br>
  etc...<br>
   </font></p>
 </td>
 </tr>
 <tr>
 <td><b><font color="#000099" face="Verdana">Changing a Editor colour. Using
  the ColorDialog:</font></b>
  <p><font face="Verdana">begin<br>
      ColorDialog1.Color := Editor.Color;<br>
    if ColorDialog1.Execute then<br>
      Editor.Color := ColorDialog1.Color;<br>
  end;<br>
   </font></p>
 </td>
 </tr>
 <tr>
 <td><b><font color="#000099" face="Verdana">Positioning the Caret in a
  Editor:</font></b>
  <p><font face="Verdana">procedure TForm1.Button1Click(Sender: TObject);<br>
  begin<br>
      Editor.SetFocus;<br>
      Editor.SelStart  :=  2;<br>
  end;</font>
  <p><font face="Verdana">0 is the first character.</font></p>
 </td>
 </tr>
 <tr>
 <td><font face="Verdana"><b><font color="#000099">Using Quick Reports for a
  Text Editor Preview </font></b><font color="#000000">(Simple Example)</font><font color="#000099">.</font></font>
  <p><font face="Verdana">First drop a TQuickRep on a Form,<br>
  Put a DetailBand on it,<br>
  Then drop a TQRMemo on the DetailBand.</font>
  <p><font face="Verdana">Form3.QRMemo1.lines := Editor.Lines;<br>
  Form3.QuickRep1.Preview;</font></p>
 </td>
 </tr>
 <tr>
 <td><b><font color="#000099" face="Verdana">To get a Text Editor to load a
  text file when your Text Editor is associated with your systems *.txt
  files.</font></b>
  <p><font face="Verdana">procedure TForm1.FormShow(Sender: TObject);<br>
  begin<br>
      if (ParamCount > 0) and FileExists(ParamStr(1)) then<br>
       
  Form1.Memo1.Lines.LoadFromFile(ParamStr(1));<br>
  end;</font></p>
 </td>
 </tr>
 <tr>
 <td><font face="Verdana">This will put the opened files name on the taskbar
  button and shows you how to use <b><font color="#000099">ExtractFileName</font></b>
  .<br>
  Application.Title := ExtractFileName(OpenDialog.FileName);</font></td>
 </tr>
 <tr>
 <td><center><b><font color="#000099" face="Verdana">Loading a text file into
  a TMemo</font></b></center>
  <ol>
  <li><b><font face="Verdana">First start a new project.</font></b>
  <li><b><font face="Verdana">Place Memo1 (TMemo) on Form1</font></b>
  <li><b><font face="Verdana">Set Memo1 Align to alBottom</font></b>
  <li><b><font face="Verdana">Place Button1 (TButton) on Form1 at the top
   of Form1</font></b>
  <li><b><font face="Verdana">Click on Form1 and in the Object Inspector
   click on Events</font></b>
  <li><b><font face="Verdana">DoubleClick on OnCreate</font></b>
  <li><b><font face="Verdana">Type in this code:</font></b></li>
  </ol>
  <font face="Verdana"><b><font color="#000000">begin</font></b><br>
  <b>    Memo1.Lines.LoadFromFile('c:\ssapcs\desktop1\config1.txt');</b><br>
  <b>end;</b><br>
  <b><font color="#000099">{ Your text file will be in a directory (Folder)
  that you want to load }</font></b></font>
  <p><b><font face="Verdana">    Next DoubleClick on Button1
  and type this code</font></b>
  <p><font face="Verdana"><b>begin</b><br>
  <b>    Memo1.Clear;</b><br>
  <b>end;</b></font>
  <p><b><font face="Verdana"> Run Project1 (Or whatever you called it),
  now you should be able to see the text from</font></b><font face="Verdana"><br>
  <b> c:\ssapcs\desktop1\config1.txt  in Memo1.</b><br>
  <b> Click on Button1 and Memo1 will clear.</b></font><center>
  <p><font face="Verdana"><b><font color="#000099">Hows that for easy!</font></b><br>
  </font>
  <hr width="100%">
  <b><font face="Verdana">Part 2</font></b>
  <p><b><font face="Verdana">Saving the Memo lines to a text file is simple.</font></b></center>
  <p><font face="Verdana"><b><font color="#000099">Put 3 Buttons on Form1,
  keep Memo1 on the Form.</font></b><br>
  <b><font color="#000099">Name the first Button '</font><font color="#cc0000">Open</font><font color="#000099">',
  name the second Button  '</font><font color="#cc0000">Save</font><font color="#000099">'
  and</font></b><br>
  <b><font color="#000099">name the third Button '</font><font color="#cc0000">Clear</font><font color="#000099">'.</font></b><br>
  <b><font color="#000099">Double-Click on the button named '</font><font color="#cc0000">Open</font><font color="#000099">',
  write this code between 'begin' and 'end'</font></b></font>
  <p><font face="Verdana"><b>procedure TForm1.OpenClick(Sender: TObject);</b><br>
  <b>begin</b><br>
  <b>  Memo1.Lines.LoadFromFile('c:\ssapcs\desktop1\config1.txt');</b><br>
  <b>  Save.Enabled := True;</b><br>
  <b>end;</b></font>
  <p><b><font face="Verdana"><font color="#000099">Double-Click on the
  button named '</font><font color="#cc0000">Save</font><font color="#000099">',
  write this code between 'begin' and 'end'</font></font></b>
  <p><font face="Verdana"><b>procedure TForm1.SaveClick(Sender: TObject);</b><br>
  <b>begin</b><br>
  <b>  Memo1.Lines.SaveToFile('c:\ssapcs\desktop1\config1.txt');</b><br>
  <b>end;</b></font>
  <p><b><font face="Verdana"><font color="#000099">Double-Click on the
  button named '</font><font color="#cc0000">Clear</font><font color="#000099">',
  write this code between 'begin' and 'end'</font></font></b>
  <p><font face="Verdana"><b>procedure TForm1.ClearClick(Sender: TObject);</b><br>
  <b>begin</b><br>
  <b>  Memo1.Clear;</b><br>
  <b>end;</b></font>
  <p><b><font color="#000099" face="Verdana">Note the names of the
  procedures.</font></b>
  <p><b><font face="Verdana">In the Object Inspector set the '<font color="#cc0000">Save</font>'
  Button to Enabled := False;</font></b>
  <p><font face="Verdana"><b>Make sure you use the path to a file that
  exists and you don't mind editing this file.</b><br>
  <b>Run the program, click on the open button add some text to the Memo
  then click on the save button, click on the clear button and open the file
  again.</b></font><center>
  <hr width="100%">
  <b><font face="Verdana">Part 3</font></b>
  <p><font face="Verdana"><b><font size="+1" color="#000099">A Simple Text
  Editor</font></b></center><font color="#000000">Here is a simple text
  editor that uses a Memo and four buttons, the OpenDialog, and the
  SaveDialog.</font></font>
  <p><font face="Verdana"><font color="#000000">This was made with Delphi 3,
  with a few small changes it should work on all versions of Delphi.</font><br>
  <font color="#000000">Study it carefully, this program will open a file,
  then you can edit the file then save the file or clear the memo and start
  again. Also a Close button is included to close the program.</font><br>
  <font color="#000000">If you want to add to this text editor program have
  a look at our Delphi Tips web page for some code and ideas.</font></font>
  <p><font color="#000000" face="Verdana">Download here - <a href="http://members.xoom.com/sandbrook/downloads/Download.htm">Download</a>.</font></p>
 </td>
 </tr>
</table>

