# \BingApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bing_bing_scraper_health_check**](BingApi.md#bing_bing_scraper_health_check) | **GET** /v1/bing/health | Bing scraper health check
[**bing_bing_scraper_health_check_head**](BingApi.md#bing_bing_scraper_health_check_head) | **HEAD** /v1/bing/health | Bing scraper health check
[**bing_image_search**](BingApi.md#bing_image_search) | **GET** /v1/bing/images | Image search
[**bing_list_supported_markets**](BingApi.md#bing_list_supported_markets) | **GET** /v1/bing/markets | List supported markets
[**bing_news_search**](BingApi.md#bing_news_search) | **GET** /v1/bing/news | News search
[**bing_search_suggestions**](BingApi.md#bing_search_suggestions) | **GET** /v1/bing/autocomplete | Search suggestions
[**bing_video_search**](BingApi.md#bing_video_search) | **GET** /v1/bing/videos | Video search
[**bing_web_search**](BingApi.md#bing_web_search) | **GET** /v1/bing/search | Web search



## bing_bing_scraper_health_check

> serde_json::Value bing_bing_scraper_health_check()
Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

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


## bing_bing_scraper_health_check_head

> serde_json::Value bing_bing_scraper_health_check_head()
Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

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


## bing_image_search

> serde_json::Value bing_image_search(query, market, count, safe_search)
Image search

Bing Images — thumbnail, full-size and source URL per result.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. 'golden retriever' | [required] |
**market** | Option<**String**> | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. |  |[default to en-US]
**count** | Option<**i32**> | Results to return |  |[default to 35]
**safe_search** | Option<**String**> | off | moderate | strict |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bing_list_supported_markets

> serde_json::Value bing_list_supported_markets()
List supported markets

Supported Bing market codes. Free — costs no credits.

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


## bing_news_search

> serde_json::Value bing_news_search(query, market, freshness)
News search

Bing News — headline, source, published time and snippet per article.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. 'interest rates' | [required] |
**market** | Option<**String**> | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. |  |[default to en-US]
**freshness** | Option<**String**> | day | week | month — restrict to recent articles |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bing_search_suggestions

> serde_json::Value bing_search_suggestions(query, market)
Search suggestions

Bing search-box query suggestions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial search term, e.g. 'coff' | [required] |
**market** | Option<**String**> | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. |  |[default to en-US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bing_video_search

> serde_json::Value bing_video_search(query, market, count, safe_search)
Video search

Bing Videos — title, thumbnail, duration, publisher and source per result.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. 'espresso tutorial' | [required] |
**market** | Option<**String**> | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. |  |[default to en-US]
**count** | Option<**i32**> | Results to return |  |[default to 35]
**safe_search** | Option<**String**> | off | moderate | strict |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bing_web_search

> serde_json::Value bing_web_search(query, market, count, offset, safe_search)
Web search

Bing web SERP — organic results, ads, related searches and total count.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. 'coffee machine' | [required] |
**market** | Option<**String**> | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. |  |[default to en-US]
**count** | Option<**i32**> | Results per page (1-50) |  |[default to 10]
**offset** | Option<**i32**> | Zero-based result offset for pagination |  |[default to 0]
**safe_search** | Option<**String**> | off | moderate | strict (default moderate) |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

