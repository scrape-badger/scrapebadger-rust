# \AliExpressApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**aliexpress_get_category_navigation**](AliExpressApi.md#aliexpress_get_category_navigation) | **GET** /v1/aliexpress/categories | Get category navigation
[**aliexpress_get_product_detail**](AliExpressApi.md#aliexpress_get_product_detail) | **GET** /v1/aliexpress/products/{product_id} | Get product detail
[**aliexpress_get_product_reviews**](AliExpressApi.md#aliexpress_get_product_reviews) | **GET** /v1/aliexpress/products/{product_id}/reviews | Get product reviews
[**aliexpress_get_search_suggestions**](AliExpressApi.md#aliexpress_get_search_suggestions) | **GET** /v1/aliexpress/autocomplete | Get search suggestions
[**aliexpress_get_store_product_categories**](AliExpressApi.md#aliexpress_get_store_product_categories) | **GET** /v1/aliexpress/stores/{store_id}/categories | Get store product categories
[**aliexpress_get_store_products**](AliExpressApi.md#aliexpress_get_store_products) | **GET** /v1/aliexpress/stores/{store_id}/products | Get store products
[**aliexpress_get_store_profile**](AliExpressApi.md#aliexpress_get_store_profile) | **GET** /v1/aliexpress/stores/{store_id} | Get store profile
[**aliexpress_search_products**](AliExpressApi.md#aliexpress_search_products) | **GET** /v1/aliexpress/search | Search products



## aliexpress_get_category_navigation

> serde_json::Value aliexpress_get_category_navigation()
Get category navigation

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


## aliexpress_get_product_detail

> serde_json::Value aliexpress_get_product_detail(product_id, country, currency, language)
Get product detail

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** |  | [required] |
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en_US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## aliexpress_get_product_reviews

> serde_json::Value aliexpress_get_product_reviews(product_id, page, page_size, sort)
Get product reviews

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 10]
**sort** | Option<**String**> |  |  |[default to complex_default]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## aliexpress_get_search_suggestions

> serde_json::Value aliexpress_get_search_suggestions(query, country, language)
Get search suggestions

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**country** | Option<**String**> |  |  |[default to US]
**language** | Option<**String**> |  |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## aliexpress_get_store_product_categories

> serde_json::Value aliexpress_get_store_product_categories(store_id, country)
Get store product categories

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**store_id** | **String** |  | [required] |
**country** | Option<**String**> |  |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## aliexpress_get_store_products

> serde_json::Value aliexpress_get_store_products(store_id, page, page_size, country, currency, language, query, sort)
Get store products

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**store_id** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 24]
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en]
**query** | Option<**String**> |  |  |[default to ]
**sort** | Option<**String**> |  |  |[default to bestmatch_sort]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## aliexpress_get_store_profile

> serde_json::Value aliexpress_get_store_profile(store_id, country, currency, language)
Get store profile

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**store_id** | **String** |  | [required] |
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## aliexpress_search_products

> serde_json::Value aliexpress_search_products(query, page, country, currency, language, sort, min_price, max_price)
Search products

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en]
**sort** | Option<**String**> |  |  |[default to default]
**min_price** | Option<**f64**> |  |  |
**max_price** | Option<**f64**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

