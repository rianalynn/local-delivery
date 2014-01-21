This code will serve as the snippet for WeDeliver merchant companies using Shopify

  <h3>Local Order WeDeliver</h3>
{{ 'http://code.jquery.com/ui/1.9.2/themes/base/jquery-ui.css' | stylesheet_tag }}
{{ '//ajax.googleapis.com/ajax/libs/jqueryui/1.9.2/jquery-ui.min.js' | script_tag }}
 
<div style="width:300px; clear:both;">
  <p>
    <label for="date">Pick a delivery date:</label>
    <input id="date" type="text" name="attributes[date]" value="{{ cart.attributes.date }}" />
    <span style="display:block" class="instructions"> You will receive a delivery time-frame upon review. Local Chicago Delivery powered by WeDeliver.</span>
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
