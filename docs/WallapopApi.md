# \WallapopApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**wallapop_autocomplete**](WallapopApi.md#wallapop_autocomplete) | **GET** /v1/wallapop/autocomplete | Autocomplete
[**wallapop_get_listing_detail**](WallapopApi.md#wallapop_get_listing_detail) | **GET** /v1/wallapop/items/{item_id} | Get listing detail
[**wallapop_get_user_listings**](WallapopApi.md#wallapop_get_user_listings) | **GET** /v1/wallapop/users/{user_id}/items | Get user listings
[**wallapop_get_user_profile**](WallapopApi.md#wallapop_get_user_profile) | **GET** /v1/wallapop/users/{user_id} | Get user profile
[**wallapop_get_user_reviews**](WallapopApi.md#wallapop_get_user_reviews) | **GET** /v1/wallapop/users/{user_id}/reviews | Get user reviews
[**wallapop_list_categories**](WallapopApi.md#wallapop_list_categories) | **GET** /v1/wallapop/categories | List categories
[**wallapop_list_filter_options**](WallapopApi.md#wallapop_list_filter_options) | **GET** /v1/wallapop/filters/{filter_id}/options | List filter options
[**wallapop_list_markets**](WallapopApi.md#wallapop_list_markets) | **GET** /v1/wallapop/markets | List markets
[**wallapop_list_search_filters**](WallapopApi.md#wallapop_list_search_filters) | **GET** /v1/wallapop/filters | List search filters
[**wallapop_search_listings**](WallapopApi.md#wallapop_search_listings) | **GET** /v1/wallapop/search | Search listings
[**wallapop_wallapop_scraper_health_check**](WallapopApi.md#wallapop_wallapop_scraper_health_check) | **GET** /v1/wallapop/health | Wallapop scraper health check
[**wallapop_wallapop_scraper_health_check_head**](WallapopApi.md#wallapop_wallapop_scraper_health_check_head) | **HEAD** /v1/wallapop/health | Wallapop scraper health check



## wallapop_autocomplete

> serde_json::Value wallapop_autocomplete(query, market)
Autocomplete

Wallapop's search-box suggestions for a partial query.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial search text, e.g. 'bici' | [required] |
**market** | Option<**String**> | Market: es (Spain), it (Italy), pt (Portugal) |  |[default to es]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## wallapop_get_listing_detail

> serde_json::Value wallapop_get_listing_detail(item_id, market)
Get listing detail

Full listing detail by id (e.g. nzxeknm5x562) or listing slug.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**item_id** | **String** |  | [required] |
**market** | Option<**String**> | Market: es (Spain), it (Italy), pt (Portugal) |  |[default to es]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## wallapop_get_user_listings

> serde_json::Value wallapop_get_user_listings(user_id, market, next_page)
Get user listings

A seller's live listings, 40 per page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |
**market** | Option<**String**> | Market: es (Spain), it (Italy), pt (Portugal) |  |[default to es]
**next_page** | Option<**String**> | Cursor from the previous page's next_page |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## wallapop_get_user_profile

> serde_json::Value wallapop_get_user_profile(user_id, market)
Get user profile

Seller profile with ratings, sales counters, response rate and verifications.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |
**market** | Option<**String**> | Market: es (Spain), it (Italy), pt (Portugal) |  |[default to es]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## wallapop_get_user_reviews

> serde_json::Value wallapop_get_user_reviews(user_id, market, next_page)
Get user reviews

Reviews a seller received, newest first, 40 per page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |
**market** | Option<**String**> | Market: es (Spain), it (Italy), pt (Portugal) |  |[default to es]
**next_page** | Option<**String**> | Cursor from the previous page's next_page |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## wallapop_list_categories

> serde_json::Value wallapop_list_categories(market)
List categories

The full category tree; ids are usable as the search category_id.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**market** | Option<**String**> | Market: es (Spain), it (Italy), pt (Portugal) |  |[default to es]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## wallapop_list_filter_options

> serde_json::Value wallapop_list_filter_options(filter_id, category_id, query, market)
List filter options

Long option lists (e.g. brand, model) for filters flagged options_endpoint.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**filter_id** | **String** |  | [required] |
**category_id** | Option<**i32**> | Category to scope options to |  |
**query** | Option<**String**> | Search text to scope options to |  |
**market** | Option<**String**> | Market: es (Spain), it (Italy), pt (Portugal) |  |[default to es]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## wallapop_list_markets

> serde_json::Value wallapop_list_markets()
List markets

Supported Wallapop markets and their default search location.

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


## wallapop_list_search_filters

> serde_json::Value wallapop_list_search_filters(category_id, query, market)
List search filters

The filters Wallapop offers for a category or query, with option ids.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category_id** | Option<**i32**> | Category the filters apply to |  |
**query** | Option<**String**> | Search text the filters apply to |  |
**market** | Option<**String**> | Market: es (Spain), it (Italy), pt (Portugal) |  |[default to es]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## wallapop_search_listings

> serde_json::Value wallapop_search_listings(query, market, latitude, longitude, distance_km, category_id, min_price, max_price, condition, brand, model, color, time_filter, shippable, has_warranty, refurbished, min_year, max_year, min_km, max_km, gearbox, min_horsepower, max_horsepower, order_by, next_page)
Search listings

Search Wallapop listings (40 per page). Needs a query, a category_id, or both.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | Option<**String**> | Search text, e.g. 'iphone 14' |  |
**market** | Option<**String**> | Market: es (Spain), it (Italy), pt (Portugal) |  |[default to es]
**latitude** | Option<**f64**> | Search centre latitude (defaults to the market capital) |  |
**longitude** | Option<**f64**> | Search centre longitude |  |
**distance_km** | Option<**i32**> | Search radius |  |
**category_id** | Option<**i32**> | Category id from /categories |  |
**min_price** | Option<**f64**> | Minimum price (EUR) |  |
**max_price** | Option<**f64**> | Maximum price (EUR) |  |
**condition** | Option<**String**> | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all |  |
**brand** | Option<**String**> | Brand, e.g. Apple |  |
**model** | Option<**String**> | Model, e.g. iPhone 14 |  |
**color** | Option<**String**> | Colour id, e.g. black |  |
**time_filter** | Option<**String**> | Only listings published within this window |  |
**shippable** | Option<**bool**> | Only listings that ship |  |[default to false]
**has_warranty** | Option<**bool**> | Only listings with a warranty |  |[default to false]
**refurbished** | Option<**bool**> | Only refurbished listings |  |[default to false]
**min_year** | Option<**i32**> | Cars: earliest model year |  |
**max_year** | Option<**i32**> | Cars: latest model year |  |
**min_km** | Option<**i32**> | Cars: minimum mileage |  |
**max_km** | Option<**i32**> | Cars: maximum mileage |  |
**gearbox** | Option<**String**> | Cars |  |
**min_horsepower** | Option<**i32**> | Cars: minimum power |  |
**max_horsepower** | Option<**i32**> | Cars: maximum power |  |
**order_by** | Option<**String**> | Sort order |  |[default to most_relevance]
**next_page** | Option<**String**> | Cursor from the previous page's next_page; other parameters are then ignored |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## wallapop_wallapop_scraper_health_check

> serde_json::Value wallapop_wallapop_scraper_health_check()
Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

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


## wallapop_wallapop_scraper_health_check_head

> serde_json::Value wallapop_wallapop_scraper_health_check_head()
Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

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

