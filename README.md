# tm.pagination
angular分页插件tm.pagination（解决触发二次请求的问题）<br/>
根据条件查询<br/>
需要重新定义一个方法<br/>  
```javascript
$scope.so = function () {
            if ($scope.paginationConf.currentPage != 1) 
                $scope.paginationConf.currentPage = 1; 
            }else{
                $scope.poat();
            }
}  
```
原因：解决了二次请求的问题，但是回归第一页需要重新赋值为1才行  
* currentPage:当前页面数,默认为1
* totalItems:总数
* itemsPerPage:显示数量
* onChange:事件
* pagesLength:分页大小数量,默认9



