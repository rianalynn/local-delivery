/*This code will serve as the snippet for WeDeliver merchant companies using Shopify*/

  <h3>Local Order WeDeliver</h3>
{{ 'http://code.jquery.com/ui/1.9.2/themes/base/jquery-ui.css' | stylesheet_tag }}
{{ '//ajax.googleapis.com/ajax/libs/jqueryui/1.9.2/jquery-ui.min.js' | script_tag }}
 
<div style="width:300px; clear:both;">
  <p>
    <label for="date">Pick a delivery date:</label>
    <input id="date" type="text" name="attributes[date]" value="{{ cart.attributes.date }}" />
  </p>
  <p>
	{% assign attribute = 'delivery-time' %}
	<label for="{{ attribute }}">Pick a delivery time: </label>
	<select id="{{ attribute }}" name="attributes[{{ attribute }}]">
    <!-- Below, set the upper-bound number to the number of options -->
    {% for i in (1..22) %}
    <!-- List your options here, captain... -->
    {% capture option %}{% cycle 'Please select', '8am', '8.30am', '9am', '9.30am', '10am', '10.30am', '11am', '11.30am', '12pm', '12.30pm', '1pm', '1.30pm', '2pm', '2.30pm', '3pm', '3.30pm', '4pm', '4.30pm', '5pm', '5.30pm', '6pm'  %}{% endcapture %}
    <option value="{{ option }}"{% if cart.attributes[attribute] == option %} selected="selected"{% endif %}>{{ option }}</option>
    {% endfor %}
	</select>
  </p>
  <p>    
      <span style="display:block" class="instructions"> We need a 24-hour notice for deliveries. You will receive a delivery time-frame upon review. Local Chicago Delivery powered by <a ref="http://www.wedeliver.us"> WeDeliver.</a></span>
  </p>
    
</div>
 
<script>
jQuery(function() {
  jQuery("#date").datepicker( { 
    minDate: +1, 
    maxDate: "+2M"
  } );
});
</script>
