# \BookingApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**booking_booking_scraper_health_check**](BookingApi.md#booking_booking_scraper_health_check) | **GET** /v1/booking/health | Booking scraper health check
[**booking_booking_scraper_health_check_head**](BookingApi.md#booking_booking_scraper_health_check_head) | **HEAD** /v1/booking/health | Booking scraper health check
[**booking_get_property_detail**](BookingApi.md#booking_get_property_detail) | **GET** /v1/booking/properties/{country_code}/{slug} | Get property detail
[**booking_get_property_reviews**](BookingApi.md#booking_get_property_reviews) | **GET** /v1/booking/properties/{country_code}/{slug}/reviews | Get property reviews
[**booking_get_room_types_and_live_rates**](BookingApi.md#booking_get_room_types_and_live_rates) | **GET** /v1/booking/properties/{country_code}/{slug}/rooms | Get room types and live rates
[**booking_search_destinations**](BookingApi.md#booking_search_destinations) | **GET** /v1/booking/destinations | Search destinations
[**booking_search_properties**](BookingApi.md#booking_search_properties) | **GET** /v1/booking/search | Search properties



## booking_booking_scraper_health_check

> serde_json::Value booking_booking_scraper_health_check()
Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

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


## booking_booking_scraper_health_check_head

> serde_json::Value booking_booking_scraper_health_check_head()
Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

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


## booking_get_property_detail

> serde_json::Value booking_get_property_detail(country_code, slug, photos, questions, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Get property detail

Full detail for one property: description, address and coordinates, star rating, review score with per-category breakdown, facilities, house rules, room types with occupancy and beds, photos and guest Q&A.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country_code** | **String** | Two-letter country code, e.g. 'it' | [required] |
**slug** | **String** | Booking page name, e.g. 'hotel-artemide' | [required] |
**photos** | Option<**i32**> | Gallery photos to return |  |[default to 40]
**questions** | Option<**i32**> | Guest Q&A pairs to return |  |[default to 10]
**language** | Option<**String**> | Locale, e.g. en-us, fr |  |
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## booking_get_property_reviews

> serde_json::Value booking_get_property_reviews(country_code, slug, limit, offset, sort, review_language, guest_type, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Get property reviews

Paginated guest reviews with score, positive and negative text, stay dates, room type, guest country and type, photos and the partner's reply.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country_code** | **String** | Two-letter country code, e.g. 'it' | [required] |
**slug** | **String** | Booking page name, e.g. 'hotel-artemide' | [required] |
**limit** | Option<**i32**> |  |  |[default to 25]
**offset** | Option<**i32**> |  |  |[default to 0]
**sort** | Option<**String**> | MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC |  |[default to MOST_RELEVANT]
**review_language** | Option<**String**> | Only reviews written in this language, e.g. 'fr' |  |
**guest_type** | Option<**String**> | FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS |  |
**language** | Option<**String**> | Locale for labels, e.g. en-us |  |
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## booking_get_room_types_and_live_rates

> serde_json::Value booking_get_room_types_and_live_rates(country_code, slug, checkin, checkout, adults, children, rooms, currency, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Get room types and live rates

Every room type at one property with every rate bookable on it for the given dates — price, price before discount, price per night, discounts and badges — plus per-room facilities, bed layouts, occupancy and photos. /search returns only the cheapest rate per property; this returns the whole table.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country_code** | **String** | Two-letter country code, e.g. 'it' | [required] |
**slug** | **String** | Booking page name, e.g. 'hotel-artemide' | [required] |
**checkin** | **String** | Check-in date YYYY-MM-DD | [required] |
**checkout** | **String** | Check-out date YYYY-MM-DD | [required] |
**adults** | Option<**i32**> |  |  |[default to 2]
**children** | Option<**String**> | Comma-separated children ages, e.g. '4,9' |  |
**rooms** | Option<**i32**> |  |  |[default to 1]
**currency** | Option<**String**> | ISO currency, e.g. EUR, USD, GBP |  |
**language** | Option<**String**> | Locale, e.g. en-us, fr, de |  |
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## booking_search_destinations

> serde_json::Value booking_search_destinations(query, limit, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Search destinations

Resolve a place name to Booking's `dest_id`/`dest_type`, with coordinates and country — feed the pair back into /search for an exact match.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Free-text place, e.g. 'amsterd' | [required] |
**limit** | Option<**i32**> |  |  |[default to 8]
**language** | Option<**String**> | Locale, e.g. en-us, fr |  |
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## booking_search_properties

> serde_json::Value booking_search_properties(location, dest_id, dest_type, checkin, checkout, adults, children, rooms, offset, limit, sort, filters, currency, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Search properties

Search Booking.com properties by destination, with dates, occupancy, sorting and filters. Returns prices, review scores, coordinates, room configuration and photos. Paginate with `offset`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | Option<**String**> | Free-text destination, e.g. 'Rome' |  |
**dest_id** | Option<**i32**> | Exact destination id (ufi) from /destinations |  |
**dest_type** | Option<**String**> | Destination type, e.g. CITY |  |[default to NO_DEST_TYPE]
**checkin** | Option<**String**> | Check-in date YYYY-MM-DD |  |
**checkout** | Option<**String**> | Check-out date YYYY-MM-DD |  |
**adults** | Option<**i32**> |  |  |[default to 2]
**children** | Option<**String**> | Comma-separated children ages, e.g. '4,9' |  |
**rooms** | Option<**i32**> |  |  |[default to 1]
**offset** | Option<**i32**> | Result offset for pagination |  |[default to 0]
**limit** | Option<**i32**> |  |  |[default to 25]
**sort** | Option<**String**> | popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh |  |
**filters** | Option<**String**> | Semicolon-separated Booking filter ids, e.g. 'class=4' |  |
**currency** | Option<**String**> | ISO currency, e.g. EUR, USD, GBP |  |
**language** | Option<**String**> | Locale, e.g. en-us, fr, de, es |  |
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

