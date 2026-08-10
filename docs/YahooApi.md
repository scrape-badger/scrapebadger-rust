# \YahooApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**yahoo_image_search**](YahooApi.md#yahoo_image_search) | **GET** /v1/yahoo/images | Image search
[**yahoo_list_supported_markets**](YahooApi.md#yahoo_list_supported_markets) | **GET** /v1/yahoo/markets | List supported markets
[**yahoo_news_search**](YahooApi.md#yahoo_news_search) | **GET** /v1/yahoo/news | News search
[**yahoo_search_suggestions**](YahooApi.md#yahoo_search_suggestions) | **GET** /v1/yahoo/autocomplete | Search suggestions
[**yahoo_video_search**](YahooApi.md#yahoo_video_search) | **GET** /v1/yahoo/videos | Video search
[**yahoo_web_search**](YahooApi.md#yahoo_web_search) | **GET** /v1/yahoo/search | Web search
[**yahoo_yahoo_scraper_health_check**](YahooApi.md#yahoo_yahoo_scraper_health_check) | **GET** /v1/yahoo/health | Yahoo scraper health check
[**yahoo_yahoo_scraper_health_check_head**](YahooApi.md#yahoo_yahoo_scraper_health_check_head) | **HEAD** /v1/yahoo/health | Yahoo scraper health check



## yahoo_image_search

> serde_json::Value yahoo_image_search(query, market, count)
Image search

Yahoo Images — thumbnail, full-size and source URL per result.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. 'golden retriever' | [required] |
**market** | Option<**String**> | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. |  |[default to us]
**count** | Option<**i32**> | Results to return |  |[default to 30]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yahoo_list_supported_markets

> serde_json::Value yahoo_list_supported_markets()
List supported markets

Supported Yahoo market codes. Free — costs no credits.

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


## yahoo_news_search

> serde_json::Value yahoo_news_search(query, market)
News search

Yahoo News — headline, source, published time and snippet per article.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. 'interest rates' | [required] |
**market** | Option<**String**> | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yahoo_search_suggestions

> serde_json::Value yahoo_search_suggestions(query, market)
Search suggestions

Yahoo search-box query suggestions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial search term, e.g. 'coff' | [required] |
**market** | Option<**String**> | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yahoo_video_search

> serde_json::Value yahoo_video_search(query, market, count)
Video search

Yahoo Videos — title, thumbnail, duration, publisher and source per result.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. 'espresso tutorial' | [required] |
**market** | Option<**String**> | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. |  |[default to us]
**count** | Option<**i32**> | Results to return |  |[default to 30]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yahoo_web_search

> serde_json::Value yahoo_web_search(query, market, offset, safe_search)
Web search

Yahoo web SERP — organic results, ads, related searches and total count.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. 'coffee machine' | [required] |
**market** | Option<**String**> | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. |  |[default to us]
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


## yahoo_yahoo_scraper_health_check

> serde_json::Value yahoo_yahoo_scraper_health_check()
Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

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


## yahoo_yahoo_scraper_health_check_head

> serde_json::Value yahoo_yahoo_scraper_health_check_head()
Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

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

