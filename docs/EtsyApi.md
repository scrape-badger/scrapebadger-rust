# \EtsyApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**etsy_get_categories**](EtsyApi.md#etsy_get_categories) | **GET** /v1/etsy/categories | Get categories
[**etsy_get_listing_detail**](EtsyApi.md#etsy_get_listing_detail) | **GET** /v1/etsy/listings/{listing_id} | Get listing detail
[**etsy_get_listing_reviews**](EtsyApi.md#etsy_get_listing_reviews) | **GET** /v1/etsy/listings/{listing_id}/reviews | Get listing reviews
[**etsy_get_search_suggestions**](EtsyApi.md#etsy_get_search_suggestions) | **GET** /v1/etsy/autocomplete | Get search suggestions
[**etsy_get_shop_listings**](EtsyApi.md#etsy_get_shop_listings) | **GET** /v1/etsy/shops/{shop_name}/listings | Get shop listings
[**etsy_get_shop_profile**](EtsyApi.md#etsy_get_shop_profile) | **GET** /v1/etsy/shops/{shop_name} | Get shop profile
[**etsy_get_shop_reviews**](EtsyApi.md#etsy_get_shop_reviews) | **GET** /v1/etsy/shops/{shop_name}/reviews | Get shop reviews
[**etsy_search_listings**](EtsyApi.md#etsy_search_listings) | **GET** /v1/etsy/search | Search listings



## etsy_get_categories

> serde_json::Value etsy_get_categories(country, currency, language)
Get categories

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en-US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## etsy_get_listing_detail

> serde_json::Value etsy_get_listing_detail(listing_id, country, currency, language)
Get listing detail

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**listing_id** | **String** |  | [required] |
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en-US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## etsy_get_listing_reviews

> serde_json::Value etsy_get_listing_reviews(listing_id, page, sort, country, currency, language)
Get listing reviews

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**listing_id** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**sort** | Option<**String**> |  |  |[default to Relevancy]
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en-US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## etsy_get_search_suggestions

> serde_json::Value etsy_get_search_suggestions(query, country, currency, language)
Get search suggestions

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en-US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## etsy_get_shop_listings

> serde_json::Value etsy_get_shop_listings(shop_name, page, country, currency, language)
Get shop listings

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**shop_name** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en-US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## etsy_get_shop_profile

> serde_json::Value etsy_get_shop_profile(shop_name, country, currency, language)
Get shop profile

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**shop_name** | **String** |  | [required] |
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en-US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## etsy_get_shop_reviews

> serde_json::Value etsy_get_shop_reviews(shop_name, page, country, currency, language)
Get shop reviews

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**shop_name** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en-US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## etsy_search_listings

> serde_json::Value etsy_search_listings(query, page, country, currency, language, sort, min_price, max_price)
Search listings

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**country** | Option<**String**> |  |  |[default to US]
**currency** | Option<**String**> |  |  |[default to USD]
**language** | Option<**String**> |  |  |[default to en-US]
**sort** | Option<**String**> |  |  |[default to most_relevant]
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

