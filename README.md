# ngmd-dialogs
A shorter & flexible way to implement Material design dialogs within angular applications
One can utilize 3 forms of dialogs by importing `mdDialogProvider` service
 * Alert
 * Confirm
 * Custom

`mdDialogProvider` accepts two parameters object & type. Object parameter consist of `optionsOrPreset` properties of the dialog & the parameter type is used to define the form of a dialog which are alert, confirm and custom.
Detailed description of the `optionsOrPreset` properties can be seen [here](https://material.angularjs.org/HEAD/api/service/$mdDialog)

### Alert Dialog
```javascript
//open alert dialog
mdDialogProvider('alert').show(
    function(){
    //ok presses
    });
```
### Confirm dialog
```javascript 
mdDialogProvider('alert').show(
    function(){
    //ok presses
    }, function(){
    //dialog cancelled
    });
```
### Custom dialog
```javascript
mdDialogProvider({
    controller:function($scope){
        $scope.name="custom dialog";
    },
    template:'<div>{{name}}</div>'
    },'custom').show();
```
Install with bower `bower install --save ngmd-dialog`


