# EndRegion-
Local $testcol1dig = StringLen($testfilearray1[$testfilerownum2][$colnum])         EndIf         While $testcol1dig &lt; $col1maxdig             Local $neg1 = StringSplit($testfilearray1[$testfilerownum2][$colnum], "")             If $neg1[1] = "-" Then                 Local $neg1testfile = StringSplit($testfilearray1[$testfilerownum2][$colnum], "-")                 $testfilearray1[$testfilerownum2][$colnum] = "-0" &amp; $neg1testfile[2]                 Local $testcol1dig = StringLen($neg1testfile[2])             Else                 $testfilearray1[$testfilerownum2][$colnum] = "0" &amp; $testfilearray1[$testfilerownum2][$colnum]                 Local $testcol1dig = StringLen($testfilearray1[$testfilerownum2][$colnum])             EndIf             Local $neg1 = StringSplit($testfilearray1[$testfilerownum2][$colnum], "")             If $neg1[1] = "-" Then                 Local $neg1testfile = StringSplit($testfilearray1[$testfilerownum2][$colnum], "-")                 Local $testcol1dig = StringLen($neg1testfile[2])             Else                 Local $testcol1dig = StringLen($testfilearray1[$testfilerownum2][$colnum])             EndIf         WEnd     Next Next _ArrayDisplay($testfilearray1, "$testfilearray1") #EndRegion Add Pad  ;Now take the array and plug it into _ArrayMultiColSort($testfilearray1, $aSortData)
