### Parse.AutoCompleteView

An auto-complete widget built with Backbone.js

##Usage##
Create a method that called `label` on your model. That method will be used for representation of model.
      var Plugin = Parse.Model.extend({
          label: function () {
              return this.get("name");
          }
      });


##And initialize the AutoCompleteView in your view.##
    new AutoCompleteView({
        input: $("#plugin"), // your input field
        model: Plugin // your parse object
    }).render();

##Configuration##
Parameter	Type	Default	Description
className	string	autocomplete	The class name of popup menu.
wait	integer	300	The throttling value as milliseconds.
minKeywordLength	integer	2	Minimum keyword length.
queryParameter	string	query	The search parameter for back-end.
onSelect	function	no-op	The callback function for selected item.
