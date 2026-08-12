# \AppStoreApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**app_store_get_app_detail**](AppStoreApi.md#app_store_get_app_detail) | **GET** /v1/app-store/apps/{app_id} | Get app detail
[**app_store_get_app_reviews**](AppStoreApi.md#app_store_get_app_reviews) | **GET** /v1/app-store/apps/{app_id}/reviews | Get app reviews
[**app_store_get_developer_apps**](AppStoreApi.md#app_store_get_developer_apps) | **GET** /v1/app-store/developers/{artist_id} | Get developer apps
[**app_store_list_genres**](AppStoreApi.md#app_store_list_genres) | **GET** /v1/app-store/genres | List genres
[**app_store_list_markets**](AppStoreApi.md#app_store_list_markets) | **GET** /v1/app-store/markets | List markets
[**app_store_search_apps**](AppStoreApi.md#app_store_search_apps) | **GET** /v1/app-store/search | Search apps
[**app_store_top_charts**](AppStoreApi.md#app_store_top_charts) | **GET** /v1/app-store/charts | Top charts



## app_store_get_app_detail

> serde_json::Value app_store_get_app_detail(app_id, country, lang, include_extras)
Get app detail

App detail: bundle id, version, pricing, ratings, genres, min OS, size, languages, screenshots, in-app purchases and version history.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**app_id** | **String** | Numeric trackId (e.g. '310633997') or bundle id (e.g. 'net.whatsapp.WhatsApp'). | [required] |
**country** | Option<**String**> |  |  |[default to us]
**lang** | Option<**String**> | Result language, e.g. 'en_us' |  |
**include_extras** | Option<**bool**> | Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch. |  |[default to true]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## app_store_get_app_reviews

> serde_json::Value app_store_get_app_reviews(app_id, country, page, sort)
Get app reviews

Paginated customer reviews (50 per page, up to 10 pages).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**app_id** | **String** | Numeric trackId, e.g. '310633997' | [required] |
**country** | Option<**String**> |  |  |[default to us]
**page** | Option<**i32**> | Apple caps reviews at 10 pages |  |[default to 1]
**sort** | Option<**String**> | mostRecent | mostHelpful |  |[default to mostRecent]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## app_store_get_developer_apps

> serde_json::Value app_store_get_developer_apps(artist_id, country)
Get developer apps

Developer info and their published apps.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**artist_id** | **String** | Numeric artistId (developer id) | [required] |
**country** | Option<**String**> |  |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## app_store_list_genres

> serde_json::Value app_store_list_genres()
List genres

The Apple App Store genre/category ids.

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


## app_store_list_markets

> serde_json::Value app_store_list_markets()
List markets

Supported App Store country codes.

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


## app_store_search_apps

> serde_json::Value app_store_search_apps(query, country, entity, limit, offset, lang)
Search apps

Search the Apple App Store.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search term, e.g. 'chat' | [required] |
**country** | Option<**String**> | App Store country code |  |[default to us]
**entity** | Option<**String**> | software | iPadSoftware | macSoftware |  |[default to software]
**limit** | Option<**i32**> |  |  |[default to 25]
**offset** | Option<**i32**> |  |  |[default to 0]
**lang** | Option<**String**> | Language, e.g. 'en_us' |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## app_store_top_charts

> serde_json::Value app_store_top_charts(country, r#type, genre, limit, entity)
Top charts

Top charts, optionally scoped to a genre.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country** | Option<**String**> |  |  |[default to us]
**r#type** | Option<**String**> | top-free | top-paid | top-grossing |  |[default to top-free]
**genre** | Option<**i32**> | Apple genre id (optional), e.g. 6014 |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**entity** | Option<**String**> | apps (iPhone) | ipad |  |[default to apps]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

