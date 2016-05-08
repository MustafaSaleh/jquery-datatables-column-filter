# Introduction #
## JQuery DataTable plugin ##
[JQuery DataTables](http://www.datatables.net) plugin is an excellent client-side plugin that enhances client-side HTML table and adds various functionalities such as pagination, filtering, ordering etc.
It also has good API that allows you to customize plugin e.g to add individual column filtering in the headers or footers. Some of the functionalities you migh need comes out of box and can be directly configured in the datatables initialization function, but for some of the other functionalities you need to manually implement using the example on the site.

## JQuery DataTables Column Filtering plugin ##
Column filtering functionality is one of the functionalities that you will need to implement using the custom examples on the DataTables site. As an alternative you can use the [DataTables Column filter](http://jquery-datatables-column-filter.googlecode.com/svn/trunk/index.html) plugin where most of the code exmaples from the DataTables site are encapsulated.

# Implementation #
To implement and customize column filtering you will ned to take DataTables plugin and column filtering plugin and enhance your HTML table with basic !dataTable plugin and then with columnFilter plugin as shown in the example:

```
$("#dataTableId").dataTable().columnFilter();
```

You can find documentation about ColumnFilter plugin on the wiki pages, and some [live examples](http://jquery-datatables-column-filter.googlecode.com/svn/trunk/default.html). Also you can take an offline version in the [example archive](http://code.google.com/p/jquery-datatables-column-filter/downloads/detail?name=JQuery-DataTables-ColumnFilter.zip)