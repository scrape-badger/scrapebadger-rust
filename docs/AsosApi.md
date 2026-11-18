# \AsosApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**asos_get_product_detail**](AsosApi.md#asos_get_product_detail) | **GET** /v1/asos/products/{product_id} | Get product detail
[**asos_get_stock_and_prices**](AsosApi.md#asos_get_stock_and_prices) | **GET** /v1/asos/stock-price | Get stock and prices
[**asos_list_categories**](AsosApi.md#asos_list_categories) | **GET** /v1/asos/categories | List categories
[**asos_list_markets**](AsosApi.md#asos_list_markets) | **GET** /v1/asos/markets | List markets
[**asos_list_search_filters**](AsosApi.md#asos_list_search_filters) | **GET** /v1/asos/filters | List search filters
[**asos_search_products**](AsosApi.md#asos_search_products) | **GET** /v1/asos/search | Search products
[**asos_search_suggestions**](AsosApi.md#asos_search_suggestions) | **GET** /v1/asos/autocomplete | Search suggestions



## asos_get_product_detail

> models::ProductResponse asos_get_product_detail(product_id, market, store, country, currency, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Get product detail

Product, live per-size stock and price, images, descriptions, reviews and breadcrumbs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **i32** |  | [required] |
**market** | Option<**String**> | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl |  |[default to uk]
**store** | Option<**String**> | Override store, e.g. COM or US |  |
**country** | Option<**String**> | ISO country override |  |
**currency** | Option<**String**> | Currency override |  |
**language** | Option<**String**> | Locale override, e.g. en-GB |  |
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**models::ProductResponse**](ProductResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## asos_get_stock_and_prices

> models::StockResponse asos_get_stock_and_prices(product_ids, market, store, country, currency, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Get stock and prices

Refresh product and variant stock/prices; reports missing product ids explicitly.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_ids** | **String** | 1–50 comma-separated product ids | [required] |
**market** | Option<**String**> | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl |  |[default to uk]
**store** | Option<**String**> | Override store, e.g. COM or US |  |
**country** | Option<**String**> | ISO country override |  |
**currency** | Option<**String**> | Currency override |  |
**language** | Option<**String**> | Locale override, e.g. en-GB |  |
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**models::StockResponse**](StockResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## asos_list_categories

> serde_json::Value asos_list_categories(gender, market, store, country, currency, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
List categories

Full nested navigation with category ids, names, images and links.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**gender** | Option<**String**> |  |  |[default to men]
**market** | Option<**String**> | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl |  |[default to uk]
**store** | Option<**String**> | Override store, e.g. COM or US |  |
**country** | Option<**String**> | ISO country override |  |
**currency** | Option<**String**> | Currency override |  |
**language** | Option<**String**> | Locale override, e.g. en-GB |  |
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


## asos_list_markets

> serde_json::Value asos_list_markets(prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
List markets

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


## asos_list_search_filters

> serde_json::Value asos_list_search_filters(query, category_id, market, store, country, currency, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
List search filters

Facet ids, labels, option counts and selections for a query or category.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | Option<**String**> |  |  |
**category_id** | Option<**i32**> |  |  |
**market** | Option<**String**> | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl |  |[default to uk]
**store** | Option<**String**> | Override store, e.g. COM or US |  |
**country** | Option<**String**> | ISO country override |  |
**currency** | Option<**String**> | Currency override |  |
**language** | Option<**String**> | Locale override, e.g. en-GB |  |
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


## asos_search_products

> models::PortalApiRoutersV1AsosSearchResponse asos_search_products(query, category_id, offset, limit, sort, brand, colour, size, min_price, max_price, market, store, country, currency, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Search products

Search by query, category_id, or both. Includes price, images and filter facets.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | Option<**String**> | Keyword, e.g. shoes |  |
**category_id** | Option<**i32**> | Category id from navigation |  |
**offset** | Option<**i32**> |  |  |[default to 0]
**limit** | Option<**i32**> |  |  |[default to 48]
**sort** | Option<**String**> |  |  |[default to recommended]
**brand** | Option<**String**> | Comma-separated brand facet ids |  |
**colour** | Option<**String**> | Comma-separated colour facet ids |  |
**size** | Option<**String**> | Comma-separated size facet ids |  |
**min_price** | Option<**f64**> |  |  |
**max_price** | Option<**f64**> |  |  |
**market** | Option<**String**> | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl |  |[default to uk]
**store** | Option<**String**> | Override store, e.g. COM or US |  |
**country** | Option<**String**> | ISO country override |  |
**currency** | Option<**String**> | Currency override |  |
**language** | Option<**String**> | Locale override, e.g. en-GB |  |
**prefer** | Option<**String**> | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. |  |
**x_callback_url** | Option<**String**> | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. |  |
**idempotency_key** | Option<**String**> | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. |  |
**r#async** | Option<**bool**> | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. |  |
**async_wait** | Option<**i32**> | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. |  |
**callback_url** | Option<**String**> | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. |  |
**idempotency_key2** | Option<**String**> | Query form of `Idempotency-Key`. Not sent to the scraper. |  |

### Return type

[**models::PortalApiRoutersV1AsosSearchResponse**](portal_api__routers__v1_asos__SearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## asos_search_suggestions

> serde_json::Value asos_search_suggestions(query, market, store, country, currency, language, prefer, x_callback_url, idempotency_key, r#async, async_wait, callback_url, idempotency_key2)
Search suggestions

Search suggestions with result counts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**market** | Option<**String**> | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl |  |[default to uk]
**store** | Option<**String**> | Override store, e.g. COM or US |  |
**country** | Option<**String**> | ISO country override |  |
**currency** | Option<**String**> | Currency override |  |
**language** | Option<**String**> | Locale override, e.g. en-GB |  |
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

