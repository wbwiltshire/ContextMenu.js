## ContextMenu.js provides a basic context menu control to a webpage using javascript and Bootstrap.
---

A simple javascript library which provides a basic context menu using javascript and Bootstrap

For more informaton:
* [Bootstrap](https://getbootstrap.com/)
* [Building a custom right-click context menu with javascript](https://www.sitepoint.com/building-custom-right-click-context-menu-javascript/)

### Usage
1. CSS changes
  * Add CCS links for ContextMenu, FontAwesome, and Bootstrap
```css
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootswatch/3.3.7/slate/bootstrap.min.css" type="text/css" />
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" type="text/css" />		
<link rel="stylesheet" type="text/css" href="/stylesheets/contexmenu.css" />
```
1. HTML5 <b>table row</b> changes for the unique id
```html
<div class="row">
    <div class="col-md-12">
        <table id="CustomerTable" class=”table table-striped tabled-bordered table-condensed table-hover”>
			<thead>
				<tr>
					<th>Id</th>
                    <th>First Name</th>
                    <th>Last Name</th>
                    <th>EMail</th>
				</tr>
			</thead>
			<tbody>
				<tr id='1' class='contextMenu-target'>
					<td >1</td>
                    <td>Daffy</td>
                    <td>Duck</td>
                    <td>DaffyD@Disney.com</td>
				</tr>
            </tbody>
	    </table>
    </div>
</div>
```
1. HTML5 add a <b>context menu</b> to the body right after the table
```html
<nav id="context-menu" class="contextMenu">
	<ul class="contextMenu-items">
		<li class="contextMenu-item">
			<a href=" Display/" class="contextMenu-action" data-action="Display">
				<i class="fa fa-file-text-o"></i> Display</a>
		</li>
		<li class="contextMenu-item">
			<a href="Edit/" class="contextMenu-action" data-action="Edit">
				<i class="fa fa-edit"></i> Edit</a>
		</li>
		<li class="contextMenu-item">
			<a href="Delete/" class="contextMenu-action" data-action="Delete">
				<i class="fa fa-trash"></i> Delete</a>
		</li>
	</ul>
</nav>
```
1. Javascript changes
  * Instantiation
```js
var contexmenu = new ContextMenu(); 
```
1. Add ContextMenu.js to page scripts
```js
<script src="/javascripts/contexmenu.js" type="text/javascript"></script>
```

### FAQ

1. How do I get the context menu to disappear again?
  * Right or left click anywhere outside the table body, including the table header
1. Can I still use the default document context menu?
  * Yes, just right click outside the table body