# \LeboncoinApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**leboncoin_get_a_seller_s_ads**](LeboncoinApi.md#leboncoin_get_a_seller_s_ads) | **GET** /v1/leboncoin/sellers/{user_id}/listings | Get a seller's ads
[**leboncoin_get_ad_detail**](LeboncoinApi.md#leboncoin_get_ad_detail) | **GET** /v1/leboncoin/ads/{list_id} | Get ad detail
[**leboncoin_get_seller_profile**](LeboncoinApi.md#leboncoin_get_seller_profile) | **GET** /v1/leboncoin/sellers/{user_id} | Get seller profile
[**leboncoin_get_similar_ads**](LeboncoinApi.md#leboncoin_get_similar_ads) | **GET** /v1/leboncoin/ads/{list_id}/similar | Get similar ads
[**leboncoin_leboncoin_scraper_health_check**](LeboncoinApi.md#leboncoin_leboncoin_scraper_health_check) | **GET** /v1/leboncoin/health | Leboncoin scraper health check
[**leboncoin_leboncoin_scraper_health_check_head**](LeboncoinApi.md#leboncoin_leboncoin_scraper_health_check_head) | **HEAD** /v1/leboncoin/health | Leboncoin scraper health check
[**leboncoin_list_categories**](LeboncoinApi.md#leboncoin_list_categories) | **GET** /v1/leboncoin/categories | List categories
[**leboncoin_list_departments**](LeboncoinApi.md#leboncoin_list_departments) | **GET** /v1/leboncoin/departments | List departments
[**leboncoin_list_markets**](LeboncoinApi.md#leboncoin_list_markets) | **GET** /v1/leboncoin/markets | List markets
[**leboncoin_list_regions**](LeboncoinApi.md#leboncoin_list_regions) | **GET** /v1/leboncoin/regions | List regions
[**leboncoin_location_autocomplete**](LeboncoinApi.md#leboncoin_location_autocomplete) | **GET** /v1/leboncoin/locations/search | Location autocomplete
[**leboncoin_search_leboncoin_ads**](LeboncoinApi.md#leboncoin_search_leboncoin_ads) | **GET** /v1/leboncoin/search | Search Leboncoin ads



## leboncoin_get_a_seller_s_ads

> serde_json::Value leboncoin_get_a_seller_s_ads(user_id, page, limit)
Get a seller's ads

A seller's active ads.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**limit** | Option<**i32**> |  |  |[default to 35]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## leboncoin_get_ad_detail

> serde_json::Value leboncoin_get_ad_detail(list_id)
Get ad detail

Full detail for a Leboncoin ad.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**list_id** | **i32** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## leboncoin_get_seller_profile

> serde_json::Value leboncoin_get_seller_profile(user_id)
Get seller profile

Public seller/pro-store profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## leboncoin_get_similar_ads

> serde_json::Value leboncoin_get_similar_ads(list_id, limit)
Get similar ads

Ads Leboncoin surfaces as similar to the given ad.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**list_id** | **i32** |  | [required] |
**limit** | Option<**i32**> |  |  |[default to 20]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## leboncoin_leboncoin_scraper_health_check

> serde_json::Value leboncoin_leboncoin_scraper_health_check()
Leboncoin scraper health check

Check health of the Leboncoin scraper service (accepts HEAD).

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


## leboncoin_leboncoin_scraper_health_check_head

> serde_json::Value leboncoin_leboncoin_scraper_health_check_head()
Leboncoin scraper health check

Check health of the Leboncoin scraper service (accepts HEAD).

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


## leboncoin_list_categories

> serde_json::Value leboncoin_list_categories()
List categories

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


## leboncoin_list_departments

> serde_json::Value leboncoin_list_departments(region_id)
List departments

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**region_id** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## leboncoin_list_markets

> serde_json::Value leboncoin_list_markets()
List markets

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


## leboncoin_list_regions

> serde_json::Value leboncoin_list_regions()
List regions

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


## leboncoin_location_autocomplete

> serde_json::Value leboncoin_location_autocomplete(q)
Location autocomplete

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Place name | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## leboncoin_search_leboncoin_ads

> serde_json::Value leboncoin_search_leboncoin_ads(text, category, region_id, department_id, city, zipcode, price_min, price_max, owner_type, ad_type, sort, page, limit)
Search Leboncoin ads

Search Leboncoin classifieds (France; scope by region/department/city).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**text** | Option<**String**> | Free-text query |  |
**category** | Option<**String**> | Category id (see /categories) |  |
**region_id** | Option<**String**> | Region id (see /regions) |  |
**department_id** | Option<**String**> | Department id, e.g. 75 |  |
**city** | Option<**String**> |  |  |
**zipcode** | Option<**String**> |  |  |
**price_min** | Option<**i32**> |  |  |
**price_max** | Option<**i32**> |  |  |
**owner_type** | Option<**String**> | all | pro | private |  |[default to all]
**ad_type** | Option<**String**> | offer | demand |  |[default to offer]
**sort** | Option<**String**> | relevance|newest|oldest|price_low|price_high |  |[default to relevance]
**page** | Option<**i32**> |  |  |[default to 1]
**limit** | Option<**i32**> |  |  |[default to 35]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

