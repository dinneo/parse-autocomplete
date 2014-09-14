# Parse.AutoCompleteView #

An auto-complete widget for the Parse.com JS SDK.
Ported from one created for Backbone.js by
[Fatih Erikli](https://github.com/fatiherikli/backbone-autocomplete "Fatih Erikli")

##Installation##
You can use bower to install:
<pre>
bower install http://github.com/timofei7/parse-autocomplete.git --save
</pre>

##Usage##
Create a `label` method in your Parse Object (aka backbone Model).
<pre>
var Plugin = Parse.Model.extend({
  label: function () {
    return this.get("name");
  }
});
</pre>


##Initialize the AutoCompleteView in your view.##
<pre>
new AutoCompleteView({
  input: $("#plugin"), // your input field
  model: Plugin // your parse class
}).render();
</pre>


##Configuration##
Parameter | Type | Default | Description<br>
--------- | ---- | ------- | ----------------------------
className	| string  | autocomplete  | The class name of popup menu.
wait | integer | 300 | The throttling value as milliseconds.
minKeywordLength | integer | 2 | Minimum keyword length.
queryParameter | string | query | The search parameter for back-end.
onSelect | function | no-op | The callback function for selected item.
