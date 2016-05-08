# Introduction #

JQuery DataTables Column Filter enables you to add individual column filtering in the HTML tables enhanced with the DataTables plugin.
In this page you can find some examples of usage and configuration of the plugin.

# Details #

## Default behavior ##
The simplest case of usage of the column filter plugin is applying the column filter plugin without any additional configuration parameters. This example is shown in the following code:

```
 $("#tableId").dataTable().columnFilter();
```

This call will enhance a HTML table with id 'tableId' and add dataTable/column filtering functionalities.

## Customize column filters ##
To customize default behavior you can add configuration parameters to the columnFilter() call and customize filter for each column. Example is shown in the following code:
```
 $("#tableId").dataTable().columnFilter(
               {
                     aoColumns: [
                                    {
                                         type: "number"
                                    },
                                    {
                                         type: "text",
                                         bRegex: true,
                                         bSmart: true
                                    },
                                    null,
                                    {
                                         type: "select",
                                         values: [ 'A', 'B', 'C' ]
                                    },
                                    {
                                         type: "number-range"
                                    },
                                    {
                                         type: "date-range"
                                    }
                                 ]
               }
 );

```
If you pass aoColumn array with definition of the individual column filters you can customize behavior of the filters. The most important setting is type that can define how filtering will be done. Possible values are:
  * text - default behavior. You can define whether the regular expression or smart filtering will be used in the filtering,
  * number - filter numbers in the column,
  * select - put the select list that will be used for filtering. Values of the items in the list are placed in the values array,
  * null - do not add filter in the column,
  * number range - add two from-to filters to filter the number in the range,
  * date-range - add two from-to calendar to filter the dates in the range.