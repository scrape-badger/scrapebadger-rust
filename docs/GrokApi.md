# \GrokApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**grok_ask_grok_a_question**](GrokApi.md#grok_ask_grok_a_question) | **GET** /v1/grok/ask | Ask Grok a question
[**grok_ask_grok_a_question_post**](GrokApi.md#grok_ask_grok_a_question_post) | **POST** /v1/grok/ask | Ask Grok a question (POST)
[**grok_get_a_grok_conversation**](GrokApi.md#grok_get_a_grok_conversation) | **GET** /v1/grok/conversations/{conversation_id} | Get a Grok conversation
[**grok_grok_scraper_health_check**](GrokApi.md#grok_grok_scraper_health_check) | **GET** /v1/grok/health | Grok scraper health check
[**grok_grok_scraper_health_check_head**](GrokApi.md#grok_grok_scraper_health_check_head) | **HEAD** /v1/grok/health | Grok scraper health check
[**grok_list_grok_assistant_modes**](GrokApi.md#grok_list_grok_assistant_modes) | **GET** /v1/grok/models | List Grok assistant modes
[**grok_measure_brand_visibility_in_grok**](GrokApi.md#grok_measure_brand_visibility_in_grok) | **GET** /v1/grok/brand-visibility | Measure brand visibility in Grok
[**grok_measure_brand_visibility_in_grok_post**](GrokApi.md#grok_measure_brand_visibility_in_grok_post) | **POST** /v1/grok/brand-visibility | Measure brand visibility in Grok (POST)



## grok_ask_grok_a_question

> serde_json::Value grok_ask_grok_a_question(prompt, conversation_id, mode, web_search)
Ask Grok a question

Ask the real Grok assistant and get its answer, web sources, and X post references.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | Prompt to send to Grok (max 4000 characters). | [required] |
**conversation_id** | Option<**String**> | Existing Grok conversation to continue. |  |
**mode** | Option<**String**> | Assistant mode: auto, fast, or expert. |  |[default to auto]
**web_search** | Option<**String**> | Web and X search: auto, force, or off. |  |[default to auto]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## grok_ask_grok_a_question_post

> serde_json::Value grok_ask_grok_a_question_post()
Ask Grok a question (POST)

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


## grok_get_a_grok_conversation

> serde_json::Value grok_get_a_grok_conversation(conversation_id)
Get a Grok conversation

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## grok_grok_scraper_health_check

> serde_json::Value grok_grok_scraper_health_check()
Grok scraper health check

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


## grok_grok_scraper_health_check_head

> serde_json::Value grok_grok_scraper_health_check_head()
Grok scraper health check

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


## grok_list_grok_assistant_modes

> serde_json::Value grok_list_grok_assistant_modes()
List Grok assistant modes

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


## grok_measure_brand_visibility_in_grok

> serde_json::Value grok_measure_brand_visibility_in_grok(prompt, brand, competitors, brand_domain, mode, web_search)
Measure brand visibility in Grok

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | Buyer or category prompt to send to Grok. | [required] |
**brand** | **String** | Brand name to measure. | [required] |
**competitors** | Option<[**Vec<String>**](String.md)> | Competitor brand names. |  |[default to []]
**brand_domain** | Option<**String**> | Brand domain for citation rank. |  |
**mode** | Option<**String**> | Assistant mode: auto, fast, or expert. |  |[default to auto]
**web_search** | Option<**String**> | Web and X search mode. |  |[default to force]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## grok_measure_brand_visibility_in_grok_post

> serde_json::Value grok_measure_brand_visibility_in_grok_post()
Measure brand visibility in Grok (POST)

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

