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

<pre class="language-lua" data-overflow="wrap" data-line-numbers><code class="lang-lua"><strong>local FinityDev = loadstring(game:HttpGet("https://raw.githubusercontent.com/LocalSmail/Finity/Development/Library"))()
</strong><strong>
</strong><strong>-- Development version of finity. May be unstable, Not work with docs, Be outdated/behind the main branch, etc. Join the discord for updates: https://discord.gg/CenXcThBFv
</strong><strong>-- Check the github: https://github.com/LocalSmail/Finity
</strong></code></pre>

Use the above line of code before you run any of Project Finity's UI methods.

{% hint style="info" %}
You can change the name from 'Finity' to whatever you want, But if your new and do not understand how to use Finity I recommend you stick with the current name.
{% endhint %}

### Finity Modules

### Toast Messages

```lua
finity:ToastMessage()
```

{% tabs %}
{% tab title="Properties" %}


<table><thead><tr><th>Properties</th><th>Default Value</th><th data-hidden></th></tr></thead><tbody><tr><td>TopText</td><td>nil</td><td></td></tr><tr><td>BottomTextBottomText</td><td>nil</td><td></td></tr><tr><td>Time</td><td>nil</td><td></td></tr><tr><td>Alert_Type</td><td>Info</td><td></td></tr><tr><td>CustomBackgroundIcon</td><td>nil</td><td></td></tr></tbody></table>

<table><thead><tr><th>Alert Types</th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td>Info</td><td></td><td></td></tr><tr><td>Warning</td><td></td><td></td></tr><tr><td>Success</td><td></td><td></td></tr></tbody></table>

{% hint style="info" %}
Each Alert type has its own colour tied to it, Warning will be a Yellow-Orange, Info a sort of White and Success Green
{% endhint %}
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


<table><thead><tr><th>Properties</th><th>Default Value</th><th data-hidden></th></tr></thead><tbody><tr><td>Title</td><td>nil</td><td></td></tr><tr><td>isdark</td><td>false</td><td></td></tr><tr><td>CustomTheme</td><td>nil</td><td></td></tr><tr><td>CustomThemeName</td><td>nil</td><td></td></tr><tr><td>HideToolTip</td><td>false</td><td></td></tr><tr><td>ToolTip</td><td>nil</td><td></td></tr><tr><td>ChangeToggleKey()</td><td>Home</td><td></td></tr></tbody></table>

{% hint style="warning" %}
The ChangeToggleKey() Doesn't fit inside the new() function, Define the window and then use the ChangeToggleKey() like this:&#x20;

`FinityWindow:`ChangeToggleKey(`"Home")`&#x20;

When adding a new key please define the button name: Home, Insert etc

[https://developer.roblox.com/en-us/api-reference/enum/KeyCode](https://developer.roblox.com/en-us/api-reference/enum/KeyCode)
{% endhint %}

{% hint style="info" %}
Although you hide the Tool Tip you might still need to add a string, It doesn't have to contain anything. It could be just `""`.&#x20;
{% endhint %}

{% hint style="info" %}
When using a custom theme. Make sure the Custom Theme is inside the `CustomTheme.lua` file when defining it from the list and that the name given is matching.
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
| <p>FinityWindow:ChangeToggleKey(<strong>Enum</strong> keycode)<br></p> | Changes the Toggle Key to the `Enum.Keycode` Set           | nil             |

{% hint style="info" %}
The default toggle key is the `Home` key.
{% endhint %}
{% endtab %}
{% endtabs %}

### Sectors

<pre class="language-lua" data-overflow="wrap"><code class="lang-lua"><strong>local FinitySector = FinityCategory:Sector()
</strong></code></pre>

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

<table><thead><tr><th>Cheat Module Type</th><th>Description</th><th>Data Types</th><th data-hidden></th></tr></thead><tbody><tr><td>Checkbox</td><td>The checkbox is useful for having a user control the state of something. Fires callback with the new state of the checkbox.</td><td>       <strong>NO DATA TYPES</strong></td><td></td></tr><tr><td>Dropdown</td><td>The dropdown is useful for having a user choose from a list of things. Fires the callback with the option that was chosen as a string.</td><td>default (String)<br>options (table) {} &#x3C;table</td><td></td></tr><tr><td>Slider</td><td>The slider is useful for having a user choose between a range of numbers. Fires the callback with the new value of the slider.</td><td>default (String)<br>min/max (int)<br>suffix (String)</td><td></td></tr><tr><td>Textbox</td><td>The textbox is useful for having the user enter a custom value. Fires the callback with the new value of the textbox as a string.</td><td>placeholder (String)</td><td></td></tr><tr><td>Button</td><td>The button is nice for a user to trigger a specific action. Fires the callback when clicked with no arguments.</td><td>       <strong>NO DATA TYPES</strong></td><td></td></tr><tr><td>Keybind</td><td>The keybind is useful for performing an action when a key is pressed. Fires the callback when the key is changed or pressed.</td><td>default (String)<br><br><strong>Just click it and press a key.</strong><br><strong>Click backspace to remove the chosen key and try again before submiting.</strong></td><td></td></tr><tr><td>Colorpicker</td><td>This is nice for choosing a certain color in range. Fires the callback each time the color is changed with the new Color3.</td><td>       <strong>NO DATA TYPES</strong></td><td></td></tr><tr><td>Label</td><td>The label is useful for displaying information to a user. Doesn't fire anything.</td><td>       <strong>NO DATA TYPES</strong></td><td></td></tr></tbody></table>

### Debugging

```lua
finity.EnableDebugging(status) -- Status only excepts true or false
```

{% hint style="warning" %}
The status is a boolean value. This means it only accepts true or false, anything other than true or false will cause it to throw an error.
{% endhint %}

## You have reached the end!

{% hint style="info" %}
Have ago at making your own GUI! If you have any suggestion then please let me know by submitting an suggesting in the discord!
{% endhint %}
