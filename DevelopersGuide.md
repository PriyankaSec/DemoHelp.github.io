Use the following steps to add the client widget to a brower page.
Add the JavaScript for the page. The following code is a general example.  Colorized Example Code 
```html
<!DOCTYPE html>
 <html>
 <head>
     <title>Spread HTML test page</title>
```
Add the SpreadJS scripts. Spread provides minified and debug versions of the scripts. The gcspread.sheets.all.xxxx.min.js supports all the functions of Spread. The gcspread.sheets.xxxx.min.js supports the core features of Spread. The gcspread.sheets.functions.xxxx.min is a minimized js file for extension functions. 
```Javascript
<script src="[Your_Scripts_Path]/gcspread.sheets.all.xxxx.min.js" type="text/javascript"></script>
```
Add the CSS files to change the appearance. Use the gcspread.sheets.xxxx.css file for a default appearance (effects the style of the scroll bar, the style of the filter dialog and child elements, cells, and tab strip). 
```Javascript
//<link href="[Your_CSS_Path]/gcspread.sheets.xxxx.css" rel="stylesheet" type="text/css"/>
//OR
<link href="[Your_CSS_Path]/bootstrap/bootstrap.min.css" rel="stylesheet" type="text/css"/>
<link href="[Your_CSS_Path]/bootstrap/bootstrap-theme.min.css" rel="stylesheet" type="text/css"/>
```
Implement the initialization and any other code. This example initializes the SpreadJS widget in a DOM element with an id of 'spreadContainer'.  Colorized Example Code 
```JavaScript 
    <script type="text/javascript">
         //<![CDATA[
         $(document).ready(function () {
             //Create a spread instance on DIV element which id is 'spreadContainer'
            // Obtain spread instance
             var spread = new GcSpread.Sheets.Spread($("#spreadContainer").get(0),{sheetCount:3});
             // Get active sheet in spread instance
             var activeSheet = spread.getActiveSheet();
            // Here is a sample to set A1 cell value to "A1" and foreground color to "red"
             // activeSheet.getCell(0,0).value("A1").foreColor("red");
             //
             // TODO: more initialize code here
        });
        //]]>
     </script>
 </head>
 <body>
```
Create the DOM element that is the target of the SpreadJS widget.  Colorized Example Code 
```JavaScript 
<div id="spreadContainer" style="width: 600px; height: 400px; border: 1px solid gray">
 </div>
 </body>
 </html>
```
 
