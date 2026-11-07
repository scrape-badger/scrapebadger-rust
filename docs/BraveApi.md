# \BraveApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**brave_autocomplete**](BraveApi.md#brave_autocomplete) | **GET** /v1/brave/autocomplete | Autocomplete
[**brave_image_search**](BraveApi.md#brave_image_search) | **GET** /v1/brave/images | Image search
[**brave_list_supported_locales**](BraveApi.md#brave_list_supported_locales) | **GET** /v1/brave/locales | List supported locales
[**brave_news_search**](BraveApi.md#brave_news_search) | **GET** /v1/brave/news | News search
[**brave_video_search**](BraveApi.md#brave_video_search) | **GET** /v1/brave/videos | Video search
[**brave_web_search**](BraveApi.md#brave_web_search) | **GET** /v1/brave/search | Web search



## brave_autocomplete

> models::BraveAutocompleteResponse brave_autocomplete(query, country)
Autocomplete

Native search-box suggestions with entity descriptions and images. Two credits.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**country** | Option<**String**> |  |  |[default to us]

### Return type

[**models::BraveAutocompleteResponse**](BraveAutocompleteResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## brave_image_search

> models::BraveResponse brave_image_search(query, country, ui_language, safe_search, count)
Image search

Native image batch with original URLs, source pages, thumbnails and dimensions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Native Brave search query | [required] |
**country** | Option<**String**> | Native result region; see /locales |  |[default to us]
**ui_language** | Option<**String**> | UI labels/date language; does not restrict result language |  |[default to en-us]
**safe_search** | Option<**String**> |  |  |[default to moderate]
**count** | Option<**i32**> | Slice the initial native image batch |  |[default to 50]

### Return type

[**models::BraveResponse**](BraveResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## brave_list_supported_locales

> models::BraveLocalesResponse brave_list_supported_locales()
List supported locales

Native country and UI-language choices. Free; result language is a separate preference.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::BraveLocalesResponse**](BraveLocalesResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## brave_news_search

> models::BraveResponse brave_news_search(query, country, ui_language, safe_search, count)
News search

Native news batch; relative source dates stay display strings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Native Brave search query | [required] |
**country** | Option<**String**> | Native result region; see /locales |  |[default to us]
**ui_language** | Option<**String**> | UI labels/date language; does not restrict result language |  |[default to en-us]
**safe_search** | Option<**String**> |  |  |[default to moderate]
**count** | Option<**i32**> | Slice the initial native news batch |  |[default to 35]

### Return type

[**models::BraveResponse**](BraveResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## brave_video_search

> models::BravePagedResponse brave_video_search(query, country, ui_language, safe_search, page, count)
Video search

Native video results with duration, creator, publisher and verified page ordinals.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Native Brave search query | [required] |
**country** | Option<**String**> | Native result region; see /locales |  |[default to us]
**ui_language** | Option<**String**> | UI labels/date language; does not restrict result language |  |[default to en-us]
**safe_search** | Option<**String**> |  |  |[default to moderate]
**page** | Option<**i32**> | 1-based native page ordinal |  |[default to 1]
**count** | Option<**i32**> |  |  |[default to 50]

### Return type

[**models::BravePagedResponse**](BravePagedResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## brave_web_search

> models::BraveSearchResponse brave_web_search(query, country, ui_language, safe_search, page, count, freshness, spellcheck)
Web search

Native Brave organic results, rich source blocks and page metadata. Seven credits.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Native Brave search query | [required] |
**country** | Option<**String**> | Native result region; see /locales |  |[default to us]
**ui_language** | Option<**String**> | UI labels/date language; does not restrict result language |  |[default to en-us]
**safe_search** | Option<**String**> |  |  |[default to moderate]
**page** | Option<**i32**> | 1-based native page ordinal |  |[default to 1]
**count** | Option<**i32**> | Slice one native page; does not change native page boundaries |  |[default to 20]
**freshness** | Option<**String**> |  |  |[default to any]
**spellcheck** | Option<**bool**> | Allow native spelling correction |  |[default to false]

### Return type

[**models::BraveSearchResponse**](BraveSearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

