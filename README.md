material-design-icons
=====================

SVG iconsets to be used with Angular-Material in this fashion:

md-icon directive:

```html
<div ng-app="appDemoSvgIcons" ng-controller="DemoCtrl" ng-cloak layout="column" layout-margin >
    <p>The simplest way to display a single SVG icon is by referencing it by URL:</p>
    <p>
        <md-icon md-svg-src="{{ insertDriveIconURL }}"
                 alt="Insert Drive Icon">
        </md-icon>
    </p>
    <p>Style the icon size and color with CSS:</p>
    <p>
      <md-icon md-svg-src="img/icons/cake.svg"            class="s24" alt="Cake"    ></md-icon>
      <md-icon md-svg-src="{{ getAndroid() }}"            class="s36" alt="Android "></md-icon>
      <md-icon md-svg-src="img/icons/addShoppingCart.svg" class="s48" alt="Cart"    ></md-icon>
    </p>
</div>
```

Angular config:
```javascript
angular.module('appDemoSvgIcons', ['ngMaterial'])
.controller('DemoCtrl', function( $scope ) {
    $scope.insertDriveIconURL = 'img/icons/ic_insert_drive_file_24px.svg';
    $scope.getAndroid = function() {
      return 'img/icons/android.svg';
    }
});
```
