# \TargetApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**target_browse_a_category**](TargetApi.md#target_browse_a_category) | **GET** /v1/target/category | Browse a category
[**target_find_nearby_stores**](TargetApi.md#target_find_nearby_stores) | **GET** /v1/target/stores | Find nearby stores
[**target_get_categories**](TargetApi.md#target_get_categories) | **GET** /v1/target/categories | Get categories
[**target_get_product_availability**](TargetApi.md#target_get_product_availability) | **GET** /v1/target/products/{tcin}/availability | Get product availability
[**target_get_product_detail**](TargetApi.md#target_get_product_detail) | **GET** /v1/target/products/{tcin} | Get product detail
[**target_get_product_questions**](TargetApi.md#target_get_product_questions) | **GET** /v1/target/products/{tcin}/questions | Get product questions
[**target_get_product_reviews**](TargetApi.md#target_get_product_reviews) | **GET** /v1/target/products/{tcin}/reviews | Get product reviews
[**target_get_search_suggestions**](TargetApi.md#target_get_search_suggestions) | **GET** /v1/target/autocomplete | Get search suggestions
[**target_get_store_detail**](TargetApi.md#target_get_store_detail) | **GET** /v1/target/stores/{store_id} | Get store detail
[**target_list_supported_markets**](TargetApi.md#target_list_supported_markets) | **GET** /v1/target/markets | List supported markets
[**target_search_products**](TargetApi.md#target_search_products) | **GET** /v1/target/search | Search products



## target_browse_a_category

> serde_json::Value target_browse_a_category(category_id, page, page_size, store_id, zip_code)
Browse a category

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category_id** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 24]
**store_id** | Option<**String**> |  |  |[default to 1375]
**zip_code** | Option<**String**> |  |  |[default to 55403]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## target_find_nearby_stores

> serde_json::Value target_find_nearby_stores(zip_code, limit)
Find nearby stores

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**zip_code** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## target_get_categories

> serde_json::Value target_get_categories(category_id)
Get categories

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category_id** | Option<**String**> |  |  |[default to 5xtly]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## target_get_product_availability

> serde_json::Value target_get_product_availability(tcin, zip_code, limit)
Get product availability

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tcin** | **String** |  | [required] |
**zip_code** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## target_get_product_detail

> serde_json::Value target_get_product_detail(tcin, store_id, zip_code)
Get product detail

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tcin** | **String** |  | [required] |
**store_id** | Option<**String**> |  |  |[default to 1375]
**zip_code** | Option<**String**> |  |  |[default to 55403]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## target_get_product_questions

> serde_json::Value target_get_product_questions(tcin, page, page_size)
Get product questions

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tcin** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## target_get_product_reviews

> serde_json::Value target_get_product_reviews(tcin, page, page_size, sort)
Get product reviews

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tcin** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 10]
**sort** | Option<**String**> |  |  |[default to most_recent]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## target_get_search_suggestions

> serde_json::Value target_get_search_suggestions(query)
Get search suggestions

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## target_get_store_detail

> serde_json::Value target_get_store_detail(store_id)
Get store detail

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**store_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## target_list_supported_markets

> serde_json::Value target_list_supported_markets()
List supported markets

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


## target_search_products

> serde_json::Value target_search_products(query, page, page_size, store_id, zip_code, sort)
Search products

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 24]
**store_id** | Option<**String**> |  |  |[default to 1375]
**zip_code** | Option<**String**> |  |  |[default to 55403]
**sort** | Option<**String**> |  |  |[default to relevance]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

