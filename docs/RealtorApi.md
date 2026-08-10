# \RealtorApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**realtor_get_full_property_detail**](RealtorApi.md#realtor_get_full_property_detail) | **GET** /v1/realtor/properties/{property_id} | Get full property detail
[**realtor_list_markets**](RealtorApi.md#realtor_list_markets) | **GET** /v1/realtor/markets | List markets
[**realtor_location_autocomplete**](RealtorApi.md#realtor_location_autocomplete) | **GET** /v1/realtor/autocomplete | Location autocomplete
[**realtor_realtor_scraper_health_check**](RealtorApi.md#realtor_realtor_scraper_health_check) | **GET** /v1/realtor/health | Realtor scraper health check
[**realtor_realtor_scraper_health_check_head**](RealtorApi.md#realtor_realtor_scraper_health_check_head) | **HEAD** /v1/realtor/health | Realtor scraper health check
[**realtor_search_property_listings**](RealtorApi.md#realtor_search_property_listings) | **GET** /v1/realtor/search | Search property listings



## realtor_get_full_property_detail

> serde_json::Value realtor_get_full_property_detail(property_id, market)
Get full property detail

Full listing detail: features, tax & price history, schools, photos, agents.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**property_id** | **String** |  | [required] |
**market** | Option<**String**> | us (realtor.com) | ca (realtor.ca) |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## realtor_list_markets

> serde_json::Value realtor_list_markets()
List markets

List supported Realtor markets (US = realtor.com, CA = realtor.ca).

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


## realtor_location_autocomplete

> serde_json::Value realtor_location_autocomplete(query, market, limit)
Location autocomplete

Resolve a location query into candidate places to feed /search.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Freetext location (city, ZIP/postal, address…) | [required] |
**market** | Option<**String**> | us (realtor.com) | ca (realtor.ca) |  |[default to us]
**limit** | Option<**i32**> |  |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## realtor_realtor_scraper_health_check

> serde_json::Value realtor_realtor_scraper_health_check()
Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

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


## realtor_realtor_scraper_health_check_head

> serde_json::Value realtor_realtor_scraper_health_check_head()
Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

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


## realtor_search_property_listings

> serde_json::Value realtor_search_property_listings(location, market, status, price_min, price_max, beds_min, baths_min, sqft_min, sqft_max, property_type, sort, page, limit, lat_min, lat_max, lng_min, lng_max)
Search property listings

Search for-sale/for-rent/sold listings with rich filters.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | Option<**String**> | 'Austin, TX', a ZIP, 'Toronto, ON'… |  |
**market** | Option<**String**> | us (realtor.com) | ca (realtor.ca) |  |[default to us]
**status** | Option<**String**> | for_sale | for_rent | sold | pending |  |[default to for_sale]
**price_min** | Option<**f64**> |  |  |
**price_max** | Option<**f64**> |  |  |
**beds_min** | Option<**i32**> |  |  |
**baths_min** | Option<**i32**> |  |  |
**sqft_min** | Option<**i32**> | US only |  |
**sqft_max** | Option<**i32**> | US only |  |
**property_type** | Option<**String**> | US only, CSV of property types |  |
**sort** | Option<**String**> | relevant | newest | price_low | price_high | photo_count |  |[default to relevant]
**page** | Option<**i32**> |  |  |[default to 1]
**limit** | Option<**i32**> |  |  |
**lat_min** | Option<**f64**> | CA bbox south |  |
**lat_max** | Option<**f64**> | CA bbox north |  |
**lng_min** | Option<**f64**> | CA bbox west |  |
**lng_max** | Option<**f64**> | CA bbox east |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

