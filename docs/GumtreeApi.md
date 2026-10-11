# \GumtreeApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gumtree_get_listing**](GumtreeApi.md#gumtree_get_listing) | **GET** /v1/gumtree/listings/{listing_id} | Get listing
[**gumtree_get_search_filters**](GumtreeApi.md#gumtree_get_search_filters) | **GET** /v1/gumtree/search/filters | Get search filters
[**gumtree_get_seller_listings**](GumtreeApi.md#gumtree_get_seller_listings) | **GET** /v1/gumtree/listings/{listing_id}/seller-listings | Get seller listings
[**gumtree_gumtree_scraper_health_check**](GumtreeApi.md#gumtree_gumtree_scraper_health_check) | **GET** /v1/gumtree/health | Gumtree scraper health check
[**gumtree_gumtree_scraper_health_check_head**](GumtreeApi.md#gumtree_gumtree_scraper_health_check_head) | **HEAD** /v1/gumtree/health | Gumtree scraper health check
[**gumtree_list_categories**](GumtreeApi.md#gumtree_list_categories) | **GET** /v1/gumtree/categories | List categories
[**gumtree_list_locations**](GumtreeApi.md#gumtree_list_locations) | **GET** /v1/gumtree/locations | List locations
[**gumtree_location_suggestions**](GumtreeApi.md#gumtree_location_suggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions
[**gumtree_search_listings**](GumtreeApi.md#gumtree_search_listings) | **GET** /v1/gumtree/search | Search listings
[**gumtree_search_suggestions**](GumtreeApi.md#gumtree_search_suggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions



## gumtree_get_listing

> serde_json::Value gumtree_get_listing(listing_id)
Get listing

Full listing — description, attributes, images, seller, similar listings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**listing_id** | **String** | Gumtree listing id — the number at the end of a gumtree.com/p/... URL | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## gumtree_get_search_filters

> serde_json::Value gumtree_get_search_filters(category, location, query)
Get search filters

Filters, sort orders and radius options for a category, with live counts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category** | Option<**String**> | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'. |  |[default to all]
**location** | Option<**String**> | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'. |  |[default to uk]
**query** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## gumtree_get_seller_listings

> serde_json::Value gumtree_get_seller_listings(listing_id, page)
Get seller listings

Every live listing by the seller of the given listing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**listing_id** | **String** | Gumtree listing id — the number at the end of a gumtree.com/p/... URL | [required] |
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## gumtree_gumtree_scraper_health_check

> serde_json::Value gumtree_gumtree_scraper_health_check()
Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

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


## gumtree_gumtree_scraper_health_check_head

> serde_json::Value gumtree_gumtree_scraper_health_check_head()
Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

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


## gumtree_list_categories

> serde_json::Value gumtree_list_categories(parent_id)
List categories

Browse Gumtree's category tree. A node's `slug` is the `/search` category.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**parent_id** | Option<**i32**> | Parent category id (default: all) |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## gumtree_list_locations

> serde_json::Value gumtree_list_locations(parent_id)
List locations

Browse Gumtree's location tree.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**parent_id** | Option<**i32**> | Parent location id (default: UK) |  |[default to 10000392]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## gumtree_location_suggestions

> serde_json::Value gumtree_location_suggestions(query)
Location suggestions

Resolve a place name or postcode to Gumtree locations with coordinates.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Town or postcode prefix, e.g. 'manch' | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## gumtree_search_listings

> serde_json::Value gumtree_search_listings(query, category, location, distance, min_price, max_price, sort, seller_type, urgent_only, with_photos, filters, page)
Search listings

Search gumtree.com listings. ~25-30 per page, up to 50 pages.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | Option<**String**> | Search keywords, e.g. 'mountain bike' |  |
**category** | Option<**String**> | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'. |  |[default to all]
**location** | Option<**String**> | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'. |  |[default to uk]
**distance** | Option<**f64**> | Radius in miles |  |
**min_price** | Option<**i32**> | GBP; needs a category |  |
**max_price** | Option<**i32**> | GBP; needs a category |  |
**sort** | Option<**String**> |  |  |
**seller_type** | Option<**String**> |  |  |
**urgent_only** | Option<**bool**> |  |  |[default to false]
**with_photos** | Option<**bool**> |  |  |[default to false]
**filters** | Option<**String**> | Category filters as key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol' |  |
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## gumtree_search_suggestions

> serde_json::Value gumtree_search_suggestions(query)
Search suggestions

Gumtree search-box keyword suggestions with their categories.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial search term, e.g. 'iph' | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

