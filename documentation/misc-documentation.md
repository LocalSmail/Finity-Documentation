---
description: >-
  Here you will find Misc Functions that you can use that are not all that
  important to the main functionality of Finity.
---

# Misc Documentation

### Debugging

```etlua
finity:EnableDebugging(status) -- Status only excepts true or false
```

{% hint style="warning" %}
The status is a boolean value. This means it only accepts true or false, anything other than true or false will cause it to throw an error.
{% endhint %}

### Redownload Assets

```etlua
finity:RedownloadAssets() -- No checks for the downloaded and remaining assets for now.
```

### Create

```etlua
finity:Create(class, properties) -- Instance type, { Properties }
```

{% hint style="info" %}
Creates new instances. This is used to create and set properties of newly created instances. You can edit the properties of the instance's name by doing : { Name = "Name" }, Every other valid property of the instance will work inside this without needing to define the instances variable constantly.
{% endhint %}

### Importing Custom themes

{% code overflow="wrap" lineNumbers="true" %}
```lua
finity:ImportCustomThemes(Theme_Name) -- the name that the theme is called.
```
{% endcode %}

The theme name is taken/looked for from the custom themes lua file that can be found inside the FinityGUI folder in your workspace. You can download your own one using the function below.

### Downloading Custom themes/Assets

{% code overflow="wrap" lineNumbers="true" %}
```lua
finity:DownloadCustomAsset(link: string, AssetName: string, IsCustomThemeFile: boolean)
```
{% endcode %}

{% hint style="warning" %}
You can download custom themes but wont be able to replace images within the gui apart for using it to interact with roblox instances. The only way it can currently interact with the Gui is by downloading a Custom theme file. (_**WILL OVERWRITE EXISTING THEMES.**_)
{% endhint %}

### Change Background Image

{% code overflow="wrap" lineNumbers="true" %}
```lua
finity:ChangeBackgroundImage(ImageID, Transparnecy)
```
{% endcode %}

{% hint style="danger" %}
If the image ID is invalid (Not a roblox asset ID) then it may break, Adding custom image support soon.
{% endhint %}

