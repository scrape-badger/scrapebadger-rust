# \VintedApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**vinted_get_item_details**](VintedApi.md#vinted_get_item_details) | **GET** /v1/vinted/items/{item_id} | Get item details
[**vinted_get_user_profile**](VintedApi.md#vinted_get_user_profile) | **GET** /v1/vinted/users/{user_id} | Get user profile
[**vinted_get_user_s_listed_items**](VintedApi.md#vinted_get_user_s_listed_items) | **GET** /v1/vinted/users/{user_id}/items | Get user's listed items
[**vinted_list_colors**](VintedApi.md#vinted_list_colors) | **GET** /v1/vinted/colors | List colors
[**vinted_list_item_conditions**](VintedApi.md#vinted_list_item_conditions) | **GET** /v1/vinted/statuses | List item conditions
[**vinted_list_markets**](VintedApi.md#vinted_list_markets) | **GET** /v1/vinted/markets | List markets
[**vinted_search_brands**](VintedApi.md#vinted_search_brands) | **GET** /v1/vinted/brands | Search brands
[**vinted_search_vinted_items**](VintedApi.md#vinted_search_vinted_items) | **GET** /v1/vinted/search | Search Vinted items
[**vinted_vinted_scraper_health_check**](VintedApi.md#vinted_vinted_scraper_health_check) | **GET** /v1/vinted/health | Vinted scraper health check
[**vinted_vinted_scraper_health_check_head**](VintedApi.md#vinted_vinted_scraper_health_check_head) | **HEAD** /v1/vinted/health | Vinted scraper health check



## vinted_get_item_details

> serde_json::Value vinted_get_item_details(item_id, market)
Get item details

Get detailed information about a Vinted item.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**item_id** | **i32** |  | [required] |
**market** | Option<**String**> |  |  |[default to fr]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## vinted_get_user_profile

> serde_json::Value vinted_get_user_profile(user_id, market)
Get user profile

Get a Vinted user's profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **i32** |  | [required] |
**market** | Option<**String**> |  |  |[default to fr]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## vinted_get_user_s_listed_items

> serde_json::Value vinted_get_user_s_listed_items(user_id, market, page, per_page)
Get user's listed items

Get items listed by a Vinted user.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **i32** |  | [required] |
**market** | Option<**String**> |  |  |[default to fr]
**page** | Option<**i32**> |  |  |[default to 1]
**per_page** | Option<**i32**> |  |  |[default to 20]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## vinted_list_colors

> serde_json::Value vinted_list_colors(market)
List colors

Get available Vinted colors for filtering.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**market** | Option<**String**> |  |  |[default to fr]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## vinted_list_item_conditions

> serde_json::Value vinted_list_item_conditions(market)
List item conditions

Get available item condition statuses.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**market** | Option<**String**> |  |  |[default to fr]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## vinted_list_markets

> serde_json::Value vinted_list_markets()
List markets

List all supported Vinted markets.

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


## vinted_search_brands

> serde_json::Value vinted_search_brands(keyword, market)
Search brands

Search Vinted brands.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**keyword** | **String** | Brand search keyword | [required] |
**market** | Option<**String**> |  |  |[default to fr]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## vinted_search_vinted_items

> serde_json::Value vinted_search_vinted_items(query, market, seller_country, page, per_page, price_from, price_to, brand_ids, catalog_ids, color_ids, status_ids, order)
Search Vinted items

Search Vinted catalog items with filters.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search text | [required] |
**market** | Option<**String**> | Market code |  |[default to fr]
**seller_country** | Option<**String**> | Filter to items whose seller is physically located in one of these comma-separated ISO-2 country codes (e.g. 'fr' or 'fr,be'). Market domains federate cross-border EU listings and Vinted has no native country filter, so each item is enriched with its seller's country and non-matching ones are dropped. Adds 1 credit per uncached seller looked up (cached for 7 days). |  |
**page** | Option<**i32**> |  |  |[default to 1]
**per_page** | Option<**i32**> |  |  |[default to 20]
**price_from** | Option<**f64**> |  |  |
**price_to** | Option<**f64**> |  |  |
**brand_ids** | Option<**String**> |  |  |
**catalog_ids** | Option<**String**> | Comma-separated Vinted catalog (category) IDs to restrict the search to, e.g. '1904' or '1904,79'. Vinted applies this before searching, so pagination totals reflect the filtered set. A catalog ID is the `catalog[]` value in a Vinted category URL (vinted.fr/catalog?catalog[]=1904). |  |
**color_ids** | Option<**String**> | Comma-separated color IDs |  |
**status_ids** | Option<**String**> | Comma-separated condition/status IDs |  |
**order** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## vinted_vinted_scraper_health_check

> serde_json::Value vinted_vinted_scraper_health_check()
Vinted scraper health check

Check health of the Vinted scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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


## vinted_vinted_scraper_health_check_head

> serde_json::Value vinted_vinted_scraper_health_check_head()
Vinted scraper health check

Check health of the Vinted scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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

