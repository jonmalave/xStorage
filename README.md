# xStorage

> Browser Storage Plugin for Nuxt.js

## Install
Copy `module/xStorage.js` to project's `/modules` folder and `plugin/xStorage.js` to `/plugins` folder. 

Add the file path `~/plugins/xStorage.js` inside the plugins key of `nuxt.config.js`

## Use

#### Init
Add the following in a `mounted()` hook to initialize xStorage

``` bash
const storage = this.$xStorage.init('xStorage');
if (storage !== null) { 
  // your code here
}
```

#### Update
Specify the xStorage properties and values you would like to add or update. 

``` bash
this.$xStorage.update({ 
  key: 'xStorage', 
  value: { 
    name: 'Jon Doe',
    age: 37,
    profession: 'developer'
  }
});  
```

#### Delete
Call `this.$xStorage.delete();` to delete the xStorage object


## FYI 
xStorage uses a single object to store browser session data persistently via localStorage. When updating a single property you must define any previously added properties and values in each update to prevent data loss.


For detailed explanation on how Nuxt.js plugins work, checkout [Nuxt.js docs](https://nuxtjs.org/guide/plugins#codefund_ad).
