StormCTF 2020 Shmoocon ticket contest: https://stormctf.ninja/shmoochal2020 writeup.

For now, just a Cyberchef recipe until I've got time to do a proper writeup. To use the recipe:

1) Upload the logo as input using the "Upload File as Input" icon on the top right.
2) Click the "Load Recipe" icon in the Recipe tab.
3) Paste the below recipe in the "Recipe" field, then click "Load."
4) Click Bake.

Here's the recipe:

Strings('Single byte',4,'Alphanumeric + punctuation (A)',false)
Extract_URLs(false)
Find_/_Replace({'option':'Regex','string':'pastebin.com/'},'pastebin.com/raw/',true,false,true,false)
HTTP_request('GET','https://pastebin.com/raw/NnH1kAxC','','Cross-Origin Resource Sharing',false)
From_Base64('A-Za-z0-9+/=',true)
From_Hex('Auto')
Reverse('Character')
From_Base64('A-Za-z0-9+/=',true)
From_Hex('Auto')
From_Base64('A-Za-z0-9+/=',true)
