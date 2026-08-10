# \WalmartApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**walmart_browse_a_category**](WalmartApi.md#walmart_browse_a_category) | **GET** /v1/walmart/category | Browse a category
[**walmart_deals_rollbacks_and_clearance**](WalmartApi.md#walmart_deals_rollbacks_and_clearance) | **GET** /v1/walmart/deals | Deals, rollbacks and clearance
[**walmart_get_a_seller_s_catalogue**](WalmartApi.md#walmart_get_a_seller_s_catalogue) | **GET** /v1/walmart/sellers/{seller_id}/products | Get a seller's catalogue
[**walmart_get_product_detail**](WalmartApi.md#walmart_get_product_detail) | **GET** /v1/walmart/products/{item_id} | Get product detail
[**walmart_get_product_reviews**](WalmartApi.md#walmart_get_product_reviews) | **GET** /v1/walmart/products/{item_id}/reviews | Get product reviews
[**walmart_get_seller_profile**](WalmartApi.md#walmart_get_seller_profile) | **GET** /v1/walmart/sellers/{seller_id} | Get seller profile
[**walmart_get_store_nearby_stores**](WalmartApi.md#walmart_get_store_nearby_stores) | **GET** /v1/walmart/stores/{store_id} | Get store + nearby stores
[**walmart_list_supported_markets**](WalmartApi.md#walmart_list_supported_markets) | **GET** /v1/walmart/markets | List supported markets
[**walmart_search_products**](WalmartApi.md#walmart_search_products) | **GET** /v1/walmart/search | Search products
[**walmart_search_suggestions**](WalmartApi.md#walmart_search_suggestions) | **GET** /v1/walmart/autocomplete | Search suggestions
[**walmart_walmart_scraper_health_check**](WalmartApi.md#walmart_walmart_scraper_health_check) | **GET** /v1/walmart/health | Walmart scraper health check
[**walmart_walmart_scraper_health_check_head**](WalmartApi.md#walmart_walmart_scraper_health_check_head) | **HEAD** /v1/walmart/health | Walmart scraper health check



## walmart_browse_a_category

> serde_json::Value walmart_browse_a_category(path, page, min_price, max_price, facet)
Browse a category

Browse a Walmart category. Same result shape as search.  No `sort`: Walmart's browse pages ignore it. Sort on `/search` instead.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**path** | **String** | Browse path, e.g. 'electronics/3944', or a '/cp/...' path | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**min_price** | Option<**f64**> |  |  |
**max_price** | Option<**f64**> |  |  |
**facet** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## walmart_deals_rollbacks_and_clearance

> serde_json::Value walmart_deals_rollbacks_and_clearance(page, min_price, max_price)
Deals, rollbacks and clearance

Walmart's current deals, rollbacks and clearance.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> |  |  |[default to 1]
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


## walmart_get_a_seller_s_catalogue

> serde_json::Value walmart_get_a_seller_s_catalogue(seller_id, query, page, sort)
Get a seller's catalogue

A marketplace seller's catalogue, scoped by a search term.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**seller_id** | **String** | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s). | [required] |
**query** | **String** | Required — Walmart returns nothing for a seller facet alone | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**sort** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## walmart_get_product_detail

> serde_json::Value walmart_get_product_detail(item_id)
Get product detail

Full product detail — price, stock, specs, variants, seller, reviews sample.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**item_id** | **String** | Walmart usItemId, e.g. '5689919121' | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## walmart_get_product_reviews

> serde_json::Value walmart_get_product_reviews(item_id, page, sort)
Get product reviews

Paginated reviews with the full star histogram. 10 per page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**item_id** | **String** | Walmart usItemId, e.g. '5689919121' | [required] |
**page** | Option<**i32**> |  |  |[default to 1]
**sort** | Option<**String**> | relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## walmart_get_seller_profile

> serde_json::Value walmart_get_seller_profile(seller_id)
Get seller profile

Marketplace seller profile — contact details, address, rating, policies.  No `page`: adding one makes Walmart's own SSR throw. Use `/sellers/{id}/products` for the catalogue.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**seller_id** | **String** | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s). | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## walmart_get_store_nearby_stores

> serde_json::Value walmart_get_store_nearby_stores(store_id)
Get store + nearby stores

Store detail with hours, per-department services, and nearby stores.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**store_id** | **String** | Walmart store number, e.g. '100' | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## walmart_list_supported_markets

> serde_json::Value walmart_list_supported_markets()
List supported markets

Supported Walmart markets.

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


## walmart_search_products

> serde_json::Value walmart_search_products(query, page, sort, min_price, max_price, facet)
Search products

Search walmart.com. ~40-60 organic products per page; ad tiles are dropped.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. 'laptop' | [required] |
**page** | Option<**i32**> | Results dry up after page 10 |  |[default to 1]
**sort** | Option<**String**> | best_match | best_seller | price_low | price_high | rating_high | new |  |
**min_price** | Option<**f64**> |  |  |
**max_price** | Option<**f64**> |  |  |
**facet** | Option<**String**> | Facet filter, e.g. 'brand:HP' |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## walmart_search_suggestions

> serde_json::Value walmart_search_suggestions(query)
Search suggestions

Walmart search-box suggestions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial search term, e.g. 'lapt' | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## walmart_walmart_scraper_health_check

> serde_json::Value walmart_walmart_scraper_health_check()
Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

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


## walmart_walmart_scraper_health_check_head

> serde_json::Value walmart_walmart_scraper_health_check_head()
Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

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

