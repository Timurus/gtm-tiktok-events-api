# TikTok Events API Tag for Google Tag Manager (Server-side)
The TikTok Events API is a Server-to-Server (S2S) integration that allows you to share website and app visitor events directly to TikTok. Data that is shared via the Events API is processed similar to information shared via other TikTok data integration business tools, like the TikTok pixel and TikTok SDK.

This Tag uses the standard GA4 Client and parses GA4 input into TikTok data and sends it through the Events API.

/This tag also supports to send from other sources/

## Input variables
* TikTok Pixel Code
* TikTok Pixel Access Token 
* (optional) GA4 Map Purchase Event

## GA4 Standard Events Mapping
The Tag parses all GA4 Client Events into TikTok Events. 

### Mapped Events
`{
  "page_view": "PageView",
  "view_item": "ViewContent",
  "click": "ClickButton",
  "search": "Search",
  "add_to_wishlist": "AddToWishlist",
  "begin_checkout": "InitiateCheckout",
  "add_payment_info": "AddPaymentInfo",
  "purchase": ”__READ_BELOW__”,
  "contact": "Contact",
  "download": "Download",
  "file_download": "Download",
  "generate_lead": "SubmitForm",
  "complete_registration": "CompleteRegistration",
  "subscribe": 'Subscribe'
}`

For the *Purchase* event you will be able to select in the dropdown menu which of the following TikTok Purchase events to map with: *PlaceAnOrder* or *CompletePayment*. By default *PlaceAnOrder* will be selected.

## Other ways to use the Tag
If you are not using GA4 standard events you can still use this tag to send data to TikTok

The request Parameters supported are
*General*
`x-ttq-event-name` - TikTok Event Name
`x-ttq-timestamp` - Timestamp in seconds
`x-ttq-event-id` - Event Id for the event (will be generated by the tag if skipped)

*Context* 
`x-ttq-ct-ip-adress` - User IP Adress
`x-ttq-ct-user-agent` - Web User Agent
`x-ttq-ct-page-url` - Page Url
`x-ttq-ct-page-referrer` - Page Referrer

`x-ttq-ttclid` - TikTok Click ID - If not in the Url, this can be sent manually.

*User Data*
`x-ttq-ud-external-id` - external id (if hashed, use sha256)
`x-ttq-ud-email` - email (if hashed, use sha256)
`x-ttq-ud-phone-number` - phone number (if hashed, use sha256)

*Properties*
`x-ttq-pt-contents` - Contents Array
`x-ttq-pt-currency` - Currency Code
`x-ttq-pt-value` - Total Value (numeric)
`x-ttq-pt-description` - Dscription
`x-ttq-pt-query` - Search Query

## Links
[Tiktok Events API]([TikTok Marketing API](https://ads.tiktok.com/marketing_api/docs?id=1701890979375106))
[Google Tag Manager Server Side]([Server-side tagging  |  Google Tag Manager - Server-side  |  Google Developers](https://developers.google.com/tag-platform/tag-manager/server-side))
[GA4 Send Data]([Send data to server-side Google Tag Manager  |  Google Tag Manager - Server-side  |  Google Developers](https://developers.google.com/tag-platform/tag-manager/server-side/send-data))
