
# Treeko Theme

My theme for VS Code, which is a slightly customized version of Gruvbox Dark.


It looks like this:

![Treeko Theme Sample](sample/treeko-sample.png)


# Customization

If you dislike some of the choices made on this theme, you can change it by doing the following steps.

1. Open the **Command Palette (Ctrl + Shift + P)**

2. Search for **Developer: Inspect Editor Tokens and Scopes**

3. Put the cursor on top of the token whose highlighting you dislike and take note of the textmate scope of that token.

4. Search for **Preferences: Open User Settings (JSON)** on the **Command Palette (Ctrl + Shift + P)**

5. Add the customization section for the theme:

```JSON
{
  "editor.tokenColorCustomizations": {
    "[Treeko]": {
      "textMateRules": [
        {
          "name": "Some Name",
          "scope": [
            // Insert textmate scope here
            "storage.type.object.array.java" 
          ],
          "settings": {
            // Add the color you prefer
            "foreground": "#8EC07C"
          }
        }
        // Other customization rules here
      ]
    }
  }
}
```