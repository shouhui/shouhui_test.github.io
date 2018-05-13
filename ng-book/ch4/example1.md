# 控制器

## 控制器在angular是一个函数，我们可以通过控制器初始化作用于$scope的值，以及定义页面时间的行为函数

example1:
```
<!DOCTYPE html>
<html ng-app="myApp">
<head>
    <title>first angular controller</title>
    <script src="../angular.min.js"></script>
</head>

<body>
    <div ng-controller="myController">
        <button ng-click="add(1)" >Add</button>
        <a ng-click="subtract(1)">Sunbract</a>
        <h4>Current count: {{counter}}</h4>
    </div>
    <script>
        var app = angular.module("myApp", []);
        app.controller("myController", function ($scope) {
            $scope.counter = 0;
            $scope.add = function (amount) {
                $scope.counter += amount;
            };
            $scope.subtract = function (amount) {
                $scope.counter -= amount;
            }
        });
    </script>
</body>
</html>
```
