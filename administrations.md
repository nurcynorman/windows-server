icacls TestFile.txt /grant User1:F #grant User1 full control over a file named TestFile.txt
icacls RestrictedData /deny GuestUser:R #you want to deny GuestUser read access to a folder called RestrictedData.
icacls ProjectFolder /remove OldUser /t /c #remove all permission for OldUser from ProjectFolder
icacls c:Data\* /save DataACLBackup.txt /t #make changes to permissions in C:\Data and want to bacak them up first
icacls C:\Data /restore DataACLBackup.txt # restore ACL from backup
icacls C:\Reports /setowner AdminUser /t /c #change ownership of a file
icacls C:\Project /findsid S-1-5-21-1234567890-13456789-123456789-1001 /t #finding file with specidied SID in ACL
icacls "C:\SharedDocs\ProblemFolder" /reset /t /c # resetting persmission to default inherited values
icacls SecureDoc.docx /setintegritylevel h #set ingerity levels to high
icacls C:\OldData /substitute S-1-5-21-OLD-SID S-1-5-21-NEW-SID #replace one SID with another
icacls C:\Inbox /verify /t #verify ACL Consistency
icacls TestFile.txt /grant User1:(D,WDAC) # Getting advanced permissioons
