# \EBayApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ebay_browse_a_category**](EBayApi.md#ebay_browse_a_category) | **GET** /v1/ebay/categories/{category_id}/items | Browse a category
[**ebay_completed_sold_listings**](EBayApi.md#ebay_completed_sold_listings) | **GET** /v1/ebay/completed | Completed / sold listings
[**ebay_ebay_scraper_health_check**](EBayApi.md#ebay_ebay_scraper_health_check) | **GET** /v1/ebay/health | eBay scraper health check
[**ebay_ebay_scraper_health_check_head**](EBayApi.md#ebay_ebay_scraper_health_check_head) | **HEAD** /v1/ebay/health | eBay scraper health check
[**ebay_get_item_detail**](EBayApi.md#ebay_get_item_detail) | **GET** /v1/ebay/items/{item_id} | Get item detail
[**ebay_get_item_reviews**](EBayApi.md#ebay_get_item_reviews) | **GET** /v1/ebay/items/{item_id}/reviews | Get item reviews
[**ebay_get_seller_feedback**](EBayApi.md#ebay_get_seller_feedback) | **GET** /v1/ebay/sellers/{username}/feedback | Get seller feedback
[**ebay_get_seller_listings**](EBayApi.md#ebay_get_seller_listings) | **GET** /v1/ebay/sellers/{username}/items | Get seller listings
[**ebay_get_seller_profile**](EBayApi.md#ebay_get_seller_profile) | **GET** /v1/ebay/sellers/{username} | Get seller profile
[**ebay_keyword_suggestions**](EBayApi.md#ebay_keyword_suggestions) | **GET** /v1/ebay/autocomplete | Keyword suggestions
[**ebay_list_categories**](EBayApi.md#ebay_list_categories) | **GET** /v1/ebay/categories | List categories
[**ebay_list_markets**](EBayApi.md#ebay_list_markets) | **GET** /v1/ebay/markets | List markets
[**ebay_search_listings**](EBayApi.md#ebay_search_listings) | **GET** /v1/ebay/search | Search listings



## ebay_browse_a_category

> serde_json::Value ebay_browse_a_category(category_id, domain, page, per_page, sort_by, min_price, max_price)
Browse a category

List active listings within an eBay category.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category_id** | **String** |  | [required] |
**domain** | Option<**String**> |  |  |[default to com]
**page** | Option<**i32**> |  |  |[default to 1]
**per_page** | Option<**i32**> |  |  |
**sort_by** | Option<**String**> | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low |  |[default to best_match]
**min_price** | Option<**f64**> |  |  |
**max_price** | Option<**f64**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## ebay_completed_sold_listings

> serde_json::Value ebay_completed_sold_listings(query, domain, category_id, page, per_page, sort_by, condition, min_price, max_price)
Completed / sold listings

Search completed/sold listings — eBay's sold-price history.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords | [required] |
**domain** | Option<**String**> | Marketplace domain (com, co.uk, de …) |  |[default to com]
**category_id** | Option<**String**> | Restrict to a category id |  |
**page** | Option<**i32**> |  |  |[default to 1]
**per_page** | Option<**i32**> | 60, 120 or 240 |  |
**sort_by** | Option<**String**> | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low |  |[default to best_match]
**condition** | Option<**String**> | new|open_box|refurbished|used|for_parts |  |
**min_price** | Option<**f64**> |  |  |
**max_price** | Option<**f64**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## ebay_ebay_scraper_health_check

> serde_json::Value ebay_ebay_scraper_health_check()
eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

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


## ebay_ebay_scraper_health_check_head

> serde_json::Value ebay_ebay_scraper_health_check_head()
eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

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


## ebay_get_item_detail

> serde_json::Value ebay_get_item_detail(item_id, domain)
Get item detail

Get a single eBay listing's full detail.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**item_id** | **String** |  | [required] |
**domain** | Option<**String**> |  |  |[default to com]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## ebay_get_item_reviews

> serde_json::Value ebay_get_item_reviews(item_id, domain, page)
Get item reviews

Get catalog product reviews shown on an eBay listing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**item_id** | **String** |  | [required] |
**domain** | Option<**String**> |  |  |[default to com]
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## ebay_get_seller_feedback

> serde_json::Value ebay_get_seller_feedback(username, domain, page)
Get seller feedback

Get a seller's recent feedback comments.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**domain** | Option<**String**> |  |  |[default to com]
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## ebay_get_seller_listings

> serde_json::Value ebay_get_seller_listings(username, domain, query, page, per_page)
Get seller listings

List the active listings of a single eBay seller.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**domain** | Option<**String**> |  |  |[default to com]
**query** | Option<**String**> |  |  |
**page** | Option<**i32**> |  |  |[default to 1]
**per_page** | Option<**i32**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## ebay_get_seller_profile

> serde_json::Value ebay_get_seller_profile(username, domain)
Get seller profile

Get an eBay seller's public profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**domain** | Option<**String**> |  |  |[default to com]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## ebay_keyword_suggestions

> serde_json::Value ebay_keyword_suggestions(query, domain)
Keyword suggestions

Return eBay keyword autocomplete suggestions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial query prefix | [required] |
**domain** | Option<**String**> |  |  |[default to com]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## ebay_list_categories

> serde_json::Value ebay_list_categories()
List categories

List eBay's top-level category ids.

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


## ebay_list_markets

> serde_json::Value ebay_list_markets()
List markets

List all supported eBay marketplaces.

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


## ebay_search_listings

> serde_json::Value ebay_search_listings(query, domain, category_id, page, per_page, sort_by, condition, buying_format, min_price, max_price, free_shipping)
Search listings

Search an eBay marketplace for active listings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords | [required] |
**domain** | Option<**String**> | Marketplace domain (com, co.uk, de …) |  |[default to com]
**category_id** | Option<**String**> | Restrict to a category id |  |
**page** | Option<**i32**> |  |  |[default to 1]
**per_page** | Option<**i32**> | 60, 120 or 240 |  |
**sort_by** | Option<**String**> | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low |  |[default to best_match]
**condition** | Option<**String**> | new|open_box|refurbished|used|for_parts |  |
**buying_format** | Option<**String**> | auction|buy_it_now|best_offer |  |
**min_price** | Option<**f64**> |  |  |
**max_price** | Option<**f64**> |  |  |
**free_shipping** | Option<**bool**> |  |  |[default to false]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

