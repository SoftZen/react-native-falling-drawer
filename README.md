# react-native-falling-drawer
Customizable falling drawer for React Native

[![NPM](https://nodei.co/npm/react-native-falling-drawer.png)](https://www.npmjs.com/package/react-native-falling-drawer)

<img src="https://raw.githubusercontent.com/SoftZen/react-native-falling-drawer/master/Example/falling_drawer.gif" alt="example drawer" width="400"/>

Installation
---
```javascript
$ npm install react-native-falling-drawer --save
```
then
```javascript
import React, { Component } from 'react';
import {
  Text,
} from 'react-native'
import FallingDrawer from 'react-native-falling-drawer'

const SCREENS = [
  {
    key: "profile",
    name: "Profile",
    color: "red",
    titleColor: "#fff",
    hamburgerColor: "#fff",
    render: () => <View><Text>This is profile screen</Text></View>
  }
]

  render() {
    return (
        <FallingDrawer screens={SCREENS}/>
    );
  }
}

```
Refer to the Example


## Available props:

| prop | type | description |default|
| ------ | ------ | ------ | ------ |
|screens|array|An array of sceens to switch between||
|headerHeight | number |Height of the header|ios: 60, android: 50|
|shakeDuration|number|Shake effect duration in ms|800|
|optionCollapseSpeed|number|Collapse speed of the options in ms|150|
|optionCollapseDelay|number|Delay between each option animation in ms|200|
|diversifyAnimations|boolean|If true, it applies bounce, shake and swing animations to the options, otherwise only shake|true|

### screens:
Each screen in the screens array is an object which looks like this:

```
{
    key: "profile",            // unique key among all screens
    name: "Profile",           // header and option title 
    color: "red",              // header and option color
    titleColor: "#fff", 
    hamburgerColor: "#fff",
    render: () => {...}        // specifies how the screen is rendered
    customHeader: () => {...}  // custom header and option
}
```

License
----

MIT
