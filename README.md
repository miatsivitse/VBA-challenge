# VBA-challenge

Option Explicit

Sub stocks()

Const FIRST_ROW As Long = 2
    
    Dim ws As Worksheet

    Dim TICKER As String
    Dim Yearly_Change As Double
    Dim Percent_Change As Double
    Dim Total_Stock_Volume As Long
    Dim LastRow As Long
    Dim CurrentRow As Long
    Dim OutputRow As Long
    
    'Loop through all of the sheets
    For Each ws In Worksheets
        'Add the Output Header
        ws.Cells(1, 9).Value = "Ticker"
        ws.Cells(1, 10).Value = "Yearly Change"
        ws.Cells(1, 11).Value = "Percent Change"
        ws.Cells(1, 12).Value = "Total Stock Volume"
        
        'Determine Last Row
        LastRow = ws.Cells(Rows.Count, 1).End(xlUp).Row
        
'        Worksheetname = ws.Name
'
'        '---------Iterate Through All Rows on Sheet--------
        For CurrentRow = FIRST_ROW To LastRow
        
'        If Cells(CurrentRow + 1, 1).Value <> Cells(CurrentRow, 1).Value Then
'            TICKER = Cells(CurrentRow, 1).Value
'            Total_Stock_Volume = Total_Stock_Volume + Cells(CurrentRow, 7).Value
'            Range("I" & OutputRow).Value = TICKER
'            Range("L" & OutputRow).Value = Total_Stock_Volume
'            Total_Stock_Volume = Total_Stock_Volume + 1
'            Total_Stock_Volume = 0
'
'        Else
'
'            Total_Stock_Volume = Total_Stock_Volume + Cells(CurrentRow, 7).Value

'        End If
        
'        'If (First row of new ticker):
'            'Volume = 0
'            'ticker = new_ticker # ??
'            'starting_price = Cells(row, OPEN_COL).Value
'        'EndIf
'
'            'Calculate Yearly Change
'            Yearly_Change = Cells(F2).Value - Cells(C2).Value
'
'            'Add Conditional Formatting to Indicate Positive or Negative Growth
'
'            If Range("J:J" > 0) Then
'               Range("J2:22771").Interior.ColorIndex = 4
'
'            ElseIf Range("J:J" < 0) Then
'            Range("J2:22771").Interior.ColorIndex = 3
'
'            End If
'
'            '----------Percent Change----------

'            'Change to Percent
'
'            'For j = 11 To 11
'
'            ws.Cells(i, j).Style = "Percentage"
'
'            'Next j
'


        Next CurrentRow
        Next
        MsgBox ("Done")
End Sub
