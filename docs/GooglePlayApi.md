# \GooglePlayApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**google_play_browse_a_category**](GooglePlayApi.md#google_play_browse_a_category) | **GET** /v1/google-play/categories/{category_id} | Browse a category
[**google_play_get_app_detail**](GooglePlayApi.md#google_play_get_app_detail) | **GET** /v1/google-play/apps/{app_id} | Get app detail
[**google_play_get_app_permissions**](GooglePlayApi.md#google_play_get_app_permissions) | **GET** /v1/google-play/apps/{app_id}/permissions | Get app permissions
[**google_play_get_app_reviews**](GooglePlayApi.md#google_play_get_app_reviews) | **GET** /v1/google-play/apps/{app_id}/reviews | Get app reviews
[**google_play_get_developer_apps**](GooglePlayApi.md#google_play_get_developer_apps) | **GET** /v1/google-play/developers/{developer} | Get developer apps
[**google_play_get_similar_apps**](GooglePlayApi.md#google_play_get_similar_apps) | **GET** /v1/google-play/apps/{app_id}/similar | Get similar apps
[**google_play_list_categories**](GooglePlayApi.md#google_play_list_categories) | **GET** /v1/google-play/categories | List categories
[**google_play_list_markets**](GooglePlayApi.md#google_play_list_markets) | **GET** /v1/google-play/markets | List markets
[**google_play_search_apps**](GooglePlayApi.md#google_play_search_apps) | **GET** /v1/google-play/search | Search apps
[**google_play_top_charts**](GooglePlayApi.md#google_play_top_charts) | **GET** /v1/google-play/collections/{collection} | Top charts



## google_play_browse_a_category

> serde_json::Value google_play_browse_a_category(category_id, country, lang, num)
Browse a category

The top apps within a Play category.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category_id** | **String** | Play category id, e.g. 'GAME_PUZZLE' or 'SOCIAL' | [required] |
**country** | Option<**String**> | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' |  |[default to US]
**lang** | Option<**String**> | Play content language (hl), e.g. 'en' or 'pt-BR' |  |[default to en]
**num** | Option<**i32**> | Max apps; follows each rail's 'see more' continuation above the ~40-120 the page renders directly |  |[default to 100]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_play_get_app_detail

> serde_json::Value google_play_get_app_detail(app_id, country, lang)
Get app detail

Full app detail: ratings histogram, installs, pricing, IAP, developer, screenshots, version metadata and what's-new.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**app_id** | **String** | Android package id, e.g. 'com.whatsapp'. | [required] |
**country** | Option<**String**> | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' |  |[default to US]
**lang** | Option<**String**> | Play content language (hl), e.g. 'en' or 'pt-BR' |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_play_get_app_permissions

> serde_json::Value google_play_get_app_permissions(app_id, lang)
Get app permissions

The app's requested Android permissions, grouped.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**app_id** | **String** | Android package id, e.g. 'com.whatsapp'. | [required] |
**lang** | Option<**String**> | Play content language (hl), e.g. 'en' or 'pt-BR' |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_play_get_app_reviews

> serde_json::Value google_play_get_app_reviews(app_id, country, lang, sort, count, page_token)
Get app reviews

Paginated app reviews via the Play batchexecute RPC.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**app_id** | **String** | Android package id, e.g. 'com.whatsapp'. | [required] |
**country** | Option<**String**> | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' |  |[default to US]
**lang** | Option<**String**> | Play content language (hl), e.g. 'en' or 'pt-BR' |  |[default to en]
**sort** | Option<**String**> | newest | rating | helpfulness |  |[default to newest]
**count** | Option<**i32**> |  |  |[default to 40]
**page_token** | Option<**String**> | Pagination token |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_play_get_developer_apps

> serde_json::Value google_play_get_developer_apps(developer, country, lang, num)
Get developer apps

A developer's published apps.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**developer** | **String** | Developer name or numeric id | [required] |
**country** | Option<**String**> | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' |  |[default to US]
**lang** | Option<**String**> | Play content language (hl), e.g. 'en' or 'pt-BR' |  |[default to en]
**num** | Option<**i32**> | Max apps; follows rail continuations above the page's directly-rendered slice |  |[default to 100]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_play_get_similar_apps

> serde_json::Value google_play_get_similar_apps(app_id, country, lang)
Get similar apps

Apps Google Play lists as similar to this one.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**app_id** | **String** | Android package id, e.g. 'com.whatsapp'. | [required] |
**country** | Option<**String**> | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' |  |[default to US]
**lang** | Option<**String**> | Play content language (hl), e.g. 'en' or 'pt-BR' |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_play_list_categories

> serde_json::Value google_play_list_categories()
List categories

The Google Play app/game category ids.

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


## google_play_list_markets

> serde_json::Value google_play_list_markets()
List markets

Supported Google Play store countries and languages.

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


## google_play_search_apps

> serde_json::Value google_play_search_apps(query, country, lang, price)
Search apps

Search Google Play for apps and games (the ~30 server-rendered results; Play exposes no page parameter).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords, e.g. 'puzzle' | [required] |
**country** | Option<**String**> | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' |  |[default to US]
**lang** | Option<**String**> | Play content language (hl), e.g. 'en' or 'pt-BR' |  |[default to en]
**price** | Option<**String**> | free | paid | all |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## google_play_top_charts

> serde_json::Value google_play_top_charts(collection, category, country, lang)
Top charts

Top charts for a collection, optionally scoped to a category.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**collection** | **String** | topselling_free | topselling_paid | topgrossing | [required] |
**category** | Option<**String**> | Play category, e.g. 'GAME' |  |[default to APPLICATION]
**country** | Option<**String**> | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' |  |[default to US]
**lang** | Option<**String**> | Play content language (hl), e.g. 'en' or 'pt-BR' |  |[default to en]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

