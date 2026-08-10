# \ZillowApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**zillow_get_agent_profile_listings**](ZillowApi.md#zillow_get_agent_profile_listings) | **GET** /v1/zillow/agent | Get agent profile + listings
[**zillow_get_property_detail**](ZillowApi.md#zillow_get_property_detail) | **GET** /v1/zillow/property/{zpid} | Get property detail
[**zillow_get_property_detail_by_url**](ZillowApi.md#zillow_get_property_detail_by_url) | **GET** /v1/zillow/property | Get property detail by URL
[**zillow_list_coverage_markets**](ZillowApi.md#zillow_list_coverage_markets) | **GET** /v1/zillow/markets | List coverage markets
[**zillow_region_address_suggestions**](ZillowApi.md#zillow_region_address_suggestions) | **GET** /v1/zillow/autocomplete | Region/address suggestions
[**zillow_search_properties**](ZillowApi.md#zillow_search_properties) | **GET** /v1/zillow/search | Search properties
[**zillow_zillow_scraper_health_check**](ZillowApi.md#zillow_zillow_scraper_health_check) | **GET** /v1/zillow/health | Zillow scraper health check
[**zillow_zillow_scraper_health_check_head**](ZillowApi.md#zillow_zillow_scraper_health_check_head) | **HEAD** /v1/zillow/health | Zillow scraper health check



## zillow_get_agent_profile_listings

> serde_json::Value zillow_get_agent_profile_listings(username, url)
Get agent profile + listings

Get a Zillow professional's profile and their active listings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | Option<**String**> | Zillow profile username |  |
**url** | Option<**String**> | Full Zillow /profile/... URL |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## zillow_get_property_detail

> serde_json::Value zillow_get_property_detail(zpid)
Get property detail

Get a single Zillow property's full detail by zpid.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**zpid** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## zillow_get_property_detail_by_url

> serde_json::Value zillow_get_property_detail_by_url(url)
Get property detail by URL

Get a single Zillow property's full detail by its homedetails URL.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | Full Zillow /homedetails/... URL | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## zillow_list_coverage_markets

> serde_json::Value zillow_list_coverage_markets()
List coverage markets

List Zillow coverage regions (US + Canada).

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


## zillow_region_address_suggestions

> serde_json::Value zillow_region_address_suggestions(query)
Region/address suggestions

Resolve a search term to Zillow regions/addresses.

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


## zillow_search_properties

> serde_json::Value zillow_search_properties(location, status, page, sort, price_min, price_max, beds_min, baths_min, home_type, sqft_min, sqft_max, lot_min, lot_max, year_built_min, year_built_max, hoa_max, keywords, days_on, north, south, east, west)
Search properties

Search Zillow for for-sale / for-rent / recently-sold properties.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | **String** | City/state, ZIP, address or neighborhood | [required] |
**status** | Option<**String**> | for_sale|for_rent|sold |  |[default to for_sale]
**page** | Option<**i32**> |  |  |[default to 1]
**sort** | Option<**String**> | homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built |  |
**price_min** | Option<**i32**> |  |  |
**price_max** | Option<**i32**> |  |  |
**beds_min** | Option<**i32**> |  |  |
**baths_min** | Option<**f64**> |  |  |
**home_type** | Option<**String**> | houses|condos|townhomes|apartments|manufactured|lots|multi_family |  |
**sqft_min** | Option<**i32**> |  |  |
**sqft_max** | Option<**i32**> |  |  |
**lot_min** | Option<**i32**> |  |  |
**lot_max** | Option<**i32**> |  |  |
**year_built_min** | Option<**i32**> |  |  |
**year_built_max** | Option<**i32**> |  |  |
**hoa_max** | Option<**i32**> |  |  |
**keywords** | Option<**String**> |  |  |
**days_on** | Option<**String**> |  |  |
**north** | Option<**f64**> | Map bounds for tiling past the 820 cap |  |
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


## zillow_zillow_scraper_health_check

> serde_json::Value zillow_zillow_scraper_health_check()
Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

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


## zillow_zillow_scraper_health_check_head

> serde_json::Value zillow_zillow_scraper_health_check_head()
Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

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

