# \DuckDuckGoApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**duckduckgo_duckduckgo_scraper_health_check**](DuckDuckGoApi.md#duckduckgo_duckduckgo_scraper_health_check) | **GET** /v1/duckduckgo/health | DuckDuckGo scraper health check
[**duckduckgo_duckduckgo_scraper_health_check_head**](DuckDuckGoApi.md#duckduckgo_duckduckgo_scraper_health_check_head) | **HEAD** /v1/duckduckgo/health | DuckDuckGo scraper health check
[**duckduckgo_image_search**](DuckDuckGoApi.md#duckduckgo_image_search) | **GET** /v1/duckduckgo/images | Image search
[**duckduckgo_instant_answer**](DuckDuckGoApi.md#duckduckgo_instant_answer) | **GET** /v1/duckduckgo/instant | Instant Answer
[**duckduckgo_list_supported_regions**](DuckDuckGoApi.md#duckduckgo_list_supported_regions) | **GET** /v1/duckduckgo/regions | List supported regions
[**duckduckgo_news_search**](DuckDuckGoApi.md#duckduckgo_news_search) | **GET** /v1/duckduckgo/news | News search
[**duckduckgo_search_suggestions**](DuckDuckGoApi.md#duckduckgo_search_suggestions) | **GET** /v1/duckduckgo/autocomplete | Search suggestions
[**duckduckgo_video_search**](DuckDuckGoApi.md#duckduckgo_video_search) | **GET** /v1/duckduckgo/videos | Video search
[**duckduckgo_web_search**](DuckDuckGoApi.md#duckduckgo_web_search) | **GET** /v1/duckduckgo/search | Web search



## duckduckgo_duckduckgo_scraper_health_check

> serde_json::Value duckduckgo_duckduckgo_scraper_health_check()
DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

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


## duckduckgo_duckduckgo_scraper_health_check_head

> serde_json::Value duckduckgo_duckduckgo_scraper_health_check_head()
DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

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


## duckduckgo_image_search

> serde_json::Value duckduckgo_image_search(query, region, safesearch, page, size, color, image_type, layout, license)
Image search

DuckDuckGo image search with size/color/type/layout/license filters.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search query | [required] |
**region** | Option<**String**> | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. |  |[default to wt-wt]
**safesearch** | Option<**String**> | on | moderate | off |  |[default to moderate]
**page** | Option<**i32**> | 100 results per page |  |[default to 1]
**size** | Option<**String**> | Small | Medium | Large | Wallpaper |  |[default to ]
**color** | Option<**String**> | color | Monochrome | Red | Blue | … |  |[default to ]
**image_type** | Option<**String**> | photo | clipart | gif | transparent | line |  |[default to ]
**layout** | Option<**String**> | Square | Tall | Wide |  |[default to ]
**license** | Option<**String**> | Any | Public | Share | ShareCommercially | Modify |  |[default to ]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duckduckgo_instant_answer

> serde_json::Value duckduckgo_instant_answer(query)
Instant Answer

DuckDuckGo Instant Answer — abstract, definition, direct answer, related topics.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Query for the Instant Answer API | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duckduckgo_list_supported_regions

> serde_json::Value duckduckgo_list_supported_regions()
List supported regions

The full DuckDuckGo region (kl) code list.

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


## duckduckgo_news_search

> serde_json::Value duckduckgo_news_search(query, region, safesearch, timelimit, page)
News search

DuckDuckGo news search — headline, source, excerpt, unix + ISO date, image.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search query | [required] |
**region** | Option<**String**> | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. |  |[default to wt-wt]
**safesearch** | Option<**String**> | on | moderate | off |  |[default to moderate]
**timelimit** | Option<**String**> | day | week | month | year |  |[default to ]
**page** | Option<**i32**> | 30 results per page |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duckduckgo_search_suggestions

> serde_json::Value duckduckgo_search_suggestions(query, region)
Search suggestions

DuckDuckGo search-box suggestions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial query to complete | [required] |
**region** | Option<**String**> | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. |  |[default to wt-wt]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duckduckgo_video_search

> serde_json::Value duckduckgo_video_search(query, region, safesearch, page, duration, resolution)
Video search

DuckDuckGo video search — title, publisher, uploader, duration, views, thumbnails.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search query | [required] |
**region** | Option<**String**> | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. |  |[default to wt-wt]
**safesearch** | Option<**String**> | on | moderate | off |  |[default to moderate]
**page** | Option<**i32**> | 60 results per page |  |[default to 1]
**duration** | Option<**String**> | short | medium | long |  |[default to ]
**resolution** | Option<**String**> | high | standard |  |[default to ]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duckduckgo_web_search

> serde_json::Value duckduckgo_web_search(query, region, safesearch, timelimit, page)
Web search

DuckDuckGo web SERP — organic results, the zero-click abstract box, ads flagged.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search query | [required] |
**region** | Option<**String**> | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. |  |[default to wt-wt]
**safesearch** | Option<**String**> | on | moderate | off |  |[default to moderate]
**timelimit** | Option<**String**> | day | week | month | year |  |[default to ]
**page** | Option<**i32**> |  |  |[default to 1]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

