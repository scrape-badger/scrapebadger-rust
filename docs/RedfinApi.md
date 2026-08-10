# \RedfinApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**redfin_get_agent_profile_listings**](RedfinApi.md#redfin_get_agent_profile_listings) | **GET** /v1/redfin/agent | Get agent profile + listings
[**redfin_get_property_detail**](RedfinApi.md#redfin_get_property_detail) | **GET** /v1/redfin/property/{property_id} | Get property detail
[**redfin_get_property_detail_by_url**](RedfinApi.md#redfin_get_property_detail_by_url) | **GET** /v1/redfin/property | Get property detail by URL
[**redfin_list_coverage_markets**](RedfinApi.md#redfin_list_coverage_markets) | **GET** /v1/redfin/markets | List coverage markets
[**redfin_redfin_scraper_health_check**](RedfinApi.md#redfin_redfin_scraper_health_check) | **GET** /v1/redfin/health | Redfin scraper health check
[**redfin_redfin_scraper_health_check_head**](RedfinApi.md#redfin_redfin_scraper_health_check_head) | **HEAD** /v1/redfin/health | Redfin scraper health check
[**redfin_region_address_suggestions**](RedfinApi.md#redfin_region_address_suggestions) | **GET** /v1/redfin/autocomplete | Region/address suggestions
[**redfin_search_properties**](RedfinApi.md#redfin_search_properties) | **GET** /v1/redfin/search | Search properties



## redfin_get_agent_profile_listings

> serde_json::Value redfin_get_agent_profile_listings(url, agent_id)
Get agent profile + listings

Get a Redfin real-estate agent's profile and their active listings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | Option<**String**> | Full Redfin /realestateagents/ URL |  |
**agent_id** | Option<**String**> | Redfin agent id |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## redfin_get_property_detail

> serde_json::Value redfin_get_property_detail(property_id)
Get property detail

Get a single Redfin property's full detail by its numeric propertyId.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**property_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## redfin_get_property_detail_by_url

> serde_json::Value redfin_get_property_detail_by_url(url)
Get property detail by URL

Get a single Redfin property's full detail by its home URL.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | Full Redfin property URL (/CA/City/.../home/12345678) | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## redfin_list_coverage_markets

> serde_json::Value redfin_list_coverage_markets()
List coverage markets

List Redfin coverage regions (US).

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


## redfin_redfin_scraper_health_check

> serde_json::Value redfin_redfin_scraper_health_check()
Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

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


## redfin_redfin_scraper_health_check_head

> serde_json::Value redfin_redfin_scraper_health_check_head()
Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

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


## redfin_region_address_suggestions

> serde_json::Value redfin_region_address_suggestions(query)
Region/address suggestions

Resolve a search term to Redfin regions/addresses.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial location — city, ZIP, address, neighborhood | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## redfin_search_properties

> serde_json::Value redfin_search_properties(location, page, sort, price_min, price_max, beds_min, baths_min, home_type, sqft_min, sqft_max, lot_min, lot_max, year_built_min, year_built_max, max_days_on_market, north, south, east, west)
Search properties

Search Redfin for for-sale / for-rent / recently-sold properties.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | **String** | City/state, ZIP, address or neighborhood | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**sort** | Option<**String**> | relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths |  |
**price_min** | Option<**i32**> |  |  |
**price_max** | Option<**i32**> |  |  |
**beds_min** | Option<**i32**> |  |  |
**baths_min** | Option<**f64**> |  |  |
**home_type** | Option<**String**> | house|condo|townhouse|multi_family|land|mobile|coop|other |  |
**sqft_min** | Option<**i32**> |  |  |
**sqft_max** | Option<**i32**> |  |  |
**lot_min** | Option<**i32**> |  |  |
**lot_max** | Option<**i32**> |  |  |
**year_built_min** | Option<**i32**> |  |  |
**year_built_max** | Option<**i32**> |  |  |
**max_days_on_market** | Option<**i32**> |  |  |
**north** | Option<**f64**> | Map bounds for tiling past the cap |  |
**south** | Option<**f64**> |  |  |
**east** | Option<**f64**> |  |  |
**west** | Option<**f64**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

