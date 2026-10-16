# \BestBuyApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bestbuy_browse_a_category**](BestBuyApi.md#bestbuy_browse_a_category) | **GET** /v1/bestbuy/category | Browse a category
[**bestbuy_get_categories**](BestBuyApi.md#bestbuy_get_categories) | **GET** /v1/bestbuy/categories | Get categories
[**bestbuy_get_laptop_and_computer_deals**](BestBuyApi.md#bestbuy_get_laptop_and_computer_deals) | **GET** /v1/bestbuy/deals | Get laptop and computer deals
[**bestbuy_get_product_availability**](BestBuyApi.md#bestbuy_get_product_availability) | **GET** /v1/bestbuy/products/{sku}/availability | Get product availability
[**bestbuy_get_product_detail**](BestBuyApi.md#bestbuy_get_product_detail) | **GET** /v1/bestbuy/products/{sku} | Get product detail
[**bestbuy_get_product_questions**](BestBuyApi.md#bestbuy_get_product_questions) | **GET** /v1/bestbuy/products/{sku}/questions | Get product questions
[**bestbuy_get_product_reviews**](BestBuyApi.md#bestbuy_get_product_reviews) | **GET** /v1/bestbuy/products/{sku}/reviews | Get product reviews
[**bestbuy_get_search_suggestions**](BestBuyApi.md#bestbuy_get_search_suggestions) | **GET** /v1/bestbuy/autocomplete | Get search suggestions
[**bestbuy_list_supported_markets**](BestBuyApi.md#bestbuy_list_supported_markets) | **GET** /v1/bestbuy/markets | List supported markets
[**bestbuy_search_products**](BestBuyApi.md#bestbuy_search_products) | **GET** /v1/bestbuy/search | Search products



## bestbuy_browse_a_category

> serde_json::Value bestbuy_browse_a_category(category_id, page)
Browse a category

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category_id** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bestbuy_get_categories

> serde_json::Value bestbuy_get_categories(query)
Get categories

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | Option<**String**> |  |  |[default to laptop]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bestbuy_get_laptop_and_computer_deals

> serde_json::Value bestbuy_get_laptop_and_computer_deals(page)
Get laptop and computer deals

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bestbuy_get_product_availability

> serde_json::Value bestbuy_get_product_availability(sku, zip_code, store_id)
Get product availability

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sku** | **String** |  | [required] |
**zip_code** | **String** |  | [required] |
**store_id** | Option<**String**> |  |  |[default to 7]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bestbuy_get_product_detail

> serde_json::Value bestbuy_get_product_detail(sku)
Get product detail

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sku** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bestbuy_get_product_questions

> serde_json::Value bestbuy_get_product_questions(sku, page, page_size, query)
Get product questions

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sku** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 10]
**query** | Option<**String**> |  |  |[default to ]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bestbuy_get_product_reviews

> serde_json::Value bestbuy_get_product_reviews(sku, page, page_size, sort)
Get product reviews

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sku** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 10]
**sort** | Option<**String**> |  |  |[default to MOST_RECENT]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bestbuy_get_search_suggestions

> serde_json::Value bestbuy_get_search_suggestions(query)
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


## bestbuy_list_supported_markets

> serde_json::Value bestbuy_list_supported_markets()
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


## bestbuy_search_products

> serde_json::Value bestbuy_search_products(query, page, sort)
Search products

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**sort** | Option<**String**> |  |  |[default to best_match]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

