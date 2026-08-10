# \ImmobiliareApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**immobiliare_get_agency_profile**](ImmobiliareApi.md#immobiliare_get_agency_profile) | **GET** /v1/immobiliare/agencies/{agency_id} | Get agency profile
[**immobiliare_get_an_agency_s_listings**](ImmobiliareApi.md#immobiliare_get_an_agency_s_listings) | **GET** /v1/immobiliare/agencies/{agency_id}/listings | Get an agency's listings
[**immobiliare_get_listing_detail**](ImmobiliareApi.md#immobiliare_get_listing_detail) | **GET** /v1/immobiliare/listings/{listing_id} | Get listing detail
[**immobiliare_immobiliare_scraper_health_check**](ImmobiliareApi.md#immobiliare_immobiliare_scraper_health_check) | **GET** /v1/immobiliare/health | Immobiliare scraper health check
[**immobiliare_immobiliare_scraper_health_check_head**](ImmobiliareApi.md#immobiliare_immobiliare_scraper_health_check_head) | **HEAD** /v1/immobiliare/health | Immobiliare scraper health check
[**immobiliare_list_filter_enums**](ImmobiliareApi.md#immobiliare_list_filter_enums) | **GET** /v1/immobiliare/reference | List filter enums
[**immobiliare_list_markets**](ImmobiliareApi.md#immobiliare_list_markets) | **GET** /v1/immobiliare/markets | List markets
[**immobiliare_location_autocomplete**](ImmobiliareApi.md#immobiliare_location_autocomplete) | **GET** /v1/immobiliare/autocomplete | Location autocomplete
[**immobiliare_price_m_time_series**](ImmobiliareApi.md#immobiliare_price_m_time_series) | **GET** /v1/immobiliare/market-insights/prices | Price €/m² time series
[**immobiliare_search_listings**](ImmobiliareApi.md#immobiliare_search_listings) | **GET** /v1/immobiliare/search | Search listings



## immobiliare_get_agency_profile

> serde_json::Value immobiliare_get_agency_profile(agency_id, market)
Get agency profile

Public agency/advertiser profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**agency_id** | **i32** |  | [required] |
**market** | Option<**String**> | it | es | gr | lu |  |[default to it]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## immobiliare_get_an_agency_s_listings

> serde_json::Value immobiliare_get_an_agency_s_listings(agency_id, market, contract, page)
Get an agency's listings

An agency's active listings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**agency_id** | **i32** |  | [required] |
**market** | Option<**String**> | it | es | gr | lu |  |[default to it]
**contract** | Option<**String**> | sale | rent |  |[default to sale]
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## immobiliare_get_listing_detail

> serde_json::Value immobiliare_get_listing_detail(listing_id, market)
Get listing detail

Full detail for a single listing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**listing_id** | **i32** |  | [required] |
**market** | Option<**String**> | it | es | gr | lu |  |[default to it]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## immobiliare_immobiliare_scraper_health_check

> serde_json::Value immobiliare_immobiliare_scraper_health_check()
Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

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


## immobiliare_immobiliare_scraper_health_check_head

> serde_json::Value immobiliare_immobiliare_scraper_health_check_head()
Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

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


## immobiliare_list_filter_enums

> serde_json::Value immobiliare_list_filter_enums()
List filter enums

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


## immobiliare_list_markets

> serde_json::Value immobiliare_list_markets()
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


## immobiliare_location_autocomplete

> serde_json::Value immobiliare_location_autocomplete(query, market)
Location autocomplete

Resolve a place name to region/province/city ids usable in search.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Free-text place name, e.g. 'Milano' | [required] |
**market** | Option<**String**> | it | es | gr | lu |  |[default to it]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## immobiliare_price_m_time_series

> serde_json::Value immobiliare_price_m_time_series(region_id, market, province_id, city_id, contract)
Price €/m² time series

Historical €/m² price statistics for an area.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**region_id** | **String** | Region id, e.g. 'lom' | [required] |
**market** | Option<**String**> | it | es | gr | lu |  |[default to it]
**province_id** | Option<**String**> | Province id, e.g. 'MI' |  |
**city_id** | Option<**String**> | City id (idComune) |  |
**contract** | Option<**String**> | sale | rent |  |[default to sale]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## immobiliare_search_listings

> serde_json::Value immobiliare_search_listings(market, location, region_id, province_id, city_id, contract, category, price_min, price_max, surface_min, surface_max, rooms_min, rooms_max, bathrooms_min, sort, page)
Search listings

Search Immobiliare-group listings (scope by location + contract + filters).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**market** | Option<**String**> | it | es | gr | lu |  |[default to it]
**location** | Option<**String**> | Free-text place (auto-resolved) |  |
**region_id** | Option<**String**> | fkRegione (from /autocomplete) |  |
**province_id** | Option<**String**> | idProvincia (from /autocomplete) |  |
**city_id** | Option<**String**> | idComune (from /autocomplete) |  |
**contract** | Option<**String**> | sale | rent |  |[default to sale]
**category** | Option<**String**> | see /reference |  |[default to residential]
**price_min** | Option<**i32**> |  |  |
**price_max** | Option<**i32**> |  |  |
**surface_min** | Option<**i32**> |  |  |
**surface_max** | Option<**i32**> |  |  |
**rooms_min** | Option<**i32**> |  |  |
**rooms_max** | Option<**i32**> |  |  |
**bathrooms_min** | Option<**i32**> |  |  |
**sort** | Option<**String**> | see /reference |  |[default to relevance]
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

