1. Restore Database AnitaDB.bak to Sqlserver
2. Extract and run blazor-webassembly-basic-authentication-example-master. This is a sample taken from web and modified. I built authetication using JwtToken in a service in .Net Core at my prior role. That takes more time so I am taking a shortcut.
3. Extract AnitaGupta.zip for .NetCore 3.1 version OR AnitGuptaNet5.zip for .Net 5 version (they are identical except for package references). You would need Visual Studio 16.8 for .Net5
4. Search and replace connection string: optionsBuilder.UseSqlServer("Server=DESKTOP-GUFIHQA;Database=AnitaDB;Trusted_Connection=True;MultipleActiveResultSets=True");
Note that I have used separate Encryption/Decryption libraries in the past. 
5. In appsettings.json, set "Autheticate": "true" to go against authetication or "false" to bypass it.

Notes: 
1. There is a hole in this security, airtight authentication will take more time to build and this is just a sample.
2. In Adding new security, I have left out adding images. In prior sites I developed, I had numerous uploads. I need more time to add that functionality.
3. The DevExpress/DevExtreme grid gives similar functionality with paging etc. I initially started with that but it was more complex and would require more than 3-4 days to implement. I also experimented with PartialViews and Razor with PageModels.
