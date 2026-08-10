# \IdealistaApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**idealista_agency_by_phone**](IdealistaApi.md#idealista_agency_by_phone) | **GET** /v1/idealista/agency/by-phone/{phone} | Agency by phone
[**idealista_agency_profile_listings**](IdealistaApi.md#idealista_agency_profile_listings) | **GET** /v1/idealista/agency/{short_name} | Agency profile + listings
[**idealista_get_listing_engagement_stats**](IdealistaApi.md#idealista_get_listing_engagement_stats) | **GET** /v1/idealista/properties/{property_code}/stats | Get listing engagement stats
[**idealista_get_property_detail**](IdealistaApi.md#idealista_get_property_detail) | **GET** /v1/idealista/properties/{property_code} | Get property detail
[**idealista_idealista_scraper_health_check**](IdealistaApi.md#idealista_idealista_scraper_health_check) | **GET** /v1/idealista/health | Idealista scraper health check
[**idealista_idealista_scraper_health_check_head**](IdealistaApi.md#idealista_idealista_scraper_health_check_head) | **HEAD** /v1/idealista/health | Idealista scraper health check
[**idealista_list_markets**](IdealistaApi.md#idealista_list_markets) | **GET** /v1/idealista/markets | List markets
[**idealista_resolve_locations**](IdealistaApi.md#idealista_resolve_locations) | **GET** /v1/idealista/suggest | Resolve locations
[**idealista_search_all_beats_result_cap**](IdealistaApi.md#idealista_search_all_beats_result_cap) | **GET** /v1/idealista/search/all | Search all (beats result cap)
[**idealista_search_listings**](IdealistaApi.md#idealista_search_listings) | **GET** /v1/idealista/search | Search listings



## idealista_agency_by_phone

> serde_json::Value idealista_agency_by_phone(phone, market, operation, property_type, page, max_items, include_listings)
Agency by phone

Reverse-lookup the agency behind a contact phone (national number), with its listings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**phone** | **String** |  | [required] |
**market** | Option<**String**> | es|it|pt |  |[default to es]
**operation** | Option<**String**> | sale|rent |  |
**property_type** | Option<**String**> | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms |  |
**page** | Option<**i32**> |  |  |[default to 1]
**max_items** | Option<**i32**> |  |  |[default to 30]
**include_listings** | Option<**bool**> |  |  |[default to true]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## idealista_agency_profile_listings

> serde_json::Value idealista_agency_profile_listings(short_name, market, operation, property_type, page, max_items, include_listings)
Agency profile + listings

An agency's microsite profile plus a page of its listings (by URL-slug shortName).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**short_name** | **String** |  | [required] |
**market** | Option<**String**> | es|it|pt |  |[default to es]
**operation** | Option<**String**> | sale|rent |  |
**property_type** | Option<**String**> | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms |  |
**page** | Option<**i32**> |  |  |[default to 1]
**max_items** | Option<**i32**> |  |  |[default to 30]
**include_listings** | Option<**bool**> |  |  |[default to true]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## idealista_get_listing_engagement_stats

> serde_json::Value idealista_get_listing_engagement_stats(property_code, market, locale)
Get listing engagement stats

Engagement counters for a listing: views, email contacts, sent-to-friend, favourites.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**property_code** | **String** |  | [required] |
**market** | Option<**String**> | es|it|pt |  |[default to es]
**locale** | Option<**String**> | Language for stat labels |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## idealista_get_property_detail

> serde_json::Value idealista_get_property_detail(property_code, market, locale)
Get property detail

Get a single Idealista listing's full detail (energy cert, characteristics, media).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**property_code** | **String** |  | [required] |
**market** | Option<**String**> | es|it|pt |  |[default to es]
**locale** | Option<**String**> | Response language (en, es, it, pt) |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## idealista_idealista_scraper_health_check

> serde_json::Value idealista_idealista_scraper_health_check()
Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

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


## idealista_idealista_scraper_health_check_head

> serde_json::Value idealista_idealista_scraper_health_check_head()
Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

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


## idealista_list_markets

> serde_json::Value idealista_list_markets()
List markets

List supported Idealista markets (ES, IT, PT).

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


## idealista_resolve_locations

> serde_json::Value idealista_resolve_locations(query, operation, property_type, market, locale)
Resolve locations

Resolve a free-text query into Idealista location codes for a search.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Free-text location, e.g. 'sagrada familia' | [required] |
**operation** | Option<**String**> | sale|rent |  |[default to sale]
**property_type** | Option<**String**> | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms |  |[default to homes]
**market** | Option<**String**> | es|it|pt |  |[default to es]
**locale** | Option<**String**> | Response language (en, es, it, pt) |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## idealista_search_all_beats_result_cap

> serde_json::Value idealista_search_all_beats_result_cap(location, operation, property_type, market, max_results, min_price, max_price, min_size, max_size, min_rooms, max_rooms, locale)
Search all (beats result cap)

Full inventory for a location, beating Idealista's ~1800 per-search cap via price-range tiling (deduped). Billed per page fetched.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | **String** | Idealista location code (from /suggest) | [required] |
**operation** | Option<**String**> | sale|rent |  |[default to sale]
**property_type** | Option<**String**> | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms |  |[default to homes]
**market** | Option<**String**> | es|it|pt |  |[default to es]
**max_results** | Option<**i32**> |  |  |[default to 500]
**min_price** | Option<**f64**> |  |  |
**max_price** | Option<**f64**> |  |  |
**min_size** | Option<**f64**> |  |  |
**max_size** | Option<**f64**> |  |  |
**min_rooms** | Option<**i32**> |  |  |
**max_rooms** | Option<**i32**> |  |  |
**locale** | Option<**String**> | Response language (en, es, it, pt) |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## idealista_search_listings

> serde_json::Value idealista_search_listings(location, operation, property_type, market, page, max_items, sort_by, sort_order, min_price, max_price, min_size, max_size, min_rooms, max_rooms, locale)
Search listings

Search Idealista real-estate listings by location code.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | **String** | Idealista location code (from /suggest) | [required] |
**operation** | Option<**String**> | sale|rent |  |[default to sale]
**property_type** | Option<**String**> | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms |  |[default to homes]
**market** | Option<**String**> | es|it|pt |  |[default to es]
**page** | Option<**i32**> |  |  |[default to 1]
**max_items** | Option<**i32**> |  |  |[default to 30]
**sort_by** | Option<**String**> | distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds |  |
**sort_order** | Option<**String**> | asc|desc |  |[default to desc]
**min_price** | Option<**f64**> |  |  |
**max_price** | Option<**f64**> |  |  |
**min_size** | Option<**f64**> |  |  |
**max_size** | Option<**f64**> |  |  |
**min_rooms** | Option<**i32**> |  |  |
**max_rooms** | Option<**i32**> |  |  |
**locale** | Option<**String**> | Response language (en, es, it, pt) |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

