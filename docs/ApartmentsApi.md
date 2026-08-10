# \ApartmentsApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apartments_apartments_scraper_health_check**](ApartmentsApi.md#apartments_apartments_scraper_health_check) | **GET** /v1/apartments/health | Apartments scraper health check
[**apartments_apartments_scraper_health_check_head**](ApartmentsApi.md#apartments_apartments_scraper_health_check_head) | **HEAD** /v1/apartments/health | Apartments scraper health check
[**apartments_get_property_detail_by_slug_id**](ApartmentsApi.md#apartments_get_property_detail_by_slug_id) | **GET** /v1/apartments/properties/{slug}/{property_id} | Get property detail by slug + id
[**apartments_get_property_detail_by_url**](ApartmentsApi.md#apartments_get_property_detail_by_url) | **GET** /v1/apartments/property | Get property detail by URL
[**apartments_search_rental_listings**](ApartmentsApi.md#apartments_search_rental_listings) | **GET** /v1/apartments/search | Search rental listings



## apartments_apartments_scraper_health_check

> serde_json::Value apartments_apartments_scraper_health_check()
Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

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


## apartments_apartments_scraper_health_check_head

> serde_json::Value apartments_apartments_scraper_health_check_head()
Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

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


## apartments_get_property_detail_by_slug_id

> serde_json::Value apartments_get_property_detail_by_slug_id(slug, property_id)
Get property detail by slug + id

Get a property by its SEO slug and 7-character listing id.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**slug** | **String** |  | [required] |
**property_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## apartments_get_property_detail_by_url

> serde_json::Value apartments_get_property_detail_by_url(url)
Get property detail by URL

Get an apartments.com property with full per-unit pricing and availability.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/ | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## apartments_search_rental_listings

> serde_json::Value apartments_search_rental_listings(location, page, beds, min_price, max_price)
Search rental listings

Search apartments.com for rental properties. 40 cards per page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | **String** | apartments.com location slug, e.g. 'kansas-city-mo' | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**beds** | Option<**i32**> | 0=studio, 1-4 bedrooms |  |
**min_price** | Option<**i32**> |  |  |
**max_price** | Option<**i32**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

