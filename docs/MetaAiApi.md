# \MetaAiApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**meta_ai_ask_meta_ai_a_question**](MetaAiApi.md#meta_ai_ask_meta_ai_a_question) | **GET** /v1/meta-ai/ask | Ask Meta AI a question
[**meta_ai_ask_meta_ai_a_question_post**](MetaAiApi.md#meta_ai_ask_meta_ai_a_question_post) | **POST** /v1/meta-ai/ask | Ask Meta AI a question (POST)
[**meta_ai_list_meta_ai_assistant_modes**](MetaAiApi.md#meta_ai_list_meta_ai_assistant_modes) | **GET** /v1/meta-ai/models | List Meta AI assistant modes
[**meta_ai_meta_ai_scraper_health_check**](MetaAiApi.md#meta_ai_meta_ai_scraper_health_check) | **GET** /v1/meta-ai/health | Meta AI scraper health check
[**meta_ai_meta_ai_scraper_health_check_head**](MetaAiApi.md#meta_ai_meta_ai_scraper_health_check_head) | **HEAD** /v1/meta-ai/health | Meta AI scraper health check



## meta_ai_ask_meta_ai_a_question

> serde_json::Value meta_ai_ask_meta_ai_a_question(prompt, country)
Ask Meta AI a question

Send a prompt to meta.ai and get the answer (anonymous, no Meta account).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | The prompt to send to Meta AI (max 4000 characters). | [required] |
**country** | Option<**String**> | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## meta_ai_ask_meta_ai_a_question_post

> serde_json::Value meta_ai_ask_meta_ai_a_question_post()
Ask Meta AI a question (POST)

POST form of `/ask`, for prompts too long for a query string.

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


## meta_ai_list_meta_ai_assistant_modes

> serde_json::Value meta_ai_list_meta_ai_assistant_modes(country)
List Meta AI assistant modes

Assistant modes meta.ai currently serves to an anonymous visitor.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country** | Option<**String**> | ISO-3166 alpha-2 egress country. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## meta_ai_meta_ai_scraper_health_check

> serde_json::Value meta_ai_meta_ai_scraper_health_check()
Meta AI scraper health check

Check health of the Meta AI scraper service (accepts HEAD).

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


## meta_ai_meta_ai_scraper_health_check_head

> serde_json::Value meta_ai_meta_ai_scraper_health_check_head()
Meta AI scraper health check

Check health of the Meta AI scraper service (accepts HEAD).

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

