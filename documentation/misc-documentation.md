---
description: >-
  Here you will find Misc Functions that you can use that are not all that
  important to the main functionality of Finity.
---

# Misc Documentation

### ChangeToggleKey

```lua
local Finity = loadstring(game:HttpGet("https://raw.githubusercontent.com/LocalSmail/Finity/main/Library"))()
-- runs the finity gui

local FinityWindow = Finity.new()
-- creates a new window

FinityWindow:ChangeToggleKey("Semicolon")
-- changes the toggle key to: ; instead of the home key.
```

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
finity:ImportCustomThemes("theme name") -- the name that the theme is called.
```
{% endcode %}

The theme name is taken/looked for from the custom themes lua file that can be found inside the FinityGUI folder in your workspace. You can download your own one using the function below.

### Downloading Custom themes/Assets

{% code overflow="wrap" lineNumbers="true" %}
```lua
finity:DownloadCustomAsset("link", "AssetName", IsCustomThemeFile: boolean)
```
{% endcode %}

{% hint style="warning" %}
You can download custom themes but wont be able to replace images within the gui apart for using it to interact with roblox instances. The only way it can currently interact with the Gui is by downloading a Custom theme file. (_**WILL OVERWRITE EXISTING THEMES.**_)
{% endhint %}

### Change Background Image

{% code overflow="wrap" lineNumbers="true" %}
```lua
finity:ChangeBackgroundImage("ImageID/Path", Transparnecy: number)
```
{% endcode %}

{% hint style="warning" %}
If the image you want to use is an roblox asset, Input the ID only (Thats all the function needs.). It will throw an error otherwise by default.
{% endhint %}

### ThinProject

{% code overflow="wrap" lineNumbers="true" %}
```lua
self2:EnableThinProject(Enable) -- true/false boolean.
```
{% endcode %}

This will allow you to use an legacy part of the Finity design which is the ThinProject setting. This like its name, will make your project "thinner".

{% hint style="warning" %}
This, Like toast notifications are finity window functions and can be used after making a gui.
{% endhint %}

### Post/Get Requests

{% code overflow="wrap" lineNumbers="true" %}
```lua
finity:requestfunc({data}) -- Data will be used to send data and get returned data. It is a table so you will need to make a table then parse the needed arguments to use it. Refer to our Example's for a demo: https://github.com/LocalSmail/Finity/tree/main/Examples
```
{% endcode %}

{% tabs %}
{% tab title="Properties" %}
| Property   | Description                                         | Default Value |
| ---------- | --------------------------------------------------- | ------------- |
| Url        | The url which will be interacted with.              | None          |
| Method     | The method we will use. (Can only use POST or GET)  | None          |
| Body       | The data returned after sending the request.        | None          |
| Headers    | The Headers returned after sending the request.     | None          |
| StatusCode | The Status Code returned after sending the request. | None          |
{% endtab %}
{% endtabs %}

### Hub Mode

{% code overflow="wrap" lineNumbers="true" %}
```lua
finity:EnableHubMode(Enable) -- Boolean
```
{% endcode %}

Hub mode allows for the developer of a hub to remove the potentially annoying credits print that finity prints by default. It gives them the option to hide it or show it.

{% hint style="warning" %}
If the value parsed is not a boolean type value it will send the credits by default and will print an error message.
{% endhint %}

