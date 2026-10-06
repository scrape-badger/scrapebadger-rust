# \NaverApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**naver_naver_blog_search**](NaverApi.md#naver_naver_blog_search) | **GET** /v1/naver/blog | Naver blog search
[**naver_naver_datalab_shopping_keyword_insight**](NaverApi.md#naver_naver_datalab_shopping_keyword_insight) | **GET** /v1/naver/shopping/insight | Naver DataLab shopping keyword insight
[**naver_naver_news_search**](NaverApi.md#naver_naver_news_search) | **GET** /v1/naver/news | Naver news search
[**naver_naver_place_detail**](NaverApi.md#naver_naver_place_detail) | **GET** /v1/naver/place/{place_id} | Naver place detail
[**naver_naver_place_local_search**](NaverApi.md#naver_naver_place_local_search) | **GET** /v1/naver/local | Naver Place/Local search
[**naver_naver_place_visitor_reviews**](NaverApi.md#naver_naver_place_visitor_reviews) | **GET** /v1/naver/place/{place_id}/reviews | Naver place visitor reviews
[**naver_naver_scraper_health_check**](NaverApi.md#naver_naver_scraper_health_check) | **GET** /v1/naver/health | Naver scraper health check
[**naver_naver_scraper_health_check_head**](NaverApi.md#naver_naver_scraper_health_check_head) | **HEAD** /v1/naver/health | Naver scraper health check
[**naver_naver_shopping_bestseller_rankings**](NaverApi.md#naver_naver_shopping_bestseller_rankings) | **GET** /v1/naver/shopping/bestsellers | Naver Shopping bestseller rankings
[**naver_naver_shopping_category_reference**](NaverApi.md#naver_naver_shopping_category_reference) | **GET** /v1/naver/shopping/categories | Naver Shopping category reference
[**naver_naver_shopping_trending_keyword_rankings**](NaverApi.md#naver_naver_shopping_trending_keyword_rankings) | **GET** /v1/naver/shopping/keywords | Naver Shopping trending keyword rankings
[**naver_naver_web_search**](NaverApi.md#naver_naver_web_search) | **GET** /v1/naver/search | Naver web search
[**naver_search_suggestions**](NaverApi.md#naver_search_suggestions) | **GET** /v1/naver/autocomplete | Search suggestions



## naver_naver_blog_search

> serde_json::Value naver_naver_blog_search(query, page)
Naver blog search

Naver blog vertical — post title, blog name and real post URLs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | 검색어 | [required] |
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## naver_naver_datalab_shopping_keyword_insight

> serde_json::Value naver_naver_datalab_shopping_keyword_insight(category_id, start_date, end_date, time_unit, count)
Naver DataLab shopping keyword insight

DataLab Shopping Insight — top search keywords in a category over a window.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category_id** | **String** | DataLab category id (cid), e.g. 50000000 | [required] |
**start_date** | **String** | YYYY-MM-DD | [required] |
**end_date** | **String** | YYYY-MM-DD | [required] |
**time_unit** | Option<**String**> | date | week | month |  |[default to date]
**count** | Option<**i32**> | Keywords to return |  |[default to 20]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## naver_naver_news_search

> serde_json::Value naver_naver_news_search(query, page)
Naver news search

Naver news vertical — publisher, age string and real article URLs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | 검색어 | [required] |
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## naver_naver_place_detail

> serde_json::Value naver_naver_place_detail(place_id)
Naver place detail

Naver Place detail by place id.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**place_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## naver_naver_place_local_search

> serde_json::Value naver_naver_place_local_search(query)
Naver Place/Local search

Naver Place/Local search — name, category, rating, hours status.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Place query, e.g. '성남 카페' | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## naver_naver_place_visitor_reviews

> serde_json::Value naver_naver_place_visitor_reviews(place_id)
Naver place visitor reviews

Visitor reviews for a Naver place — rating, body, reviewer, voted keywords, photos.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**place_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## naver_naver_scraper_health_check

> serde_json::Value naver_naver_scraper_health_check()
Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

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


## naver_naver_scraper_health_check_head

> serde_json::Value naver_naver_scraper_health_check_head()
Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

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


## naver_naver_shopping_bestseller_rankings

> serde_json::Value naver_naver_shopping_bestseller_rankings(category_id, age_type, sort_type, period_type)
Naver Shopping bestseller rankings

Naver Shopping bestseller rankings — ranked products with price, review score, mall.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category_id** | Option<**String**> | Naver shopping category id, or ALL |  |[default to ALL]
**age_type** | Option<**String**> | ALL | MEN_20 | WOMEN_20 | ... |  |[default to ALL]
**sort_type** | Option<**String**> | PRODUCT_CLICK | PRODUCT_BUY |  |[default to PRODUCT_CLICK]
**period_type** | Option<**String**> | DAILY | WEEKLY |  |[default to DAILY]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## naver_naver_shopping_category_reference

> serde_json::Value naver_naver_shopping_category_reference()
Naver Shopping category reference

Naver Shopping top-level category ids (for bestsellers/keywords/insight). Free.

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


## naver_naver_shopping_trending_keyword_rankings

> serde_json::Value naver_naver_shopping_trending_keyword_rankings(category_id, age_type, sort_type, period_type)
Naver Shopping trending keyword rankings

Trending Naver Shopping keywords for a category (snxbest keyword rankings).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category_id** | **String** | Naver shopping category id (see /shopping/categories) | [required] |
**age_type** | Option<**String**> | ALL | MEN_20 | WOMEN_20 | ... |  |[default to ALL]
**sort_type** | Option<**String**> |  |  |[default to KEYWORD_POPULAR]
**period_type** | Option<**String**> | DAILY | WEEKLY |  |[default to WEEKLY]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## naver_naver_web_search

> serde_json::Value naver_naver_web_search(query, page)
Naver web search

Naver integrated SERP — organic results plus the inline Place pack.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | 검색어, e.g. '성남 카페' | [required] |
**page** | Option<**i32**> | Result page |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## naver_search_suggestions

> serde_json::Value naver_search_suggestions(query)
Search suggestions

Naver search-box suggestions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial search term | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

