# Process
## Template
```md
{  
// Make changes here to the cmd.exe profile.  
"guid": "{799fa555-861d-4a1e-ac05-f44dfe39bdb6}",  
"name": "Anaconda",  
"commandline": "cmd.exe /K C:\\ProgramData\\Anaconda3\\Scripts\\activate.bat",  
"hidden": false,  
"icon": "C:\\ProgramData\\Anaconda3\\Menu\\anaconda-navigator.ico",  
"startingDirectory": "%USERPROFILE%"  
}
```

>[!tip]
>**To find the guid of the terminal you can generate a new with**
>
>`[guid]::NewGuid()`

## Steps
- Right click on the terminal
- Open up the terminal file location
- Right click, select properties
- Place the target in the commandline info and the start in the startingDirectory
	- It might be necessary to put double \\ in the file location instead of the single \. 

![[Pasted image 20220616205247.png]]

- Add the icon by selecting the 'Change Icon' button and copying the file path.