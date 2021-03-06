# NativeScript Material Button

Material Design's [Button](https://material.io/components/buttons) component for NativeScript.

[![npm](https://img.shields.io/npm/v/@nativescript-community/ui-material-button.svg)](https://www.npmjs.com/package/@nativescript-community/ui-material-button)
[![npm](https://img.shields.io/npm/dt/@nativescript-community/ui-material-button.svg?label=npm%20downloads)](https://www.npmjs.com/package/@nativescript-community/ui-material-button)

## Contents

1. [Installation](#installation)
2. [Changelog](#changelog)
3. [FAQ](#faq)
4.  [Usage](#usage)
    - [Plain NativeScript](#plain-nativescript)
    - [Angular](#nativescript--angular)
    - [Vue](#nativescript--vue)
5.  [API](#api)

## Installation

### :warning: Warning :warning:
From NativeScript 5.x using this component will break the [NativeScript tab component](https://docs.nativescript.org/ui/components/tabs) on iOS (which is bound to be removed). This is needed to allow using the latest native iOS features. If needed you can use either [bottomnavigationbar](https://www.npmjs.com/package/@nativescript-community/ui-material-bottomnavigationbar) (this one is the best choice, closest to material design) or [material-tabs](https://www.npmjs.com/package/@nativescript-community/ui-material-tabs) (clone of the NativeScript one, but with a little less features).

##

For NativeScript 7.0+
* `tns plugin add @nativescript-community/ui-material-button`

##

For NativeScript 6.x
* `tns plugin add nativescript-material-button`

##

If using ```tns-core-modules```
* `tns plugin add nativescript-material-button@2.5.4`

##

Be sure to run a new build after adding plugins to avoid any issues.

## [Changelog](./CHANGELOG.md)

## [FAQ](../../README.md#faq)

## Usage

### Plain NativeScript

<span style="color:red">IMPORTANT: </span>_Make sure you include `xmlns:mdb="@nativescript-community/ui-material-button"` on the Page element_

#### XML

```XML
<Page xmlns:mdb="@nativescript-community/ui-material-button">
    <StackLayout horizontalAlignment="center">
        <mdb:Button text="raised button"/>
        <mdb:Button variant="flat" text="flat button"/>
        <mdb:Button variant="text" text="text button"/>
        <mdb:Button elevation="5" rippleColor="red" text="raised custom button"/>
   </StackLayout>
</Page>
```

#### CSS

```CSS
mdbutton {
    ripple-color: blue;
    elevation: 4;
}
```

##

### NativeScript + Angular

```typescript
import { NativeScriptMaterialButtonModule } from "@nativescript-community/ui-material-button/angular";

@NgModule({
    imports: [
        NativeScriptMaterialButtonModule,
        ...
    ],
    ...
})
```

```html
<MDButton rippleColor="blue" text="text button"></MDButton>
```

##

### NativeScript + Vue

```javascript
import Vue from 'nativescript-vue';
import ButtonPlugin from '@nativescript-community/ui-material-button/vue';

Vue.use(ButtonPlugin);
```

```html
<MDButton rippleColor="blue" text="text button"/>
```

## API

### Attributes

Inherite from NativeScript [Button](https://docs.nativescript.org/ui/ns-ui-widgets/button) so it already has all the same attributes.

* **elevation** _optional_

An attribute to set the elevation of the button. This will increase the 'drop-shadow' of the button.

* **variant** _optional_

An attribute to set the variant of the button. Can be ```flat``` or ```text```. No value means raised button

* **rippleColor** _optional_

An attribute to set the ripple color of the button.
