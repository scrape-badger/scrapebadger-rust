# \AutoScout24Api

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**autoscout24_check_autoscout24_health**](AutoScout24Api.md#autoscout24_check_autoscout24_health) | **GET** /v1/autoscout24/health | Check AutoScout24 health
[**autoscout24_get_listing**](AutoScout24Api.md#autoscout24_get_listing) | **GET** /v1/autoscout24/listing | Get listing
[**autoscout24_list_markets**](AutoScout24Api.md#autoscout24_list_markets) | **GET** /v1/autoscout24/markets | List markets
[**autoscout24_list_search_filters**](AutoScout24Api.md#autoscout24_list_search_filters) | **GET** /v1/autoscout24/filters | List search filters
[**autoscout24_search_vehicles**](AutoScout24Api.md#autoscout24_search_vehicles) | **GET** /v1/autoscout24/search | Search vehicles



## autoscout24_check_autoscout24_health

> serde_json::Value autoscout24_check_autoscout24_health()
Check AutoScout24 health

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


## autoscout24_get_listing

> models::AutoScout24ListingResponse autoscout24_get_listing(url, listing_id, market)
Get listing

Full public vehicle specifications, equipment, photos, price and seller data.  Exactly one of url or listing_id is required. Supported markets match /markets. Successful detail costs 10 credits; removed or missing listings return an unbilled 404. Invalid inputs return 422 and source failures 503.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | Option<**String**> | Full HTTPS listing URL from search results. Supply url or listing_id, not both. |  |
**listing_id** | Option<**String**> | Listing UUID from search results; requires no SEO slug. |  |
**market** | Option<**String**> | Inferred from URL, otherwise de. Explicit market must match the URL host. |  |

### Return type

[**models::AutoScout24ListingResponse**](AutoScout24ListingResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## autoscout24_list_markets

> models::AutoScout24MarketsResponse autoscout24_list_markets()
List markets

Verified marketplaces, domains, languages and currency. Free reference endpoint.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AutoScout24MarketsResponse**](AutoScout24MarketsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## autoscout24_list_search_filters

> models::AutoScout24FiltersResponse autoscout24_list_search_filters(market, make)
List search filters

Current native make, model and vehicle filter options. Set make for its models.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**market** | Option<**String**> |  |  |[default to de]
**make** | Option<**String**> |  |  |

### Return type

[**models::AutoScout24FiltersResponse**](AutoScout24FiltersResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## autoscout24_search_vehicles

> models::AutoScout24SearchResponse autoscout24_search_vehicles(market, make, model, price_min, price_max, mileage_min, mileage_max, year_min, year_max, power_min, power_max, fuel_type, transmission, body_type, seller_type, condition, zip, radius, sort_by, page)
Search vehicles

Search live vehicle cards, seller/location information and current filter taxonomy.  Browsing is capped at 200 pages (normally 20 cards each). Narrow the query to reach more inventory. Empty results cost zero credits. Pass a result's url or id to /listing for its full specifications and equipment.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**market** | Option<**String**> |  |  |[default to de]
**make** | Option<**String**> | Native make slug, e.g. volkswagen or bmw. |  |
**model** | Option<**String**> | Native model slug, e.g. golf. Requires make. |  |
**price_min** | Option<**i32**> |  |  |
**price_max** | Option<**i32**> |  |  |
**mileage_min** | Option<**i32**> | Kilometres. |  |
**mileage_max** | Option<**i32**> |  |  |
**year_min** | Option<**i32**> |  |  |
**year_max** | Option<**i32**> |  |  |
**power_min** | Option<**i32**> | Engine power in kW. |  |
**power_max** | Option<**i32**> |  |  |
**fuel_type** | Option<**String**> |  |  |
**transmission** | Option<**String**> |  |  |
**body_type** | Option<**String**> |  |  |
**seller_type** | Option<**String**> |  |  |
**condition** | Option<**String**> |  |  |
**zip** | Option<**String**> | Postal code in the requested market. |  |
**radius** | Option<**i32**> | Kilometres; requires zip. |  |
**sort_by** | Option<**String**> |  |  |[default to best_match]
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**models::AutoScout24SearchResponse**](AutoScout24SearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

