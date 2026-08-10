# \ChatGptApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chatgpt_ask_chatgpt_a_question**](ChatGptApi.md#chatgpt_ask_chatgpt_a_question) | **GET** /v1/chatgpt/ask | Ask ChatGPT a question
[**chatgpt_ask_chatgpt_a_question_post**](ChatGptApi.md#chatgpt_ask_chatgpt_a_question_post) | **POST** /v1/chatgpt/ask | Ask ChatGPT a question (POST)
[**chatgpt_chatgpt_scraper_health_check**](ChatGptApi.md#chatgpt_chatgpt_scraper_health_check) | **GET** /v1/chatgpt/health | ChatGPT scraper health check
[**chatgpt_chatgpt_scraper_health_check_head**](ChatGptApi.md#chatgpt_chatgpt_scraper_health_check_head) | **HEAD** /v1/chatgpt/health | ChatGPT scraper health check
[**chatgpt_list_chatgpt_models**](ChatGptApi.md#chatgpt_list_chatgpt_models) | **GET** /v1/chatgpt/models | List ChatGPT models
[**chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer**](ChatGptApi.md#chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer) | **GET** /v1/chatgpt/brand-visibility | Measure a brand's visibility in a ChatGPT answer
[**chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post**](ChatGptApi.md#chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post) | **POST** /v1/chatgpt/brand-visibility | Measure a brand's visibility in a ChatGPT answer (POST)



## chatgpt_ask_chatgpt_a_question

> serde_json::Value chatgpt_ask_chatgpt_a_question(prompt, country, web_search)
Ask ChatGPT a question

Send a prompt to ChatGPT and get the answer plus the web sources it cited.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | The prompt to send to ChatGPT (max 4096 characters). | [required] |
**country** | Option<**String**> | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. |  |
**web_search** | Option<**String**> | auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened. |  |[default to auto]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## chatgpt_ask_chatgpt_a_question_post

> serde_json::Value chatgpt_ask_chatgpt_a_question_post()
Ask ChatGPT a question (POST)

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


## chatgpt_chatgpt_scraper_health_check

> serde_json::Value chatgpt_chatgpt_scraper_health_check()
ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

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


## chatgpt_chatgpt_scraper_health_check_head

> serde_json::Value chatgpt_chatgpt_scraper_health_check_head()
ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

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


## chatgpt_list_chatgpt_models

> serde_json::Value chatgpt_list_chatgpt_models(country)
List ChatGPT models

Models chatgpt.com currently serves to an anonymous visitor.

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


## chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer

> serde_json::Value chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer(prompt, brand, domain, aliases, competitors, country, web_search)
Measure a brand's visibility in a ChatGPT answer

Ask ChatGPT, then report whether the brand is mentioned, cited and how prominently.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | The prompt to ask ChatGPT. | [required] |
**brand** | **String** | Brand name to look for in the answer. | [required] |
**domain** | Option<**String**> | Brand domain, for citation matching. |  |
**aliases** | Option<**String**> | Comma-separated alternative names. |  |
**competitors** | Option<**String**> | Comma-separated competitor names. |  |
**country** | Option<**String**> | ISO-3166 alpha-2 egress country. |  |
**web_search** | Option<**String**> | auto | force | off |  |[default to force]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post

> serde_json::Value chatgpt_measure_a_brand_s_visibility_in_a_chatgpt_answer_post()
Measure a brand's visibility in a ChatGPT answer (POST)

POST form, for longer prompts and larger competitor sets.

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

