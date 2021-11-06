# event-id
Google Tag Manager Custom Variable Template for generating unique event ids.

## Deduplication for CAPI and Facebook Pixel
The template can be used to create a uique event id at every event-push to the dataLayer in Google Tag Manager. Use the variable for deduplication of FB hits from browser. 

Add the variable as eventID to custom HTML code (https://developers.facebook.com/docs/marketing-api/conversions-api/deduplicate-pixel-and-server-events/) or "Event-Id" field in the FB tag, when using the facebookincubator tag template.

Then add an event parameter "event_id" to your corresponding GA4 tag that fires on the same event. 

*Note*: If you are not able to fire both GA4 and FB Pixel on the same dataLayer event, you can not use this variable. For example this might occur when different trigger groups are used to combine events and vendor consent.

There is a gist with a workaround to create a cached event id for every type of event (and some fixes for other edge cases) at https://gist.github.com/mbaersch/5919bc1c795031183a525cb8c64a9352  
