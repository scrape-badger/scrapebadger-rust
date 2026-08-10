# \DepopApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**depop_depop_scraper_health_check**](DepopApi.md#depop_depop_scraper_health_check) | **GET** /v1/depop/health | Depop scraper health check
[**depop_depop_scraper_health_check_head**](DepopApi.md#depop_depop_scraper_health_check_head) | **HEAD** /v1/depop/health | Depop scraper health check
[**depop_get_a_user_s_products**](DepopApi.md#depop_get_a_user_s_products) | **GET** /v1/depop/users/{username}/products | Get a user's products
[**depop_get_product_detail**](DepopApi.md#depop_get_product_detail) | **GET** /v1/depop/products/{product_id} | Get product detail
[**depop_get_shop_user_profile**](DepopApi.md#depop_get_shop_user_profile) | **GET** /v1/depop/users/{username} | Get shop/user profile
[**depop_list_markets**](DepopApi.md#depop_list_markets) | **GET** /v1/depop/markets | List markets
[**depop_search_depop_products**](DepopApi.md#depop_search_depop_products) | **GET** /v1/depop/search | Search Depop products



## depop_depop_scraper_health_check

> serde_json::Value depop_depop_scraper_health_check()
Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

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


## depop_depop_scraper_health_check_head

> serde_json::Value depop_depop_scraper_health_check_head()
Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

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


## depop_get_a_user_s_products

> serde_json::Value depop_get_a_user_s_products(username, market, per_page, cursor)
Get a user's products

A user's active listings (cursor-paginated).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**market** | Option<**String**> | Market code |  |[default to us]
**per_page** | Option<**i32**> |  |  |[default to 24]
**cursor** | Option<**String**> | Pagination cursor |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## depop_get_product_detail

> serde_json::Value depop_get_product_detail(product_id, market)
Get product detail

Full detail for a single product (by numeric id or slug).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** |  | [required] |
**market** | Option<**String**> | Market code |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## depop_get_shop_user_profile

> serde_json::Value depop_get_shop_user_profile(username, market)
Get shop/user profile

Public shop/user profile by username.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**market** | Option<**String**> | Market code |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## depop_list_markets

> serde_json::Value depop_list_markets()
List markets

List supported Depop markets (country + currency).

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


## depop_search_depop_products

> serde_json::Value depop_search_depop_products(query, market, per_page, cursor, price_min, price_max, brands, categories, sizes, conditions, gender, sort)
Search Depop products

Search the Depop catalog with filters (cursor-paginated).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search text, e.g. 'nike vintage' | [required] |
**market** | Option<**String**> | Market code (us, gb, au, it, fr, ...) |  |[default to us]
**per_page** | Option<**i32**> | Results per page |  |[default to 24]
**cursor** | Option<**String**> | Pagination cursor (from previous page) |  |
**price_min** | Option<**f64**> | Minimum price |  |
**price_max** | Option<**f64**> | Maximum price |  |
**brands** | Option<**String**> | Comma-separated brand IDs |  |
**categories** | Option<**String**> | Comma-separated category IDs |  |
**sizes** | Option<**String**> | Comma-separated size IDs |  |
**conditions** | Option<**String**> | Comma-separated condition slugs (brand_new, used_excellent, ...) |  |
**gender** | Option<**String**> | male | female |  |
**sort** | Option<**String**> | relevance | newlyListed | priceAscending | priceDescending |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

