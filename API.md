# Basic Usage
> toast is a UI that can be used as an alternative means of window.alert, window.confirm and window.prompt

## setConfig()
`setConfig([options])`
You define the default settings for the toast. Create a ax5.ui.toast instance, using the setConfig method in that instance, you can define a default value.
 
```js
var myToast = new ax5.ui.toast();
myToast.set_config({
    msg: "String",
    theme: "String",
    width: "Number", 
    icon: "String",
    closeIcon: "String",
    onStateChanged: "Function",
    displayTime: "Number",
    animateTime: "Number",
    containerPosition: "String",
    lang: "Object"
});
```


### msg

Type: `String`  

Title of toast.


### theme

Type: `String`  [default: default]

Theme of toast, ax5modal themes using six colors defined by the bootstrap is provided.


### width

Type: `Number` [default: 300]

Toast width


### icon

Type: `String`


### closeIcon

Type: `String`


### onStateChanged

Type: `Function`  

onStateChanged function is executed when the toast of the state is changed,
this.state state value is passed to this time onStateChanged function.


### displayTime

Type: `Number` [default : 3000]



### animateTime

Type: `Number` [default : 300]



### containerPosition

Type: `String` [top-left|top-right|bottom-left|bottom-right]



### lang

Type: `Object`

```js
myToast.setConfig({
    lang: {
        "ok": "확인"
    }
});
```


- - -

## push()
`push(String|Options[, callBack])`

If this is String in the first argument and recognizes the first argument to `msg`.  
it is possible to redefine all of the options that can be used in setConfig.  

```js
toast.push('Toast message', function () {
    console.log(this);
});

toast.push({
    theme: 'danger',
    msg:'Toast message'
}, function () {
    console.log(this);
});
```

- - -

## confirm()
`confirm(String|Options[, callBack])`

```js
confirmToast.confirm({
    msg: 'Confirm message'
}, function(){

});
```

## close()
`close()`