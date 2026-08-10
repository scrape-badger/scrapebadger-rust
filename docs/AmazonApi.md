# \AmazonApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**amazon_amazon_scraper_health_check**](AmazonApi.md#amazon_amazon_scraper_health_check) | **GET** /v1/amazon/health | Amazon scraper health check
[**amazon_amazon_scraper_health_check_head**](AmazonApi.md#amazon_amazon_scraper_health_check_head) | **HEAD** /v1/amazon/health | Amazon scraper health check
[**amazon_bestsellers_by_category**](AmazonApi.md#amazon_bestsellers_by_category) | **GET** /v1/amazon/bestsellers | Bestsellers by category
[**amazon_browse_node_category_listing**](AmazonApi.md#amazon_browse_node_category_listing) | **GET** /v1/amazon/category | Browse-node category listing
[**amazon_get_all_seller_offers_buybox**](AmazonApi.md#amazon_get_all_seller_offers_buybox) | **GET** /v1/amazon/products/{asin}/offers | Get all seller offers (buybox)
[**amazon_get_product_detail**](AmazonApi.md#amazon_get_product_detail) | **GET** /v1/amazon/products/{asin} | Get product detail
[**amazon_get_product_reviews**](AmazonApi.md#amazon_get_product_reviews) | **GET** /v1/amazon/products/{asin}/reviews | Get product reviews
[**amazon_get_seller_feedback**](AmazonApi.md#amazon_get_seller_feedback) | **GET** /v1/amazon/sellers/{seller_id}/feedback | Get seller feedback
[**amazon_get_seller_profile**](AmazonApi.md#amazon_get_seller_profile) | **GET** /v1/amazon/sellers/{seller_id} | Get seller profile
[**amazon_get_seller_storefront_products**](AmazonApi.md#amazon_get_seller_storefront_products) | **GET** /v1/amazon/sellers/{seller_id}/products | Get seller storefront products
[**amazon_keyword_suggestions**](AmazonApi.md#amazon_keyword_suggestions) | **GET** /v1/amazon/autocomplete | Keyword suggestions
[**amazon_list_category_aliases**](AmazonApi.md#amazon_list_category_aliases) | **GET** /v1/amazon/categories | List category aliases
[**amazon_list_marketplaces**](AmazonApi.md#amazon_list_marketplaces) | **GET** /v1/amazon/markets | List marketplaces
[**amazon_new_releases_by_category**](AmazonApi.md#amazon_new_releases_by_category) | **GET** /v1/amazon/new-releases | New releases by category
[**amazon_search_amazon_products**](AmazonApi.md#amazon_search_amazon_products) | **GET** /v1/amazon/search | Search Amazon products
[**amazon_today_s_deals**](AmazonApi.md#amazon_today_s_deals) | **GET** /v1/amazon/deals | Today's deals



## amazon_amazon_scraper_health_check

> serde_json::Value amazon_amazon_scraper_health_check()
Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

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


## amazon_amazon_scraper_health_check_head

> serde_json::Value amazon_amazon_scraper_health_check_head()
Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

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


## amazon_bestsellers_by_category

> serde_json::Value amazon_bestsellers_by_category(domain, category, page)
Bestsellers by category

Top-selling products for a category (browse node).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**domain** | Option<**String**> |  |  |[default to com]
**category** | Option<**String**> | Bestsellers node id or slug |  |
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## amazon_browse_node_category_listing

> serde_json::Value amazon_browse_node_category_listing(node, domain, page, sort_by)
Browse-node category listing

List products within an Amazon browse-node category.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**node** | **String** | Amazon browse-node id | [required] |
**domain** | Option<**String**> |  |  |[default to com]
**page** | Option<**i32**> |  |  |[default to 1]
**sort_by** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## amazon_get_all_seller_offers_buybox

> serde_json::Value amazon_get_all_seller_offers_buybox(asin, domain, zip)
Get all seller offers (buybox)

All third-party offers for an ASIN, including the Buy Box winner.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**asin** | **String** |  | [required] |
**domain** | Option<**String**> |  |  |[default to com]
**zip** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## amazon_get_product_detail

> serde_json::Value amazon_get_product_detail(asin, domain, zip, language)
Get product detail

Full product detail by ASIN (price, variants, badges, buybox, ranks…).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**asin** | **String** |  | [required] |
**domain** | Option<**String**> |  |  |[default to com]
**zip** | Option<**String**> | Delivery postal/zip for localized buybox |  |
**language** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## amazon_get_product_reviews

> serde_json::Value amazon_get_product_reviews(asin, domain, page, sort_by, star, verified_only, media_only)
Get product reviews

Customer reviews for an ASIN (featured + paginated, with filters).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**asin** | **String** |  | [required] |
**domain** | Option<**String**> |  |  |[default to com]
**page** | Option<**i32**> | Review page (1-100, ~10 reviews/page) |  |[default to 1]
**sort_by** | Option<**String**> | helpful | recent |  |[default to helpful]
**star** | Option<**String**> | one_star..five_star | positive | critical |  |
**verified_only** | Option<**bool**> |  |  |[default to false]
**media_only** | Option<**bool**> |  |  |[default to false]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## amazon_get_seller_feedback

> serde_json::Value amazon_get_seller_feedback(seller_id, domain, page)
Get seller feedback

Buyer feedback entries for a seller.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**seller_id** | **String** |  | [required] |
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


## amazon_get_seller_profile

> serde_json::Value amazon_get_seller_profile(seller_id, domain)
Get seller profile

Seller profile, ratings and feedback summary.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**seller_id** | **String** |  | [required] |
**domain** | Option<**String**> |  |  |[default to com]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## amazon_get_seller_storefront_products

> serde_json::Value amazon_get_seller_storefront_products(seller_id, domain, page)
Get seller storefront products

Products listed in a seller's storefront.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**seller_id** | **String** |  | [required] |
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


## amazon_keyword_suggestions

> serde_json::Value amazon_keyword_suggestions(query, domain)
Keyword suggestions

Get Amazon search autocomplete suggestions for keyword research.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial search term | [required] |
**domain** | Option<**String**> |  |  |[default to com]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## amazon_list_category_aliases

> serde_json::Value amazon_list_category_aliases(domain)
List category aliases

List common Amazon department/category aliases and bestseller nodes.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**domain** | Option<**String**> |  |  |[default to com]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## amazon_list_marketplaces

> serde_json::Value amazon_list_marketplaces()
List marketplaces

List all supported Amazon marketplaces.

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


## amazon_new_releases_by_category

> serde_json::Value amazon_new_releases_by_category(domain, category, page)
New releases by category

Newly released products for a category (browse node).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**domain** | Option<**String**> |  |  |[default to com]
**category** | Option<**String**> |  |  |
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## amazon_search_amazon_products

> serde_json::Value amazon_search_amazon_products(query, domain, page, sort_by, category, min_price, max_price, zip, language)
Search Amazon products

Search the Amazon catalog with filters and sorting.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords | [required] |
**domain** | Option<**String**> | Amazon marketplace TLD or code (com, co.uk, de…) |  |[default to com]
**page** | Option<**i32**> |  |  |[default to 1]
**sort_by** | Option<**String**> | relevance | price_low_to_high | price_high_to_low | avg_review | newest |  |
**category** | Option<**String**> | Department/category alias (i= param) |  |
**min_price** | Option<**f64**> |  |  |
**max_price** | Option<**f64**> |  |  |
**zip** | Option<**String**> | Delivery postal/zip code for localized pricing |  |
**language** | Option<**String**> | Locale for results, e.g. en_US, fr_FR |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## amazon_today_s_deals

> serde_json::Value amazon_today_s_deals(domain, category, page)
Today's deals

Current Amazon deals (lightning deals, best deals).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**domain** | Option<**String**> |  |  |[default to com]
**category** | Option<**String**> |  |  |
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

