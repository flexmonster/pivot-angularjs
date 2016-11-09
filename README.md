# Flexmonster Pivot table component integration with AngularJS framework
[![Flexmonster Pivot table component](https://s3.amazonaws.com/flexmonster/github/fm-github-cover.png)](http://flexmonster.com)
Website: www.flexmonster.com

## Example

Please find more examples in the repository. Also, [full tutorial is available at the www.flexmonster.com](http://www.flexmonster.com/doc/integration-with-angularjs/).
```html
<!DOCTYPE html>
<html ng-app="App">
<head>
    <title>My AngularJS/Flexmonster Project</title>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.8/angular.js"></script>
    <script type="text/javascript">angular.module("App", ["flexmonster"]);</script>
    <script src="https://code.jquery.com/jquery-2.2.4.min.js"></script>
    <script src="https://s3.amazonaws.com/flexmonster/2.3/flexmonster.js"></script>
</head>
<body>
<div fm-pivot 
     fm-toolbar="true" 
     fm-component-folder="https://s3.amazonaws.com/flexmonster/2.3/"
     fm-report="'https://s3.amazonaws.com/flexmonster/2.3/reports/report.json'"
     fm-license-key="XXX">
</div>
</body>
</html>
```

## Properties

Please note, that every attribute for fm-pivot directive is set either as a string value or as an angular variable. List of available attributes:

- `fm-toolbar` – parameter to embed the toolbar or not. Default value is false – without the toolbar.
- `fm-license-key` – the license key.
- `fm-width` – width of the component on the page (pixels or percent). The default value for width is 100%.
- `fm-height` – height of the component on the page (pixels or percent). The default value for height is 500.
- `fm-component-folder` – URL of the component’s folder which contains all necessary files. Also, it is used as a base URL for report files, localization files, styles and images. The default value is `flexmonster/`.
- `fm-report` – property to set a report. It can be inline report JSON, URL to report JSON or URL to report XML.
- `fm-global` – object that allows you to preset options for all reports. These options can be overwritten for concrete reports. Object structure is the same as for report.

All attributes are equal to those which are passed to [`$.flexmonster()`](http://www.flexmonster.com/api/flexmonster/). The only difference is that `fm-` prefix was added to each of them.

## Event handlers:

- `fm-ready`
- `fm-report-complete`
- `fm-report-change`
- `fm-update`
- `fm-cell-click`
- `fm-cell-doubleclick`
- `fm-filter-open`
- `fm-fields-list-open`
- `fm-fields-list-close`

Full list of events is [available in the documentation](http://www.flexmonster.com/api/events/).
