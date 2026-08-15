# \GoogleApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**google_get_author_citations_per_year_chart**](GoogleApi.md#google_get_author_citations_per_year_chart) | **GET** /v1/google/scholar/author/citation | Get author citations-per-year chart
[**google_get_business_posts**](GoogleApi.md#google_get_business_posts) | **GET** /v1/google/maps/posts | Get business posts
[**google_get_citation_formats_for_a_scholar_paper**](GoogleApi.md#google_get_citation_formats_for_a_scholar_paper) | **GET** /v1/google/scholar/cite | Get citation formats for a Scholar paper
[**google_get_place_details**](GoogleApi.md#google_get_place_details) | **GET** /v1/google/maps/place | Get place details
[**google_get_place_photos**](GoogleApi.md#google_get_place_photos) | **GET** /v1/google/maps/photos | Get place photos
[**google_get_place_reviews**](GoogleApi.md#google_get_place_reviews) | **GET** /v1/google/maps/reviews | Get place reviews
[**google_get_scholar_author_profile**](GoogleApi.md#google_get_scholar_author_profile) | **GET** /v1/google/scholar/author | Get Scholar author profile
[**google_get_stock_index_quote**](GoogleApi.md#google_get_stock_index_quote) | **GET** /v1/google/finance/quote | Get stock/index quote
[**google_google_ai_mode_search**](GoogleApi.md#google_google_ai_mode_search) | **GET** /v1/google/ai-mode/search | Google AI Mode search
[**google_google_ai_overview_inline_serp_block**](GoogleApi.md#google_google_ai_overview_inline_serp_block) | **GET** /v1/google/ai-overview | Google AI Overview (inline SERP block)
[**google_google_flights_calendar_cheapest_fare_per_date**](GoogleApi.md#google_google_flights_calendar_cheapest_fare_per_date) | **GET** /v1/google/flights/calendar | Google Flights calendar — cheapest fare per date
[**google_google_flights_search**](GoogleApi.md#google_google_flights_search) | **GET** /v1/google/flights/search | Google Flights search
[**google_google_lens_visual_search**](GoogleApi.md#google_google_lens_visual_search) | **GET** /v1/google/lens/search | Google Lens visual search
[**google_google_scraper_health_check**](GoogleApi.md#google_google_scraper_health_check) | **GET** /v1/google/health | Google scraper health check
[**google_google_scraper_health_check_head**](GoogleApi.md#google_google_scraper_health_check_head) | **HEAD** /v1/google/health | Google scraper health check
[**google_google_search_suggestions**](GoogleApi.md#google_google_search_suggestions) | **GET** /v1/google/autocomplete | Google search suggestions
[**google_google_shorts_search**](GoogleApi.md#google_google_shorts_search) | **GET** /v1/google/shorts/search | Google Shorts search
[**google_google_web_search**](GoogleApi.md#google_google_web_search) | **GET** /v1/google/search | Google web search
[**google_hotel_details**](GoogleApi.md#google_hotel_details) | **GET** /v1/google/hotels/details | Hotel details
[**google_immersive_product_detail**](GoogleApi.md#google_immersive_product_detail) | **GET** /v1/google/products/detail | Immersive product detail
[**google_interest_by_region**](GoogleApi.md#google_interest_by_region) | **GET** /v1/google/trends/regions | Interest by region
[**google_interest_over_time**](GoogleApi.md#google_interest_over_time) | **GET** /v1/google/trends/interest | Interest over time
[**google_multi_seller_offers_by_barcode**](GoogleApi.md#google_multi_seller_offers_by_barcode) | **GET** /v1/google/shopping/offers | Multi-seller offers by barcode
[**google_news_by_topic**](GoogleApi.md#google_news_by_topic) | **GET** /v1/google/news/topics | News by topic
[**google_patent_details**](GoogleApi.md#google_patent_details) | **GET** /v1/google/patents/detail | Patent details
[**google_related_topics_queries**](GoogleApi.md#google_related_topics_queries) | **GET** /v1/google/trends/related | Related topics & queries
[**google_search_google_images**](GoogleApi.md#google_search_google_images) | **GET** /v1/google/images/search | Search Google Images
[**google_search_google_jobs**](GoogleApi.md#google_search_google_jobs) | **GET** /v1/google/jobs/search | Search Google Jobs
[**google_search_google_maps_places**](GoogleApi.md#google_search_google_maps_places) | **GET** /v1/google/maps/search | Search Google Maps places
[**google_search_google_news**](GoogleApi.md#google_search_google_news) | **GET** /v1/google/news/search | Search Google News
[**google_search_google_scholar**](GoogleApi.md#google_search_google_scholar) | **GET** /v1/google/scholar/search | Search Google Scholar
[**google_search_google_videos**](GoogleApi.md#google_search_google_videos) | **GET** /v1/google/videos/search | Search Google Videos
[**google_search_hotels**](GoogleApi.md#google_search_hotels) | **GET** /v1/google/hotels/search | Search hotels
[**google_search_patents**](GoogleApi.md#google_search_patents) | **GET** /v1/google/patents/search | Search patents
[**google_search_products**](GoogleApi.md#google_search_products) | **GET** /v1/google/shopping/search | Search products
[**google_search_scholar_author_profiles**](GoogleApi.md#google_search_scholar_author_profiles) | **GET** /v1/google/scholar/profiles | Search Scholar author profiles
[**google_trending_news**](GoogleApi.md#google_trending_news) | **GET** /v1/google/news/trending | Trending news
[**google_trending_searches**](GoogleApi.md#google_trending_searches) | **GET** /v1/google/trends/trending | Trending searches
[**google_trends_topic_autocomplete**](GoogleApi.md#google_trends_topic_autocomplete) | **GET** /v1/google/trends/autocomplete | Trends topic autocomplete



## google_get_author_citations_per_year_chart

> serde_json::Value google_get_author_citations_per_year_chart(author_id, hl)
Get author citations-per-year chart

Return the citations-per-year chart for a Google Scholar author.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**author_id** | **String** | Scholar user ID | [required] |
**hl** | Option<**String**> | Language code |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_get_business_posts

> serde_json::Value google_get_business_posts(data_id, next_page_token)
Get business posts

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**data_id** | **String** | Maps data ID | [required] |
**next_page_token** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_get_citation_formats_for_a_scholar_paper

> serde_json::Value google_get_citation_formats_for_a_scholar_paper(q, hl)
Get citation formats for a Scholar paper

Return MLA, APA, Chicago, Harvard, and Vancouver citation formats for a paper.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Cluster ID from a search result | [required] |
**hl** | Option<**String**> | Language code |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_get_place_details

> serde_json::Value google_get_place_details(place_id, data_id, hl, gl)
Get place details

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**place_id** | Option<**String**> |  |  |
**data_id** | Option<**String**> |  |  |
**hl** | Option<**String**> |  |  |[default to en]
**gl** | Option<**String**> |  |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_get_place_photos

> serde_json::Value google_get_place_photos(data_id, hl, next_page_token)
Get place photos

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**data_id** | **String** | Maps data ID | [required] |
**hl** | Option<**String**> |  |  |[default to en]
**next_page_token** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_get_place_reviews

> serde_json::Value google_get_place_reviews(data_id, sort_by, hl, next_page_token, results)
Get place reviews

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**data_id** | **String** | Maps data ID | [required] |
**sort_by** | Option<**String**> | qualityScore | newestFirst | ratingHigh | ratingLow |  |[default to qualityScore]
**hl** | Option<**String**> |  |  |[default to en]
**next_page_token** | Option<**String**> | Cursor from the previous response's pagination.next; omit for page 1. |  |
**results** | Option<**i32**> |  |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_get_scholar_author_profile

> serde_json::Value google_get_scholar_author_profile(author_id, hl, cstart, pagesize)
Get Scholar author profile

Get detailed Google Scholar author profile including articles, stats, co-authors.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**author_id** | **String** | Scholar user ID (the `user` query parameter) | [required] |
**hl** | Option<**String**> | Language code |  |[default to en]
**cstart** | Option<**i32**> | Articles pagination offset |  |[default to 0]
**pagesize** | Option<**i32**> | Articles per page |  |[default to 20]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_get_stock_index_quote

> serde_json::Value google_get_stock_index_quote(q, hl)
Get stock/index quote

Get a stock or index quote from Google Finance.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Ticker and exchange (e.g. \"AAPL:NASDAQ\", \"BTC-USD\") | [required] |
**hl** | Option<**String**> | Language code |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_google_ai_mode_search

> serde_json::Value google_google_ai_mode_search(q, gl, hl, include_html)
Google AI Mode search

Get AI-generated search results from Google AI Mode.  Returns the structured `text_blocks` (paragraphs, headings, comparison `table` blocks and lists), a flat `references` source list, a compact `markdown` rendering of the whole answer and — unless `include_html` is false — the raw `answer_html` body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query for AI-generated response | [required] |
**gl** | Option<**String**> | Country code |  |[default to us]
**hl** | Option<**String**> | Language code |  |[default to en]
**include_html** | Option<**bool**> | Include the raw `answer_html` (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured `text_blocks` + `markdown`. |  |[default to true]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_google_ai_overview_inline_serp_block

> serde_json::Value google_google_ai_overview_inline_serp_block(q, gl, hl)
Google AI Overview (inline SERP block)

Get the AI Overview block Google renders inline at the top of a SERP.  Deferred overviews (where Google lazy-loads the block via a follow-up ``page_token``) are chased automatically.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query — same shape as a Google Search query | [required] |
**gl** | Option<**String**> | Country code |  |[default to us]
**hl** | Option<**String**> | Language code |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_google_flights_calendar_cheapest_fare_per_date

> serde_json::Value google_google_flights_calendar_cheapest_fare_per_date(departure_id, arrival_id, outbound_date_from, outbound_date_to, trip_type, trip_length_days, return_date_from, return_date_to, adults, children, infants_in_seat, infants_on_lap, travel_class, currency, gl, hl)
Google Flights calendar — cheapest fare per date

Price a whole range of dates in one call — up to 200 dates per request.  Google Flights' own price graph / date grid: the cheapest fare per departure date instead of one search per date. Prices match `/flights/search` exactly.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**departure_id** | **String** | Departure airport IATA code or location ID | [required] |
**arrival_id** | **String** | Arrival airport IATA code or location ID | [required] |
**outbound_date_from** | **String** | First outbound date to price (YYYY-MM-DD) | [required] |
**outbound_date_to** | **String** | Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode. | [required] |
**trip_type** | Option<**String**> | one_way | round_trip |  |[default to one_way]
**trip_length_days** | Option<**i32**> | Round-trip stay length in nights (price-graph mode). Defaults to 7. |  |
**return_date_from** | Option<**String**> | Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only. |  |
**return_date_to** | Option<**String**> | Date-grid mode: last return date |  |
**adults** | Option<**i32**> |  |  |[default to 1]
**children** | Option<**i32**> |  |  |[default to 0]
**infants_in_seat** | Option<**i32**> |  |  |[default to 0]
**infants_on_lap** | Option<**i32**> |  |  |[default to 0]
**travel_class** | Option<**String**> |  |  |[default to economy]
**currency** | Option<**String**> | ISO-4217 currency |  |[default to USD]
**gl** | Option<**String**> |  |  |[default to us]
**hl** | Option<**String**> |  |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_google_flights_search

> serde_json::Value google_google_flights_search(departure_id, arrival_id, outbound_date, return_date, trip_type, adults, children, infants_in_seat, infants_on_lap, travel_class, currency, gl, hl, stops, max_price, departure_token)
Google Flights search

Search Google Flights for available itineraries.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**departure_id** | **String** | Departure airport IATA code or location ID | [required] |
**arrival_id** | **String** | Arrival airport IATA code or location ID | [required] |
**outbound_date** | **String** | Outbound date (YYYY-MM-DD) | [required] |
**return_date** | Option<**String**> | Return date (round-trip only) |  |
**trip_type** | Option<**String**> | round_trip | one_way | multi_city |  |[default to round_trip]
**adults** | Option<**i32**> |  |  |[default to 1]
**children** | Option<**i32**> |  |  |[default to 0]
**infants_in_seat** | Option<**i32**> |  |  |[default to 0]
**infants_on_lap** | Option<**i32**> |  |  |[default to 0]
**travel_class** | Option<**String**> |  |  |[default to economy]
**currency** | Option<**String**> | ISO-4217 currency |  |[default to USD]
**gl** | Option<**String**> |  |  |[default to us]
**hl** | Option<**String**> |  |  |[default to en]
**stops** | Option<**String**> |  |  |[default to any]
**max_price** | Option<**i32**> |  |  |
**departure_token** | Option<**String**> | A round-trip offer's departure_token; returns the return-leg flights for that selected outbound (round-trip only). |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_google_lens_visual_search

> serde_json::Value google_google_lens_visual_search(url, query, country, language, gl, hl, product, visual_matches, exact_matches)
Google Lens visual search

Google Lens visual search.  Response carries ``lens_results`` (Scrapingdog parity alias) with ``title`` / ``source`` / ``source_favicon`` / ``thumbnail`` / ``original_thumbnail`` / ``rating`` / ``reviews`` / ``in_stock``, plus ``price`` (``{value, currency, extracted}``) and the raw ``tag`` chip it is parsed from, on shoppable matches. ``related_searches`` chips come alongside. Legacy ``results`` alias kept for backwards compat.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | Public URL of the image to search visually | [required] |
**query** | Option<**String**> | Optional text refinement (e.g. 'pizza') |  |
**country** | Option<**String**> | ISO country code (alias for gl) |  |
**language** | Option<**String**> | Language code (alias for hl) |  |
**gl** | Option<**String**> | Country code |  |[default to us]
**hl** | Option<**String**> | Language code |  |[default to en]
**product** | Option<**bool**> | Bias towards shoppable product matches |  |[default to false]
**visual_matches** | Option<**bool**> | Include the visual-matches carousel |  |[default to true]
**exact_matches** | Option<**bool**> | Restrict to exact-match results |  |[default to false]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_google_scraper_health_check

> serde_json::Value google_google_scraper_health_check()
Google scraper health check

Check health of the Google scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_google_scraper_health_check_head

> serde_json::Value google_google_scraper_health_check_head()
Google scraper health check

Check health of the Google scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_google_search_suggestions

> serde_json::Value google_google_search_suggestions(q, hl, gl)
Google search suggestions

Get Google search autocomplete suggestions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query to get suggestions for | [required] |
**hl** | Option<**String**> | Language code |  |[default to en]
**gl** | Option<**String**> | Country code |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_google_shorts_search

> serde_json::Value google_google_shorts_search(q, gl, hl, domain, num, start)
Google Shorts search

Return short-form video results (YouTube Shorts, TikToks) from Google Shorts mode.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query | [required] |
**gl** | Option<**String**> | Country code |  |[default to us]
**hl** | Option<**String**> | Language code |  |[default to en]
**domain** | Option<**String**> | Google domain |  |[default to google.com]
**num** | Option<**i32**> | Results per page |  |[default to 20]
**start** | Option<**i32**> | Pagination offset |  |[default to 0]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_google_web_search

> serde_json::Value google_google_web_search(q, gl, hl, num, start, domain, device, user_agent, output, location, lr, tbs, safe, uule, filter, nfpr, cr, ludocid, lsig, kgmid, si, ibp, uds, ai_overview)
Google web search

Search Google and get structured results (organic, ads, KG, AI overview, PAA).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query (supports Google operators) | [required] |
**gl** | Option<**String**> | Country code |  |[default to us]
**hl** | Option<**String**> | Language code |  |[default to en]
**num** | Option<**i32**> |  |  |[default to 10]
**start** | Option<**i32**> | Page offset (0, 10, 20...) |  |[default to 0]
**domain** | Option<**String**> | Google domain |  |[default to google.com]
**device** | Option<**String**> | Device target: desktop, mobile, iphone, android, tablet |  |[default to desktop]
**user_agent** | Option<**String**> | Custom User-Agent (overrides device) |  |
**output** | Option<**String**> | Response format: json (parsed) or html (raw SERP) |  |[default to json]
**location** | Option<**String**> | City-level geo-targeting |  |
**lr** | Option<**String**> | Language restrict (e.g. lang_en) |  |
**tbs** | Option<**String**> | Time filter (e.g. qdr:d) |  |
**safe** | Option<**String**> |  |  |[default to off]
**uule** | Option<**String**> | UULE encoded location |  |
**filter** | Option<**i32**> | Show omitted results |  |
**nfpr** | Option<**i32**> | Disable auto-correction |  |[default to 0]
**cr** | Option<**String**> | Country restrict |  |
**ludocid** | Option<**String**> | Google Place CID |  |
**lsig** | Option<**String**> | Knowledge Graph map ID |  |
**kgmid** | Option<**String**> | Knowledge Graph entity ID |  |
**si** | Option<**String**> | Cached search params |  |
**ibp** | Option<**String**> | Layout control |  |
**uds** | Option<**String**> | Google filter string |  |
**ai_overview** | Option<**bool**> | Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview. |  |[default to false]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_hotel_details

> serde_json::Value google_hotel_details(property_token, check_in, check_out)
Hotel details

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**property_token** | **String** | Property token | [required] |
**check_in** | **String** | YYYY-MM-DD | [required] |
**check_out** | **String** | YYYY-MM-DD | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_immersive_product_detail

> serde_json::Value google_immersive_product_detail(product_id, q, gl, hl, catalog_id, image_docid, headline_offer_docid, mid, include_offers, include_variants)
Immersive product detail

Get deep product details from Google's immersive product page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Google Shopping ``gpcid`` — the product_id returned on ``/shopping/search`` tiles. Scrapingdog-compatible. | [required] |
**q** | **String** | Original search query that surfaced the product. Required by Google's ``/async/oapv`` RPC. | [required] |
**gl** | Option<**String**> | Country code (ISO 3166 alpha-2) |  |[default to us]
**hl** | Option<**String**> | Language code |  |[default to en]
**catalog_id** | Option<**String**> | Optional ``catalogid`` from the Shopping tile (improves parity). |  |
**image_docid** | Option<**String**> | Optional ``imageDocid`` for higher-fidelity images. |  |
**headline_offer_docid** | Option<**String**> | Optional ``headlineOfferDocid`` to pin the featured seller. |  |
**mid** | Option<**String**> | Optional Google Knowledge-Graph ``mid``. |  |
**include_offers** | Option<**bool**> | When true, fetch the full merchant-offer list via a secondary RPC (``/async/piu_ps``). Adds ~1 s. |  |[default to false]
**include_variants** | Option<**bool**> | When true, fetch size/colour variants via a secondary RPC (``/async/toy_v``). Adds ~1 s. |  |[default to false]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_interest_by_region

> serde_json::Value google_interest_by_region(q, geo)
Interest by region

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search term | [required] |
**geo** | Option<**String**> |  |  |[default to ]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_interest_over_time

> serde_json::Value google_interest_over_time(q, geo, date)
Interest over time

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search terms | [required] |
**geo** | Option<**String**> |  |  |[default to ]
**date** | Option<**String**> |  |  |[default to today 12-m]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_multi_seller_offers_by_barcode

> serde_json::Value google_multi_seller_offers_by_barcode(barcode, gl, hl)
Multi-seller offers by barcode

Resolve a barcode to a product via Google web search, then return its Google Shopping seller offers (source + price per merchant).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**barcode** | **String** | Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14 | [required] |
**gl** | Option<**String**> | Country code (ISO 3166 alpha-2) |  |
**hl** | Option<**String**> | Language code |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_news_by_topic

> serde_json::Value google_news_by_topic(topic, hl, gl, max_results)
News by topic

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**topic** | **String** | Topic name | [required] |
**hl** | Option<**String**> |  |  |[default to en]
**gl** | Option<**String**> |  |  |[default to US]
**max_results** | Option<**i32**> |  |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_patent_details

> serde_json::Value google_patent_details(patent_id)
Patent details

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**patent_id** | **String** | Patent number | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_related_topics_queries

> serde_json::Value google_related_topics_queries(q, geo)
Related topics & queries

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search term | [required] |
**geo** | Option<**String**> |  |  |[default to ]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_search_google_images

> serde_json::Value google_search_google_images(q, gl, hl, tbs, imgsz, imgcolor, imgtype, safe, page)
Search Google Images

Search Google Images for visual content.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Image search query | [required] |
**gl** | Option<**String**> | Country code |  |[default to us]
**hl** | Option<**String**> | Language code |  |[default to en]
**tbs** | Option<**String**> | Time/filter string (e.g. qdr:d) |  |
**imgsz** | Option<**String**> | Image size: l, m, i, xXl |  |
**imgcolor** | Option<**String**> | Image color filter |  |
**imgtype** | Option<**String**> | Image type: face, photo, clipart |  |
**safe** | Option<**String**> | Safe search |  |[default to off]
**page** | Option<**i32**> | Page number |  |[default to 0]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_search_google_jobs

> serde_json::Value google_search_google_jobs(q, location, gl, job_type, date_posted)
Search Google Jobs

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Job title, keywords | [required] |
**location** | Option<**String**> |  |  |
**gl** | Option<**String**> |  |  |[default to us]
**job_type** | Option<**String**> |  |  |
**date_posted** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_search_google_maps_places

> serde_json::Value google_search_google_maps_places(q, ll, gl, hl, start)
Search Google Maps places

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query | [required] |
**ll** | Option<**String**> |  |  |
**gl** | Option<**String**> |  |  |[default to us]
**hl** | Option<**String**> |  |  |[default to en]
**start** | Option<**i32**> |  |  |[default to 0]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_search_google_news

> serde_json::Value google_search_google_news(q, hl, gl, max_results)
Search Google News

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query | [required] |
**hl** | Option<**String**> |  |  |[default to en]
**gl** | Option<**String**> |  |  |[default to US]
**max_results** | Option<**i32**> |  |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_search_google_scholar

> serde_json::Value google_search_google_scholar(q, hl, as_ylo, as_yhi, as_sdt, page, num)
Search Google Scholar

Search Google Scholar for scholarly articles.  Each result ships with its doc ``id``, ``type`` badge ([BOOK]/[PDF]/...), wrapped ``inline_links`` (versions + cited_by + related), PDF ``resources`` list, and structured ``authors`` (with ``author_id`` for profiled authors — pipe straight into ``/scholar/author``). Envelope carries ``scholar_results`` alias (Scrapingdog parity), ``related_searches``, and matched ``profiles`` cards.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query for scholarly articles | [required] |
**hl** | Option<**String**> | Language code |  |[default to en]
**as_ylo** | Option<**i32**> | Year from (e.g. 2020) |  |
**as_yhi** | Option<**i32**> | Year to (e.g. 2024) |  |
**as_sdt** | Option<**String**> | Search type: 0=exclude patents, 7=include |  |[default to 0]
**page** | Option<**i32**> | Page number (0-based) |  |[default to 0]
**num** | Option<**i32**> | Results per page (max 20) |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_search_google_videos

> serde_json::Value google_search_google_videos(q, gl, hl, tbs, safe, page)
Search Google Videos

Search Google for video results.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Video search query | [required] |
**gl** | Option<**String**> | Country code |  |[default to us]
**hl** | Option<**String**> | Language code |  |[default to en]
**tbs** | Option<**String**> | Time filter (e.g. qdr:d) |  |
**safe** | Option<**String**> | Safe search |  |[default to off]
**page** | Option<**i32**> | Page number |  |[default to 0]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_search_hotels

> serde_json::Value google_search_hotels(q, check_in, check_out, adults, currency, gl)
Search hotels

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Location or hotel name | [required] |
**check_in** | **String** | YYYY-MM-DD | [required] |
**check_out** | **String** | YYYY-MM-DD | [required] |
**adults** | Option<**i32**> |  |  |[default to 2]
**currency** | Option<**String**> |  |  |[default to USD]
**gl** | Option<**String**> |  |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_search_patents

> serde_json::Value google_search_patents(q, page, num, sort, inventor, assignee, country, language, status, patent_type, before, after)
Search patents

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query (Boolean logic supported) | [required] |
**page** | Option<**i32**> |  |  |[default to 0]
**num** | Option<**i32**> |  |  |[default to 10]
**sort** | Option<**String**> | 'new' or 'old' |  |
**inventor** | Option<**String**> | Inventor name(s) |  |
**assignee** | Option<**String**> | Assignee / company name(s) |  |
**country** | Option<**String**> | Country code (US, EP, WO, …) |  |
**language** | Option<**String**> | Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH |  |
**status** | Option<**String**> | GRANT or APPLICATION |  |
**patent_type** | Option<**String**> | PATENT or DESIGN |  |
**before** | Option<**String**> | Before date YYYYMMDD |  |
**after** | Option<**String**> | After date YYYYMMDD |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_search_products

> serde_json::Value google_search_products(q, gl, min_price, max_price, sort_by)
Search products

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Product search query | [required] |
**gl** | Option<**String**> |  |  |[default to us]
**min_price** | Option<**i32**> |  |  |
**max_price** | Option<**i32**> |  |  |
**sort_by** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_search_scholar_author_profiles

> serde_json::Value google_search_scholar_author_profiles(mauthors, hl, after_author, before_author)
Search Scholar author profiles

Search Google Scholar for author profiles by name.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**mauthors** | **String** | Author name query (e.g. 'Geoffrey Hinton') | [required] |
**hl** | Option<**String**> | Language code |  |[default to en]
**after_author** | Option<**String**> | Pagination token (next page) |  |
**before_author** | Option<**String**> | Pagination token (previous page) |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_trending_news

> serde_json::Value google_trending_news(hl, gl, max_results)
Trending news

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**hl** | Option<**String**> |  |  |[default to en]
**gl** | Option<**String**> |  |  |[default to US]
**max_results** | Option<**i32**> |  |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_trending_searches

> serde_json::Value google_trending_searches(geo)
Trending searches

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**geo** | Option<**String**> |  |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_trends_topic_autocomplete

> serde_json::Value google_trends_topic_autocomplete(q, hl, tz)
Trends topic autocomplete

Return categorized Knowledge Graph topic entities (mid, type) for a query.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Query prefix to resolve into Trends topics | [required] |
**hl** | Option<**String**> | Language code |  |[default to en-US]
**tz** | Option<**String**> | Timezone offset in minutes |  |[default to 0]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

