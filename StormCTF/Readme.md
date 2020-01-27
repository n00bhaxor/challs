StormCTF 2020 Shmoocon ticket contest: https://stormctf.ninja/shmoochal2020 writeup.

For now, just a Cyberchef recipe until I've got time to do a proper writeup. To use the recipe:

1) Upload the logo as input using the "Upload File as Input" icon on the top right.
2) Click the "Load Recipe" icon in the Recipe tab.
3) Paste the below recipe in the "Recipe" field, then click "Load."
4) Click Bake.

Here's the recipe:

[
  { "op": "Strings",
    "args": ["Single byte", 4, "Alphanumeric + punctuation (A)", false] },
  { "op": "Extract URLs",
    "args": [false] },
  { "op": "Find / Replace",
    "args": [{ "option": "Regex", "string": "pastebin.com/" }, "pastebin.com/raw/", true, false, true, false] },
  { "op": "HTTP request",
    "args": ["GET", "https://pastebin.com/raw/NnH1kAxC", "", "Cross-Origin Resource Sharing", false] },
  { "op": "From Base64",
    "args": ["A-Za-z0-9+/=", true] },
  { "op": "From Hex",
    "args": ["Auto"] },
  { "op": "Reverse",
    "args": ["Character"] },
  { "op": "From Base64",
    "args": ["A-Za-z0-9+/=", true] },
  { "op": "From Hex",
    "args": ["Auto"] },
  { "op": "From Base64",
    "args": ["A-Za-z0-9+/=", true] }
]
