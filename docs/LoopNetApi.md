# \LoopNetApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**loopnet_get_broker_profile**](LoopNetApi.md#loopnet_get_broker_profile) | **GET** /v1/loopnet/brokers/{slug}/{broker_id} | Get broker profile
[**loopnet_get_listing_detail**](LoopNetApi.md#loopnet_get_listing_detail) | **GET** /v1/loopnet/listings/{listing_id} | Get listing detail
[**loopnet_list_coverage_markets**](LoopNetApi.md#loopnet_list_coverage_markets) | **GET** /v1/loopnet/markets | List coverage markets
[**loopnet_list_property_types**](LoopNetApi.md#loopnet_list_property_types) | **GET** /v1/loopnet/property-types | List property types
[**loopnet_loopnet_scraper_health_check**](LoopNetApi.md#loopnet_loopnet_scraper_health_check) | **GET** /v1/loopnet/health | LoopNet scraper health check
[**loopnet_loopnet_scraper_health_check_head**](LoopNetApi.md#loopnet_loopnet_scraper_health_check_head) | **HEAD** /v1/loopnet/health | LoopNet scraper health check
[**loopnet_search_commercial_real_estate**](LoopNetApi.md#loopnet_search_commercial_real_estate) | **GET** /v1/loopnet/search | Search commercial real estate



## loopnet_get_broker_profile

> serde_json::Value loopnet_get_broker_profile(slug, broker_id, market)
Get broker profile

Get a LoopNet broker profile + their listings by slug + id.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**slug** | **String** |  | [required] |
**broker_id** | **String** |  | [required] |
**market** | Option<**String**> | us|ca|uk|fr|es |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## loopnet_get_listing_detail

> serde_json::Value loopnet_get_listing_detail(listing_id, market)
Get listing detail

Get a single LoopNet listing's full detail by its numeric id.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**listing_id** | **String** |  | [required] |
**market** | Option<**String**> | us|ca|uk|fr|es |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## loopnet_list_coverage_markets

> serde_json::Value loopnet_list_coverage_markets()
List coverage markets

List LoopNet coverage markets (US, CA, UK, FR, ES).

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


## loopnet_list_property_types

> serde_json::Value loopnet_list_property_types()
List property types

List LoopNet property-type facets accepted by /search.

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


## loopnet_loopnet_scraper_health_check

> serde_json::Value loopnet_loopnet_scraper_health_check()
LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

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


## loopnet_loopnet_scraper_health_check_head

> serde_json::Value loopnet_loopnet_scraper_health_check_head()
LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

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


## loopnet_search_commercial_real_estate

> serde_json::Value loopnet_search_commercial_real_estate(location, market, listing_type, property_type, page, min_price, max_price, price_type, min_size, max_size)
Search commercial real estate

Search LoopNet for-lease / for-sale / auction listings across all markets.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | **String** | City/state, ZIP, state code, or 'usa' | [required] |
**market** | Option<**String**> | us|ca|uk|fr|es |  |[default to us]
**listing_type** | Option<**String**> | for-lease|for-sale|auctions |  |[default to for-lease]
**property_type** | Option<**String**> | Slug from /property-types |  |
**page** | Option<**i32**> |  |  |[default to 1]
**min_price** | Option<**i32**> |  |  |
**max_price** | Option<**i32**> |  |  |
**price_type** | Option<**String**> | unit | sf | acre |  |
**min_size** | Option<**i32**> |  |  |
**max_size** | Option<**i32**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

