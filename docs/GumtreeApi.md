# \GumtreeApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gumtree_get_listing**](GumtreeApi.md#gumtree_get_listing) | **GET** /v1/gumtree/listings/{listing_id} | Get listing
[**gumtree_get_search_filters**](GumtreeApi.md#gumtree_get_search_filters) | **GET** /v1/gumtree/search/filters | Get search filters
[**gumtree_get_seller_listings**](GumtreeApi.md#gumtree_get_seller_listings) | **GET** /v1/gumtree/listings/{listing_id}/seller-listings | Get seller listings
[**gumtree_gumtree_scraper_health_check**](GumtreeApi.md#gumtree_gumtree_scraper_health_check) | **GET** /v1/gumtree/health | Gumtree scraper health check
[**gumtree_gumtree_scraper_health_check_head**](GumtreeApi.md#gumtree_gumtree_scraper_health_check_head) | **HEAD** /v1/gumtree/health | Gumtree scraper health check
[**gumtree_list_categories**](GumtreeApi.md#gumtree_list_categories) | **GET** /v1/gumtree/categories | List categories
[**gumtree_list_locations**](GumtreeApi.md#gumtree_list_locations) | **GET** /v1/gumtree/locations | List locations
[**gumtree_list_markets**](GumtreeApi.md#gumtree_list_markets) | **GET** /v1/gumtree/markets | List markets
[**gumtree_location_suggestions**](GumtreeApi.md#gumtree_location_suggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions
[**gumtree_search_listings**](GumtreeApi.md#gumtree_search_listings) | **GET** /v1/gumtree/search | Search listings
[**gumtree_search_suggestions**](GumtreeApi.md#gumtree_search_suggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions



## gumtree_get_listing

> serde_json::Value gumtree_get_listing(listing_id, market, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Get listing

Full listing — description, attributes, images, seller, similar listings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**listing_id** | **String** | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one) | [required] |
**market** | Option<**String**> | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. |  |[default to uk]
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


## gumtree_get_search_filters

> serde_json::Value gumtree_get_search_filters(category, location, query, filters, market, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Get search filters

Filters, sort orders and radius options for a category, with live counts.  Feed a `key` and a `value` back into `/search` as `filters=key:value`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category** | Option<**String**> | uk: category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs', 'bicycles'. au/za: numeric category id, e.g. '18320' (au cars) or '9077' (za cars). Use /categories to browse the tree. Default 'all'. |  |[default to all]
**location** | Option<**String**> | uk: location slug ('london'), town name or UK postcode ('SW1A 1AA'). au/za: numeric location id, e.g. '3003435' (au Sydney) or '3100003' (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. |  |
**query** | Option<**String**> | Optional keywords to scope the counts |  |
**filters** | Option<**String**> | za only: filters already applied (e.g. 'ma:toyota' to list Toyota models) |  |
**market** | Option<**String**> | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. |  |[default to uk]
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


## gumtree_get_seller_listings

> serde_json::Value gumtree_get_seller_listings(listing_id, page, market, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Get seller listings

Every live listing by the seller of the given listing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**listing_id** | **String** | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one) | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**market** | Option<**String**> | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. |  |[default to uk]
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


## gumtree_gumtree_scraper_health_check

> serde_json::Value gumtree_gumtree_scraper_health_check()
Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

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


## gumtree_gumtree_scraper_health_check_head

> serde_json::Value gumtree_gumtree_scraper_health_check_head()
Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

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


## gumtree_list_categories

> serde_json::Value gumtree_list_categories(parent_id, market, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
List categories

Browse Gumtree's category tree.  A node's `slug` (uk) or `id` (au/za) is the `/search` category.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**parent_id** | Option<**i32**> | Category id to list the children of (default: all) |  |
**market** | Option<**String**> | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. |  |[default to uk]
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


## gumtree_list_locations

> serde_json::Value gumtree_list_locations(parent_id, market, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
List locations

Browse Gumtree's location tree.  uk: UK -> nations -> counties -> towns. au: states -> regions -> areas, each with its live ad count. za: provinces -> towns.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**parent_id** | Option<**i32**> | Location id to list the children of (default: the whole country) |  |
**market** | Option<**String**> | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. |  |[default to uk]
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


## gumtree_list_markets

> serde_json::Value gumtree_list_markets(prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
List markets

The Gumtree sites this API covers (uk, au, za) with currency and id formats.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
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


## gumtree_location_suggestions

> serde_json::Value gumtree_location_suggestions(query, market, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Location suggestions

Resolve a place name or postcode to Gumtree location ids (uk: with coordinates).  The `id` (au/za) or `name` (uk) is what `/search` takes as `location`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Town, area or postcode prefix, e.g. 'manch' or 'SW1A' | [required] |
**market** | Option<**String**> | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. |  |[default to uk]
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


## gumtree_search_listings

> serde_json::Value gumtree_search_listings(query, category, location, distance, min_price, max_price, sort, seller_type, urgent_only, with_photos, filters, page, market, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Search listings

Search Gumtree listings in the UK, Australia or South Africa.  Up to 50 pages. Page size: uk 25, au 24 (plus up to 6 featured top ads), za 20.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | Option<**String**> | Search keywords, e.g. 'mountain bike' |  |
**category** | Option<**String**> | uk: category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs', 'bicycles'. au/za: numeric category id, e.g. '18320' (au cars) or '9077' (za cars). Use /categories to browse the tree. Default 'all'. |  |[default to all]
**location** | Option<**String**> | uk: location slug ('london'), town name or UK postcode ('SW1A 1AA'). au/za: numeric location id, e.g. '3003435' (au Sydney) or '3100003' (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. |  |
**distance** | Option<**f64**> | Radius around `location`: miles (uk) or km (au). Not offered by za. |  |
**min_price** | Option<**i32**> | Minimum price in the market's currency (uk: needs a category, not 'all') |  |
**max_price** | Option<**i32**> | Maximum price in the market's currency (uk: needs a category, not 'all') |  |
**sort** | Option<**String**> | Result ordering (default relevance). 'distance' needs uk, or au with a location. |  |
**seller_type** | Option<**String**> | uk/za: 'trade' covers dealers, agencies and recruiters. au: not supported — use a category filter such as 'cars.forsaleby_s:ownr'. |  |
**urgent_only** | Option<**bool**> | uk only: only ads marked urgent |  |[default to false]
**with_photos** | Option<**bool**> | uk only: only ads with photos |  |[default to false]
**filters** | Option<**String**> | Category-specific filters as comma-separated key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol,min_vehicle_mileage:10000' (uk), 'cars.carmake_s:toyota,cars.forsaleby_s:ownr' (au) or 'ma:toyota,fu:petrol,max_km:100000' (za). Range filters take min_<key>/max_<key>. Discover keys and values with /search/filters for the same market. |  |
**page** | Option<**i32**> |  |  |[default to 1]
**market** | Option<**String**> | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. |  |[default to uk]
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


## gumtree_search_suggestions

> serde_json::Value gumtree_search_suggestions(query, market, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Search suggestions

Gumtree search-box keyword suggestions with their categories.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial search term, e.g. 'iph' | [required] |
**market** | Option<**String**> | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. |  |[default to uk]
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

