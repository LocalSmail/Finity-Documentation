---
description: >-
  Here you can find the basics on how part of the Library works and how to
  interact with them.
---

# Documentation

## Project Finity Library

Project Finity has a variety of different modules for you to customize your cheat. Below is the documentation on how to use each of them.\


{% hint style="danger" %}
WIP || Work in progress, Haven't added most things yet.
{% endhint %}

## Importation

You can add the library to your exploit by doing the following:

{% code overflow="wrap" lineNumbers="true" %}
```lua
local Finity = loadstring(game:HttpGet("https://raw.githubusercontent.com/LocalSmail/Finity/main/Library"))()
```
{% endcode %}

Use the above line of code before you run any of Project Finity's UI methods.

{% hint style="info" %}
You can change the name from 'Finity' to whatever you want, But if your new and do not understand how to use Finity I recommend you stick with the current name.
{% endhint %}

### Finity Modules

### Toast Messages

```lua
finity.ToastMessage() -- Currently not much functionality
```

{% hint style="warning" %}
This is currently a base for now, I may add more to it in the future if it is received well.
{% endhint %}

{% tabs %}
{% tab title="Properties" %}


| Properties | Default Value |   |
| ---------- | ------------- | - |
| Header     | nil           |   |
| Content    | nil           |   |
| Time       | nil           |   |
{% endtab %}
{% endtabs %}

### Windows

{% code overflow="wrap" lineNumbers="true" %}
```lua
local FinityWindow = Finity.new()
```
{% endcode %}

{% hint style="info" %}
You can Parse an Boolean Value to Enable or Disable Dark Mode for the GUI.
{% endhint %}

A Finity Window is what stores all the rest of your content within your GUI.

{% tabs %}
{% tab title="Properties" %}


| Properties                       | Default Value |   |
| -------------------------------- | ------------- | - |
| Title                            | nil           |   |
| isdark                           | false         |   |
| CustomTheme (Barely any func rn) | nil           |   |
| HideToolTip                      | false         |   |
| ToolTip                          | nil           |   |
| ChangeToggleKey()                | Home          |   |

{% hint style="warning" %}
The ChangeToggleKey() Doesn't fit inside the new() function, Define the window and then use the ChangeToggleKey() like this:&#x20;

`FinityWindow.ChangeToggleWindow(Home)`&#x20;

When adding a new key please define the button name: Home, Insert etc

[https://developer.roblox.com/en-us/api-reference/enum/KeyCode](https://developer.roblox.com/en-us/api-reference/enum/KeyCode)
{% endhint %}

{% hint style="info" %}
Although you hide the Tool Tip you might still need to add a string, It doesn't have to contain anything. It could be just `""`.&#x20;
{% endhint %}
{% endtab %}
{% endtabs %}

### Change Background Image

```lua
finity.ChangeBackgroundImage()
```

{% tabs %}
{% tab title="Properties" %}
| Properties   | Default Value |
| ------------ | ------------- |
| ImageID      | nil           |
| Transparency | 0             |

{% hint style="danger" %}
If the image ID is invalid (Not a roblox asset ID) then it may break.
{% endhint %}


{% endtab %}
{% endtabs %}

### Categories

A Category can be made by doing the following:\


```lua
local FinityCategory = FinityWindow:Category()
```

{% hint style="info" %}
You can parse an String Value to give the Category an Name to help users distinguish between each Category.
{% endhint %}

{% tabs %}
{% tab title="Methods" %}
| Method                                                                 | Description                                                | Returns         |
| ---------------------------------------------------------------------- | ---------------------------------------------------------- | --------------- |
| FinityWindow:Category(string name)                                     | Creates an Category, Can parse an string to give it a name | Finity Category |
| <p>FinityWindow.ChangeToggleKey(<strong>Enum</strong> keycode)<br></p> | Changes the Toggle Key to the `Enum.Keycode` Set           | nil             |

{% hint style="info" %}
The default toggle key is the `Home` key.
{% endhint %}
{% endtab %}
{% endtabs %}

### Sectors

<pre class="language-lua" data-overflow="wrap"><code class="lang-lua"><strong>local FinitySector = FinityCategory:Sector()</strong></code></pre>

{% hint style="info" %}
You can Parse an String Value to give the Sector an name to to help users distinguish between each Sector.
{% endhint %}

A Finity Sector instance is essentially a mini-category, allowing for even more categorization. You could say these are like tabs.

For example, it would allow you to sub-categorize a "Visuals" category into things like "Player Visuals," "Zombie Visuals," and "Item Visuals."

Below are the methods associated with a Finity Sector.

{% tabs %}
{% tab title="Methods" %}


| Method                                                                                                                                                        | Description                                                                            | Returns      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | ------------ |
| <p>FinitySector:Cheat(<strong>string</strong> type, <strong>string</strong> name [, <strong>function</strong> callback, <strong>array</strong> data])<br></p> | Creates a new FinityCheat with a type and a name. (Optional: callback function & data) | Finity Cheat |
{% endtab %}

{% tab title="Properties" %}


| Property | Description       | Returns |
| -------- | ----------------- | ------- |
| name     | The Sectors name. | nil     |
|          |                   |         |
|          |                   |         |
{% endtab %}
{% endtabs %}

### Cheat

{% code overflow="wrap" lineNumbers="true" %}
```lua
local FinityCheat = FinitySector:Cheat("type", "name", function (NewValue)
    print(NewValue)
end, {})
```
{% endcode %}

A Finity Cheat is a cheat modules useful for hooking Call Backs to Toggles in order to have a smooth and organized script.

There are many different types of Cheat Modules. Here's a table to compare them all:

| Cheat Module Type | Description                                                                                                                            |   |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------- | - |
| Checkbox          | The checkbox is useful for having a user control the state of something. Fires callback with the new state of the checkbox.            |   |
| Dropdown          | The dropdown is useful for having a user choose from a list of things. Fires the callback with the option that was chosen as a string. |   |
| Slider            | The slider is useful for having a user choose between a range of numbers. Fires the callback with the new value of the slider.         |   |
| Textbox           | The textbox is useful for having the user enter a custom value. Fires the callback with the new value of the textbox as a string.      |   |
| Button            | The button is nice for a user to trigger a specific action. Fires the callback when clicked with no arguments.                         |   |
| Keybind           | The keybind is useful for performing an action when a key is pressed. Fires the callback when the key is changed or pressed.           |   |
| Colorpicker       | This is nice for choosing a certain color in range. Fires the callback each time the color is changed with the new Color3.             |   |
| Label             | The label is useful for displaying information to a user. Doesn't fire anything.                                                       |   |

## You have reached the end!

{% hint style="info" %}
Have ago at making your own GUI! If you have any suggestion then please let me know by submitting an suggesting in the discord!
{% endhint %}
