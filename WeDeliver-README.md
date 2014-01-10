
  
  This code will serve as the snippet for WeDeliver merchant companies using Shopify
  
   local-delivery
==============




  <div id="order-delivery">
  <h3>Local Order WeDeliver</h3>
      
    <div id="order-delivery-form-wrapper" class="clearfix">
      <p>One or more of the items in your cart are available for local delivery.<p>
      
      <p>{{shop.metafields.local_delivery.custom_text}}</p>
      
      <p>When would you like your order delivered?</p>
      
      <p>Date: <input type="text" id="datepicker" readonly="readonly" /> <p>

      <div id="loading">Finding available delivery times...</div>
      
      <div style="DISPLAY: none" id="timeDiv">
        <p>Time:<select name="attributes[local_delivery_request]" id="local_delivery" style="width: 150px"></select></p> 
      </div>
        
    </div>
  
    <div id="wrapper-response"></div>
  </div>
  
  <br />
{% endif %}
