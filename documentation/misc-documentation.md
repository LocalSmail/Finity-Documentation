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
