---
description: >-
  Here you will find Misc Functions that you can use that are not all that
  important to the main functionality of Finity.
---

# Misc Documentation

### ChangeToggleKey

```lua
FinityWindow:ChangeToggleKey(KeyCdoe)
```

{% hint style="warning" %}
The KeyCodes are the names of the keys that are on your keyboard, If they are not typed correctly then it will still be applied but will not work. E.g:

ChangeToggleKey("e") -- This will set it to the letter e but it will not work when you press E as it is not typed correctly. Capitalise the e letter and it will work
{% endhint %}

{% hint style="info" %}
Dont know what keycodes there are and the names for each one? Heres roblox's official documentation: [https://create.roblox.com/docs/reference/engine/enums/KeyCode](https://create.roblox.com/docs/reference/engine/enums/KeyCode)

KeyCode names are what is at the end of: `Enum.KeyCode. The keycode name is accepted as an acceptable toggle but only when entered correctly (View the warn above for more understanding). You can enter the entire Enum.KeyCode.Keyname as it will strip the input of:` Enum.KeyCode. `Just make sure the key name is correct.`
{% endhint %}

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

### Thin Project

{% code overflow="wrap" lineNumbers="true" %}
```lua
self2:EnableThinProject(Enable) -- true/false boolean.
```
{% endcode %}

This will allow you to use an legacy part of the Finity design which is the ThinProject setting. This like its name, will make your project "thinner".

{% hint style="warning" %}
This, Like toast notifications are finity window functions and can be used after making a gui.
{% endhint %}

### Hub Mode

{% code overflow="wrap" lineNumbers="true" %}
```lua
finity:EnableHubMode(Enable) -- Boolean
```
{% endcode %}

Hub mode allows for the developer of a hub to remove the potentially annoying credits print that Finity prints by default. It gives them the option to hide it or show it.

{% hint style="warning" %}
If the value parsed is not a Boolean type value it will send the credits by default and will print an error message.
{% endhint %}

